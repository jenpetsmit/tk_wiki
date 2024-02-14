# How To Use the Command Line Terminal - PC or Mac

Notes: 

In this context the word _directory_ is the technical term for a computer folder.

The working directory (also called current working directory or present working directory (PWD)) is the folder that you are currently in. The bin directory is where binaries (think of them as mini computer programs) are stored. To run a binary prograsm, you have to be in the bin directory or tell the operating system where the bin directory is.

The direction of slashes varies with operating systems.

To get started: 

1. Open command line terminal 

    * PC 	Click **Start** and search for _Command Line_  

    * Mac 	From the Dock, click **Launchpad** icon, and in the search field type _Terminal_

 2. To see a list of files and directories 

    * PC 		Type the following: 

`dir` 

    * Mac 	Type the following: 

 `ls -a` 

The structure of folders is a vertical hierarchy.  

3. To _change_ to a lower _directory_ _one level down_, type
   `cd <name of directory>`

4. To change to a higher directory on level higher, type
   `cd ..

6. To change directories to a level that is more than one level up or down, type
   `cd <path/to/directory>`

   # Toolkit Tools
1. To run Toolkit tools (also called _commands_ or _utilities_), first **change directories to the bin folder** in the SRA Toolkit you downloaded

   `cd <path\to\bin`
2. For PC users, run all Toolkit commands from bin directory. See screenshot for an example with Prefetch tool.

3. For some Toolkit tools, you need to **provide the path** to the location of the data

4. For Mac and Linux users, run all Toolkit commands from any location after setting the PATH Variable 

In the following command, replace PWD with your path to bin directory: 

`export PATH=$PATH:$PWD`

5. To stop a long running executuion,
     * control + z 
    * contorl + c
6.  To exit,  type **EXIt** close the terminal window.
   
