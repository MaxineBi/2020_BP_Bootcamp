# 2020_BP_Bootcamp
Author: Christina Stephens	EST: 20200822 UPD: 20200822

Purpose: This is meant as a general reveiw for python basics including some of
the most common datatypes and Python packages as well as an introduction to
jupyter notebook.

N.B. If you do not already have anaconda installed on your computer you might
     find it useful to have and know how to use it so you can set up specific
     environements that have specific python packages or versions of software that
     may otherwise be incompatible.  More detailed instructions can be found
     here: link to Adam's instructions

     You do, however, need to have IPython installed wherever you plan to run
     jupyter notebook.  The easiest way to do that is to type 'conda install
     anaconda' in your terminal if you have anaconda installed. 

It is not necessary to run python code through jupyter notebook (it's sort of an
IDE or integrated development environment), but you may find it useful while
building up your scripts, debugging, and visualizing your data. Jupyter
notebook does have a function to convert cells in your notebook to a standard
python script (but you should always check it for mistakes).


(1) Opening Jupyter Notebook and creating a new file Jupyter Notebook is not
    limited to python, but you can customize your notebook to create scripts in
    other languages or kernels including R, Julia, Matlab, Java, and more. 

    To open jupyter notebook simply type 'jupyter notebook' into the
    command line of your terminal This should automatically launch a jupyter
    notebook on a local port that can be accessed from any browser (I'm using
    google chrome). If your computer did not automatically open up a new browser
    window, highlight the URL and right click to 'Open URL'.

   (Optional) Running Jupyter Notebook from a remote computer: You may also find
	      it useful (especially during Covid-times or when you wish to work remotely) to
              access your work station's compute power while still being to work on code usign
              jupyter notebook. 

	   (a) ssh to the remote computer, we are going to use wynton for this
    	       example, type the following into the command line:
			> ssh studentname@log1.wynton.ucsf.edu
    	       (!) Make sure you have connected to the UCSF VPN via Pulse Secure

	   (b) On the remote computer, launch jupyter notebook with the command: 
			> jupyter notebook --no-browser --port 8080 
    	       This will run a notebook on a specific port and without opening a browser. I recommend using
               your own 4-digit value.

	   (c) Now you need to forward that port so that you can access the notebook remotely.
    	       On your local machine, type:
			> ssh -fNT -L 8080:localhost:8080 studentname@log1.wynton.ucsf.edu

	   (d) The notebook can be now accessed on a browser in your local machine at the
    	       URL obtained in step (b)

	   If your connection drops, sometimes you need to close the port you just opened, by typing:
			> kill $(lsof -i:8080 | grep LISTEN | awk '{print $2}')
	   (!) Remember to replace 8080 with your port number. This kills a process so make sure it's correct

	   To avoid having to retype everything each time, you can save the above
	   commands as aliases in your ~/.bash_aliases file (remote or local)

   In your jupyter notebook session you should see all the files and folders located in the 
   directory where you initiate the session. 

   To create a new python script go to the 'new' button in the top right-hand corner and select a language (for this
   tutorial choose Python 3). This should open up a new jupyter notebook file.
   (!) As Python 2 is no longer maintained by its developers its not usually recommended over Python 3.


(2) Python Basics - see the notebook for this, just click on it in jupyter notebook list of items


 
