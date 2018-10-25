# ImageJ/FIJI Z-Projection Script


This is a FIJI/ImageJ script that batch projects image stacks with optional .avi production.
IMB_Z Projection and AVI output.
Developed by Dr Nicholas Condon.

[ACRF:Cancer Biology Imaging Facility](https://imb.uq.edu.au/microscopy), 
Institute for Molecular Biosciences, The University of Queensland
Brisbane, Australia 2018.

This script is written in the ImageJ1 Macro Language.


Background
-----

This script is designed to project multiple dimension files.

This script can work on multiple files within a single directory and as long as the format is Bio-formats compatible,  it should run fine. (TIP: Go windowless for the format which you plan to use. See “Preventing Bio-formats Importer window.rtf” file to do this.)

The script can be run as a simple file converter by selecting “No Projection” and “Save .tif output” options. Note even if selected, no .avi will be created.

Running the script
-----
The first dialog box to appear explains the script, acknowledges the creator and the ACRF:Cancer Biology Imaging Facility.

The second dialog to open will warn the user to select the working directory of your files and to take note of the file extension that they wish to process.

The script then asks you to select the directory you wish to process.

The script will prompt you for the for the parameters you wish to include in your processing.

The projection type is selected by the “Run Z-Projection” drop down list of projections (Maximum, Minimum, Average or No Projection). Note: Use “No Projection” for running this macro as a batch file converter.

The file extension is actually a file ‘filter’ running the command ‘ends with’ which means for example .tif may be different from .txt in your folder only opening .tif files. Perhaps you wish to process files in a folder containing <Filename>.tif and <Filename>+deconvolved.tif you could enter in the box here deconvolved.tif to select only those files. It also uses this information to tidy up file names it creates (i.e. no example.tif.avi)

The script can reset the brightness and contrast of your images by moving to the middle slice of the first frame and running the reset command. It will do this for all channels.

The two output types are .avi and .tif Tick either of these options (or both) to create files of these type.

Running the script in batch mode won’t open the files into your OS, instead it runs in the background, which is faster and more memory efficient.

If you select to output .avi files the following pop-up will run. This is where you can select your compression type (Hint: Black and white images should be either None or PNG), and frame rate.

The final dialog box is an alert to the user that the batch is completed. 


Output files
-----
Files are put into a results directory called '<Projectiontype>_Results_<date&time>' within the chosen working directory. Files will be saved as either a .tif  .avi or .txt for the log file. Original filenames are kept and have tags appended to them based upon the chosen parameters.

A text file called log.txt is included which has the chosen parameters and date and time of the run.


￼
