# Submit Gaussian16 jobs for Yale's Chem 426/526

## Install

In your home directory (if you aren't sure, just type `cd`), type 

`git clone https://github.com/jjgoings/YaleCompChem.git`
`cd YaleCompChem`
`python setup.py install`
`cd` (to get back to your `HOME` directory)

This should install the submitter `gausub`.

## Usage

Given a Gaussian job (we'll call it `myjob.com`):

`gausub myjob.com`

This will prepare a submission script for you and send it to the queue to run.

If you want to inspect the submission script, it will have the same name as your input, but with a `.sh` extension (e.g. `myjob.sh`)

## Options and help

Type `gausub --help` for a list of command-line options. You can change the time given to the job and number of CPUs here. 

(Note that if you want to use more CPUs, you must *also* change the input file to request a greater number of CPUs. In the Gaussian `.com` or `.gjf` file, you must edit `%NprocShared=<num CPUs>`.)


