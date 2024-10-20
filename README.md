# RF_cristae_in_mitos
## Random Forest Classifier to segment cristae within mitochondria masks in EM images

The classifier uses features extracted via the Local Binary Patterns (LBP) texture descriptor and the Sobel edge detector.

Data source kindly provided by [Ryan Conrad](https://github.com/conradry), one of the MitoNet and napari-empanada developers: [mouse liver FIBSEM](https://www.dropbox.com/s/za9q1h2yancx1ow/openorganelle_mouse_liver_roi.tif?dl=0)

1. Create and activate a new virtual environment using conda:
```bash
  conda create -n cristae_ml python=3.10 -y
  conda activate cristae_ml
```
2. Install the required libraries:
```bash
  pip install scikit-learn scikit-image opencv-python matplotlib jupyterlab joblib
```
3. Run the `detect_cristae.ipynb` notebook to train the Random Forest classifier and perform prediction.
4. The trained classifier can be saved and loaded via the `joblib` library as follows:
```bash
  joblib.dump(clf, 'rf_classifier.pkl') 
  clf = joblib.load('rf_classifier.pkl')
```

