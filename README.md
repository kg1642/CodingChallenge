# Coding Challenge

# Task 1

You are provided with a real, though quite simple, experiment code ( so called TRST for Triangle Rotated Stimulus Test ).  

1.	Open main.m, run it and go through all the trials. How much points you were able to earn? How easy/difficult it was earning points? 
2.	What are your observations about the program? Was it easier to interact with? What can you improve with the code?
3.	Introduce your improvements. For example, if you run the program on two screens you might find the central triangle difficult to rotate. Why is it so? What can you do to improve it?
4.	The user results file and log file overwrites each time you run the main.m (for given date). Please modify the code to prevent overwriting of data files.
5.	Each time the code generates a new taskmap for any subject except for subject # 0. However, if the taskmap for given subject already exists it does not allow to proceed with this subject within the same session throwing the following error:

`
Error using initSubjectInfo (line 57)
ERROR! Result data file already exists! Choose a different subject/session number.
`

 6. What can you do to allow to run the subject multiple times for one session? The experimenter must receive a warning if the subject id has been already used.

7. The probe triangle orientation is selected randomly. However, in several cases it overlays the stimulus triangle and the subject has nothing to do but just to submit the response without rotating the triangle. Modify the code to ensure the difference btw stimulus and presented probe triangle orientations no less then 30 degrees. 
8.	Currently the task consists of 10 trials. However, if the number of trials increases we need to let the subject to rest after some number of trials completed. Please introduce this functionality into program. You can split program by block, say 2 blocks with 5 trials each and ask the experimenter to type the number of block he wants to run (1 or 2). If the block has been already run, the warning pops-up asking the experimenter to confirm his/her intention to re-run the block again. Save results of consecutive runs of the same block into separate files to avoid overwriting. Make the number of blocks modifiable, but each time ensure there is equal number of trials in each block.
9.	In terms of interactivity, is it correct to ask the subject to press a space bar to start or to finish the experiment while still using mouse for responding? Write two versions of code – for responding with mouse only and with space-bar only.
10.	Modify the code to allow the experimenter to exit program any time when ‘Q’ key is pressed. In this case data for previous trials must be saved.
11.	For some MEG and fMRI experiments we use a buttonbox to submit the responses (buttons 1-4) and a dial for rotations (assume ‘t’ key – rotates clockwise, ‘b’ –key counterclockwise). Modify the code to allow subject to select and submit the responses using buttonbox and dial. Assume we are performing fMRI task. Allow the experimenter to initialize the scanner by pressing ‘5’ key (in some modifications it is ‘~’ key, please also take it into account). Please make a separate screen informing the subject that scanner initialization is in process.

## Task 2
There are different ways to measure the working memory capacity. The widely accepted one is closely related to the notion of “set size” – the number of items stored in the working memory.  Currently our code asks to remember only one stimulus.
1.	Modify the code to remember 5 (n, in general) differently-oriented stimuli, placed in randomly selected 5 main orientations (say, we have selected following 5 out of 12 main orientations [30, 90, 150, 270, 340]. The triangles must be placed in these orientations plus some jitter between [-10,10]  degrees. Please ensure the triangles are not overlapping) 
![alt text](https://github.com/vbabushkin/CodingChallenge/blob/master/img1.png)
