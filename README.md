# Evaluating Automated Seismic Event Detection Approaches: An Application to Victoria Land, East Antarctica
By Long Ho, Jacob Walter, Samantha Hansen, Jose Sánchez-Roldán, and Zhigang Peng  
This is a repository of the code used in Ho et al (2024, JGR in rev)
## Acknowledgements
  1. Seisbench source code is introduced here: [Woollam, J., Münchmeyer, J., Tilmann, F., Rietbrock, A., Lange, D., Bornstein, T., Diehl, T., Giunchi, C., Haslinger, F., Jozinović, D. and Michelini, A. (2022). SeisBench—A toolbox for machine learning in seismology. Seismological Research Letters, 93(3), 1695-1709.](https://github.com/seisbench/seisbench)
  2. The transfer-learned models were deployed on continuous data using easyQuake: [Walter, J. I., Ogwari, P., Thiel, A., Ferrer, F., & Woelfel, I. (2021). easyQuake: Putting machine learning to work for your regional seismic network or local earthquake study. Seismological Research Letters, 92(1), 555-563.](https://github.com/jakewalter/easyQuake/tree/master/easyQuake)
  3. NonLinLoc was used for event relocation: [Lomax A., Virieux J., Volant P., Berge-Thierry C. (2000) Probabilistic Earthquake Location in 3D and Layered Models. In: Thurber C.H., Rabinowitz N. (eds) Advances in Seismic Event Location. Modern Approaches in Geophysics, vol 18. Springer, Dordrecht.](https://github.com/alomax/NonLinLoc.git)
  4. Seismic data were obtained from here http://ds.iris.edu/mda/
### Installation
Clone this Github repository:  
`git clone https://github.com/longmho/Ho_etal_2024.git`
### Download the waveform data
The waveform data used in this study were obtained from the SAGE Data Management Center and have been made available on Zenodo (doi:10.5281/zenodo.12544109) as HDF5 files.  The three starting catalogs (MF, ML, and SL), which were used for transfer learning, are also available on the Zenodo site. These were generated with the [easyQuake](https://github.com/jakewalter/easyQuake.git) software package.  
Save the waveforms and their metadata to .seisbench/ folder located in your home directory.
### Preprocess the data
Split the data into training, testing, and validation sets can be found at:
```
/data/tam_mf.py  
/data/tam_ml.py
/data/tam_og.py
```
### Training, Evaluating, and Exporting Models
The Jupyter Notebook `train_evaluation_example.ipynb` provides examples of how to load, train, evaluate, and export the fine-tuned models.   
All of our generated fine-tuned models can be found in the Zenodo [repository](10.5281/zenodo.12544109).
### Using the Trained Models
Use [easyQuake](https://github.com/jakewalter/easyQuake/tree/master/easyQuake) to apply the fine-tuned models to the continuous waveform data. 
### Relocate the Seismic Events
Seismic events were relocated using NonLinLoc, whose software can be found [here](https://github.com/alomax/NonLinLoc). Our relocated event catalogs can be found in the Zenodo [repository](10.5281/zenodo.12544109).
