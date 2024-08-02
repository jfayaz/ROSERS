## RAPID ON-SITE ESTIMATION OF RESPONSE SPECTRUM (ROSERS)

This tool, named as Rapid On-Site Estimation of Response Spectrum (ROSERS), uses a variational autoencoder (VAE) and deep neural network (DNN) framework to estimate a cross-dependent vector of component spectral acceleration (S_a) at 96 periods. The inputs to the framework include two site characteristics (soil shear-wave velocity V_s30; basin depth Z_2.5) and seven intensity measures (Arias intensity I_a; cumulative absolute velocity CAV; peak ground acceleration PGA; peak ground velocity PGV; peak ground displacement PGD; mean period T_m; significant duration D_(5-95)) computed from first three seconds of arriving ground motion waveform component. Hence, given the site characteristics and intensity measures, this tool returns a median prediction of the S_a at 96 periods. The executable is developed by Jawad Fayaz (https://jfayaz.github.io/layouts/codeandsoft.html/). For further details please read the article mentioned in the “Reference”.

Download the application from the following Dropbox link
      
      https://www.dropbox.com/scl/fo/qgkufohuyszhazrdva5c3/AEW_YbL031YW9S_TVAOZiOQ?rlkey=2b0r3xgghj64acfz5g124o2w0&dl=0


  1. ROSERS Input File

      The tool requires an input csv file that must be provided in the directory of the tool as shown in Figure 1 (see Manual) (user can provide any name for the csv file). The file must contain the two site characteristics (soil shear-wave velocity V_s30 (in m/s); basin depth Z_2.5 (in m)) and seven intensity measures (Arias intensity I_a (in m/s); cumulative absolute velocity CAV (in m/s); peak ground acceleration PGA (in g); peak ground velocity PGV (in m/s); peak ground displacement PGD (in m); mean period T_m (in sec); significant duration D_(5-95)(in sec)) in the same format as shown in Figure 2 (see Manual) (to avoid any errors please use the example ‘Inputs.csv’ file). The users can provide any number of inputs by adding rows to the csv file in the same format
 
  2.	Calling ROSERS 
  
        The tool package consists of the executable application “ROSERS.exe” which can be easily called from any command line or programming language/software. An example to run the ROSERS program is given in Figure 3 (see Manual) which shows calling of the input csv file. The generalized syntax to run the executable is as follows:
ROSERS.exe  InputFileName
 
         In case all the inputs are not properly provided the tool will throw an error as shown in Figure 4 (see Manual).
 
  3.	ROSERS Outputs

        The tool creates an “Outputs” folder in the current directory where results for all inputs are saved. The output screen of the framework is shown in Figure 5 (see Manual).
 
        The outputs consist of three files for each input row: 1) “LatentVariables_i.jpg” file showing the latent variable deduced for the input compared to the latent variables of the utilized database (shown in Figure 6 (see Manual)), 2) “ReconSpectrum_i.jpg” file showing the reconstructed median S_a spectrum (shown in Figure 7 (see Manual)), and 3) “ReconSpectrum_i.out” file containing estimated values of  log⁡(S_a (T)) in units of g corresponding to the 96 periods (shown in Figure 8 (see Manual)). The outputs are developed for ith row provided in the input file. 
 

    Reference
    Jawad Fayaz and Carmine Galasso (2023). "A Deep Neural Network Framework for Real-Time On-Site Estimation of Acceleration Response Spectra of Seismic Ground Motions". Computer-Aided Civil And Infrastructure Engineering, 1-17. https://doi.org/10.1111/mice.12830
