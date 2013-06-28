=======
Installing MoogStokes the Easy Way™
=======

:Info: See the `GitHub repository <http://www.github.com/Acetylene5/moog>`_ for the latest source
:Author: Casey Deen, Max Planck Insitute for Astronomy (deen@mpia.de)
:Original Author: Andy Casey, Australian National University (andy@the.astrowizici.st)
:Website: `astrowizici.st <http://astrowizici.st>`_
:License: Distribute to anyone you see fit, as long as you adhere to the licenses set by the dependencies (`SuperMongo <http://www.astro.princeton.edu/~rhl/sm/>`_, `MOOG <http://www.as.utexas.edu/~chris/moog.html>`_, etc). Improvements are welcome!


Background
----------
`MOOG <http://www.as.utexas.edu/~chris/moog.html>`_ was written by `Chris
Sneden <mailto:chris@verdi.as.utexas.edu>`_ and has -- and continues to be
-- an
invaluable contribution to modern stellar astrophysics. From the `MOOG <http://www.as.utexas.edu/~chris/moog.html>`_ website:

*MOOG is a code that performs a variety of LTE line analysis and spectrum
synthesis tasks. The typical use of MOOG is to assist in the determination
of the chemical composition of a star.*

MoogStokes is an extension of the original Moog code which includes the 
effects of magnetic fields via the Zeeman effect.  MoogStokes allows the 
user to model emergent spectra of stars with strong magnetic fields.

The current `MoogStokes <http://www.github.com/Acetylene5/MoogStokes/>`_ version
hosted by this repository is the June 2013 version (version 1.00).


Installation
------------
Classically, MOOG has been difficult to install. Or at least, it has been
for me because I'm bad at computers. Now it's easy-ier!

**1)** If you are on a Mac then you will need to ensure you have `Xcode
<https://developer.apple.com/xcode/>`_ installed
as well as the `Command Line Tools
<http://stackoverflow.com/a/9329325/424731>`_ first. Regardless of your
operating system, you will need either `gfortran
<http://gcc.gnu.org/wiki/GFortran>`_ (recommended) or `g77
<http://hpc.sourceforge.net/>`_ to compile MOOG.

**2)** `Download this repository
<https://github.com/Acetylene5/moog/archive/master.zip>`_, extract the files and type:

``python setup.py install --prefix=/desired/path/to/MoogStokes/executable/``

The installer will compile ``MoogStokes`` and ``MoogStokessilent`` and place
them in defined in ``--prefix``.  If necessary, it will also install the
required AquaTerm framework to ``/Library/Frameworks/AquaTerm.framework/``, 
and create a ``~/.moog`` directory to contain data files.

**3)** the ATLAS and LAPACK libraries included in the /lib directory may not be
correctly tuned for your system.  If this is the case, please download and 
install the libraries on your system, and copy the .a libraries into the /lib 
directory (overwriting the ones included in the tarball)

Uninstall
---------
Just type the following files to uninstall MOOG:

``sudo pip uninstall moog``

And to clean up completely:

``sudo rm -Rf ~/.moog /Library/Frameworks/AquaTerm.framework/``

