# Evaluating Automated Seismic Event Detection Approaches: An Application to Victoria Land, East Antarctica
By Long Ho, Jacob Walter, Samantha Hansen, Jose Sánchez-Roldán, and Zhigang Peng  
This is a repository of the code used in Ho et al (2024, JGR in rev)
## Acknowledgements
  1. Seisbench source code is introduced here: [Woollam, J., Münchmeyer, J., Tilmann, F., Rietbrock, A., Lange, D., Bornstein, T., Diehl, T., Giunchi, C., Haslinger, F., Jozinović, D. and Michelini, A. (2022). SeisBench—A toolbox for machine learning in seismology. Seismological Research Letters, 93(3), 1695-1709.](https://github.com/seisbench/seisbench)
  2. The transfer-learned models were deployed on continuous data using easyQuake: [Walter, J. I., Ogwari, P., Thiel, A., Ferrer, F., & Woelfel, I. (2021). easyQuake: Putting machine learning to work for your regional seismic network or local earthquake study. Seismological Research Letters, 92(1), 555-563.](https://github.com/jakewalter/easyQuake/tree/master/easyQuake)
  3. Seismic data were obtained from here http://ds.iris.edu/mda/
### Installation
Clone this Github repository:  
`git clone https://github.com/longmho/Ho_etal_2024.git`
### Download the waveform data
The three catalogs ((MF, ML, IN) used for transfer learning in this study were generated through the easyQuake software (https://github.com/jakewalter/easyQuake.git).  Those three catalogs, along with their waveform data and their associated metadata can be downloaded at:
doi:10.5281/zenodo.12544109  
Save the waveforms and their metadata to .seisbench/ folder located in your home directory.
### Preprocess the data
Split the data into training, testing, and validation sets can be found at:
```
/data/tam_mf.py  
/data/tam_ml.py
/data/tam_og.py
```
### Training, Evaluating, and Exporting Models
Jupyter notebook showing examples on how to load, train, evaluate, and export models:  
`train_evaluation_example.ipynb`  
All the fine-tuned models can be found in this [repository](10.5281/zenodo.12544109).
### Using the Trained Models
Use [easyQuake](https://github.com/jakewalter/easyQuake/tree/master/easyQuake) to apply the models to continuous data. 
### Relocate the Seismic Events
Relocate the seismic events using NonLinLoc. NonLinLoc software can be found at [NonLinLoc](https://github.com/alomax/NonLinLoc). The relocated catalogs can be found [here](10.5281/zenodo.12544109).
