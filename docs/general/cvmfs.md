# CVMFS

UChicago hosts the CVMFS origin server (`osg-cvmfs.grid.uchicago.edu`) for several
experiments and the OSG module system. This server is a CentOS7 VM with 
singularity that can be used to build EL6 versions of software. The 
repositories are associated with a respective user, e.g. 
`spt.opensciencegrid.org` has an `spt` user, that are typically accessible to 
the relevant members of the experiments.  The VM is fairly large with 8 cores 
and 16 GB RAM. The `/cvmfs` directory is a separate disk that can be resized 
if need be.

## Modules

The modules are hosted out of the `connect.opensciencegrid.org` subrepo. They
are setup using [spack](https://spack.io/). A good place to start understanding 
spack is the spack tutuorial available 
[here](https://spack.readthedocs.io/en/latest/tutorial.html). There is a 
[fork of spack in the OSG Connect GitHub](https://github.com/OSGConnect/spack) 
which contains a few necessary changes and additional packages. The main change 
required for OSG is that CentOS instances are considered the same as RHEL or 
SL. This is an artifact from using the python `platform` package.

### Path Structure

The structure for the software is as follows:

* `/cvmfs/connect.opensciencegrid.org`
** `modules` - Main directory
*** `spack` - Spack instances
*** `packages` - Where individual packages are installed
*** `modulefiles` - Where lmod files are located


### Configuration

There are some important spack config files that may need adjusting over time, 
esp. when trying to reconfigure the module structure or adding new 
features:

`SPACK_ROOT=/cvmfs/connect.opensciencegrid.org/modules/spack`

* `$HOME/.spack/linux/compilers.yaml`

This defines the compilers that can be used by spack. We currently list two 
compilers by default here: GCC 4.8.5 installed using spack and GCC 6.4.0 also
installed using spack. We had to install GCC 4.8.5 (system compiler for EL7) 
because certain programs, e.g. R, require `libgfortran` to be present to run. 
This is not guaranteed on OSG since some nodes do not have any development 
tools installed. GCC 6.4.0 is needed for support for C++14. 

* `$SPACK_ROOT/etc/spack/config.yaml`

Defines global configuration parameters for spack. In our case this is just 
_where_ the packages will installed (`install_tree`) and _where_ the module
files will be located (`module_roots/lmod`). For other options see 
(here)[https://spack.readthedocs.io/en/latest/config_yaml.html#config-yaml]

* `$SPACK_ROOT/etc/spack/packages.yaml`

Defines the global or package specific settings for build variants. This means 
that it allows one to turn on or off certain package-specific configuration 
parameters. In our case, we want to disable the need for packages to compile 
with MPI support and reduce the number of versions of certain libraries, e.g. 
always compile `libxml2` with python support.

* `$SPACK_ROOT/etc/spack/modules.yaml`

Defines the organization and general settings for creating module files. For 
example, in our cause we have suffixes to differentiate versions that depend
on Python 2.7 and 3.7 and only the lmod modules are enabled.

### Adding a Module

Adding a new module is fairly straight forward. On the CVMFS origin host, log 
in as the `connect` user. Now start a CVMFS transaction:

```
cvmfs_server transaction connect.opensciencegrid.org
```

Please note that only a single transaction can be open at a time, so if you 
don't finish the transaction (for example building ROOT takes hours) no one 
else can add new modules while a transaction is active. 

Once the transaction has been started, go to the spack `bin` directory, 
`$SPACK_ROOT/bin/`:

``` cd /cvmfs/connect.opensciencegrid.org/modules/spack/bin```

If the desired piece of software and version is available in the (spack
package list)[https://spack.readthedocs.io/en/latest/package_list.html], simply 
run

```
spack install <package>@<version>%gcc@<gcc_version>
```

To check what `<gcc_version>`s are available see 
`$HOME/.spack/linux/compilers.yaml`

Adding a new version of a piece of software requires editing the respective 
package file using

```
spack edit <package>
```

Adding a new package is fairly straightforward as well. Simply run

```
spack create <url_to_package_tarball>
```

and edit the resulting file as needed, e.g. add dependencies, add 
configure/cmake options, etc. For examples check out various other packages in 
`$SPACK_ROOT/var/spack/repos/builtin/packages/`.

# Experiments

## SPT

See Midscale-Engagements

## XENON

See Midscale-Engagements

## VERITAS

See Midscale-Engagements

## nEXO

The nEXO repository is handled by OSG personnel. The organization is the same 
as the SPT repos. The repo is very much in flux because of the development of 
the nEXO MonteCarlo software.

### Dependency List

Shortened list
Boost 1.67.0
cmake 3.11.1
geant4 10.04.p01
python 2.7.14
ROOT 6.12.06 with builtin_fftw3, using our gsl 1.16, minuit on, caster off, 
roofit on, rfio off, xrootd off, gfal and ruby disabled 
vgm 4.4  http://ivana.home.cern.ch

