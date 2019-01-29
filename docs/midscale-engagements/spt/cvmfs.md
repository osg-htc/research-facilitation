# CVMFS 

The SPT repo is handled by the experiment. The point of contact is Nathan
Whitehorn. The structure follows a fairly simple pattern: 
`py2-v1/<os_architecture>`, `py3-v1/<os_architecture>`, etc. The initial 
indicates the python version (py2 vs py3) and then the version of the other 
dependencies, where `v1` is the minimal version required to run the SPT code
and ever increasing versions are newer versions of the dependencies. At the
moment, `v4` is the bleeding edge`. For each combination of python and 
dependency set version there will be a version delineated by OS version and 
CPU architecture.

## Dependency List

gcc
binutils
python
python-setuptools
python-pip
boost
hdf5
netcdf
fftw
gsl
gnuplot
pgplot
tcl
bzip
zlib
xz
cmake
flac
freetype
cfitsio
openblas
globus-toolkit
numpy
scipy 
ipython
jupyter
pyfits
astropy
numexpr
Cython
matplotlib
Sphinx
tables
urwid
pyFFTW
healpy
spectrum
tornado
SQLAlchemy
PyYAML
ephem
idlsave
ipdb
jsonschema
h5py
pandas
line_profiler
memory_profiler
simplejson
joblib
lmfit