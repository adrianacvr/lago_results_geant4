# Charge histogram of each site

## In this folder you will find: 

+ The .root files of eight sites.  
+ To convert the .root files to .dat files please follow the instructions below:
	- make clean
	- Edit the file main.cxx to select the maximum range (in this case "binForPhotons = 800") and the histogram you want to convert. 
		> For instance "histTest = (TH1F*)fileIn.Get("histCerenPhoElectAll")" to obtain the histogram of the number of pe of all particles.
	- make 
	- ./mainExe file.root > name.dat 
		> For example ./mainExe chacaltaya.root > ch_all.dat, gets the histogram of pe corresponding to all particles in Chacaltaya.
	- For each site you should obtain six data files, for instance:
		>- ch_all.dat
		>- ch_muon.dat
		>- ch_elec.dat
		>- ch_gamm.dat
		>- ch_neut.dat
		>- ch_hadr.dat

> For more information about the main code please contact mauromsd@gmail.com

+ The script for switching from photoelectrons to energy deposited:
	- Please execute the lines that you need from reconversion.sh and you will obtain the files, for instance Chacaltaya:
		>- eng_ch_all.dat
		>- eng_ch_muon.dat
		>- eng_ch_elec.dat
		>- eng_ch_gamm.dat
		>- eng_ch_neut.dat
		>- eng_ch_hadr.dat

+ The histogram.gp allows you to plot the energy deposited histogram of each site. 
	- Please check:
		>- The name of the output file (line 3)
		>- The title of the plot (line 13-20)
		>- The data of the site to be plotted (line 38-45) 

> For more information please contact adrianacvr67@gmail.com
