Large Scale PSG Analysis Student Projects
=========================================
The motivation for the projects described below is to help make analyzing thousands of sleep studies common place. The projects are targeted at interdisciplinary types, engineers and computer scientists. All of the projects require programming. The projects could be developed in many different language. 

Are you a biology major and want to strengthen your programming skills, well there will be projects for you too. I suggest you start with a tutorial for your language of choice.  Python and JAVA are the most popular languages. MATLAB is my language of choice. There may be a slight bias for the selection of examples that include MATLAB source code.


Do you have a project you want to post? Send me and email and I will post it here. 

Did you complete one of the projects? Email me so that we can post a link to your solution.


#### Data Access Projects

1. **Porting low level signal file loaders**. Data access projects in early programming projects involve using low level command to load text files. Engineers are often provided loader for there projects.  I have developed a set of loaders for sleep file written in European Data Format in MATLAB that would be nice to have ported to Python, JAVA and Octave.  The two loaders are [BlockEdfLoad](https://github.com/DennisDean/BlockEdfLoad/blob/master/README.md) and [BlockEdfLoadClass](https://github.com/DennisDean/BlockEdfLoadClass/blob/master/README.md). Porting the loaders would provide and oportuniting to think about efficient loading of large data sets. My loaders are relatively effienct and use many modern MATLAB features. You will have to work through the MATLB syntax and find parallels in a second language. What fun! 

2. **More Efficent Load**. The loaders mentioned above, load all the data and only pass back the data (signals and sleep epochs). I suspect that refining the loader to only load what is needed in an efficent way could reduce load times in practice. Look at the signal load area in [BlockEdfLoad](https://github.com/DennisDean/BlockEdfLoad/blob/master/README.md) or [BlockEdfLoadClass](https://github.com/DennisDean/BlockEdfLoadClass/blob/master/README.md). The task is to infer the most efficent data loading strategy based on the user request. Most sleep files have between ten and twenty signals.  However, most analyses would require only a single signal.

3. **Low Level XML parser**.  Sleep annotation files are written in XML. We are currently reading the XML file from within MATLAB with a JAVA interface provide by MATLAB.  A low level parser that allowed the schema to be inferred would allow us to load and check according to a schema.  There are several types of sleep annotation files written in XML.  A generic schema based loader could be configured to load different file types.  An example of our XML loader and file examples can be found [here](https://github.com/DennisDean/LoadCompumedicsAnnotationsClass). This project is suited for a person who has taken or wants to take acompiler design course.  The project motivation is to be able to load/process files written over 20 years that have known issues.  A smarted loader would allow for more robust tools to be developed.

#### Signal Generation and Analysis

4. **Sleep EEG Spectral Simulations**. There are characteristic spectra during [NREM](http://en.wikipedia.org/wiki/Non-rapid_eye_movement_sleep) and [REM](http://en.wikipedia.org/wiki/Rapid_eye_movement_sleep) sleep. Moreover, these spectra change during the life course.  As we developed automated analysis tools, it would be nice to have the ability to generated simulated signals for which to perform simulation studies. What would be nice to have would be a spectral editor that would allow a domain expert to interactively edit/save/simulate chaaracteristic spectra.  There spectra could then be used to simulate NREM-REM patterns over the night. I found a nice project that allows you to edit in the [time domain](http://www.mathworks.com/matlabcentral/fileexchange/23526-waveform-generator-gui).  The project would have to inverted so that editing was done in the frequency domain and simulations were done in the time domain. This project would require some learning to be done about sleep and sleep stages inorder for the tool to be accepted by domain experts. This project goes beyond the cursory fft of a square wave done in many quantiative classes. Just to add a little fun, it would be nice for the generating function to create sleep files (EDF format), to use sleep annotation files to generate random instances and to upload spectral results so that simulations of individuals could be formed. The project as described would require traversing low level read/write, signal processing functionality and GUI devleopment. Nice way to strengthed and add new skills. 

5. **Large Scale Spectral and Coherence Analysis**. I wrote an effient spectral analysis and coherence program.  But I can't sleep at night because I am not using all the cores on my 6 core machine.  I am sure there must be ways to improve the running time, especially the coherence analysis. The datasets we work with are in the order of hundreds of Gigabyte. The uploaded [spectral analysis program](https://github.com/DennisDean/SpectralTrainFig/blob/master/README.md) includes examples. Are there strategies for processing the data on desktop that enable more efficent processing?

#### Cognitive Assessment

6. **Two Dimensional MAZE test**.  One of the [most interesting studies](http://onlinelibrary.wiley.com/doi/10.1111/j.1365-2869.2005.00484.x/full) I have read involved giving maze test to people who are sleep deprived.  The study was done with paper mazes. Why not do the same thing on a PC or tablet. It stuck me as rediculously fun to write software to interactively generate and test maze performance. Beyond the fun to be had, generating random mazes with the same properties would be fun. I found sites with information on how to generate [random mazes](http://www.mathworks.com/matlabcentral/fileexchange/6705-maze) and there are tools for [generating cognitive tests](https://psychtoolbox.org/HomePage). The two would just have to be put together.  This is the type of projectd that could be paired up with people across disciplines.  Most researachers won't use a tool with out validation.  Generate some study results for extra credits. Writing a MAZE program was one of my first projects.  You would learn about data stuctures, algrithmns and random generation. Developing a cognitive test would required you to think about system response time and recording of ingormation.
