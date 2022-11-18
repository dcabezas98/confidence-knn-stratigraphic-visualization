# confidence-knn-stratigraphic-visualization
## Measuring the Confidence of the k-Nearest Neighbors Algorithm developed in Python for Visualizing the 3D Stratigraphic Architecture of the Llobregat River Delta in NE Spain

In a previous paper (https://www.mdpi.com/2077-1312/10/7/986, https://github.com/dcabezas98/knn-stratigraphic-visualization), a machine learning k-nearest neighbors (KNN) algorithm and Python libraries were used to create two interactive 3D HTLM models for visualizing the 3D stratigraphic architecture of sedimentary porous media in the Quaternary onshore Llobregat River Delta (LRD) in northeastern Spain. The first model showed the consecutive 5-m-equispaced set of horizontal sections of the granulometry classes created with the KNN algorithm from 0 to 120 m b.s.l., and the second model showed the 3D mapping of the main Quaternary gravel and coarse sand sedimentary bodies (lithosomes) and the basement (Pliocene and older rocks) top surface created with Python libraries. The main limitation was the absence of routines to quantify the confidence of these HTML models. This paper is aimed at computing the confidence of these HTML models, which is crucial for quantitative geological evaluations. A variant of the Similarity Ratio that uses weight instead of similarity was implemented to quantify the confidence of KNN predictions. The rationale was the equivalence between similarity and assigning weights inversely proportional to the distance of each granulometry class. While the KNN algorithm and Python libraries have proven its suitability for visualizing the 3D stratigraphic structure of sedimentary porous media, the KNN prediction confidence quantified the reliability of KNN predictions. At a given prospecting depth, confidence is a function of data density at that 2D data field. At a 3D data field, confidence also reflects the typical decreasing data density with prospecting depth. Average-weighted confidence was in the 0.44–0.53 and 0.42–0.55 ranges for prospecting depths in the 12.7–72.4 m b.s.l. and 4.6–83.9 m b.s.l. ranges for gravel and coarse sand lithosomes, respectively. Spurious average-weighted confidences of 0.29 in one gravel lithosomes and 0.30 in one coarse sand lithosomes were due to the quite different weights of neighbors from different classes. The KNN algorithm confidence has proven ability to identify these disparities in the supposedly well-depurated granulometry database. Visualization of the 3D stratigraphic architecture and confidence of the mapped lithosomes are needed for interpretations in order to take decisions in different environmental and economic geology disciplines.

## How to use

### Download the code

The code can be found in the repository, it can be downloaded as ZIP by clicking in the geen Code button. The only necessary file is the notebook `confidence.ipynb`.

### Download the data

The data can be found in the `data` folder. Only two files are necessary: `deltacontourn.csv`, that contains the points of the contour of the Delta; and `hsd new basements.xls`, that contains the data from the wells.

### How to run the notebook

You can run the notebook in [Jupyter-Notebook](https://jupyter.org/) or [Visual Studio Code](https://code.visualstudio.com/), you also need a Python kernel installed in your computer. We recommend installing [Anaconda](https://www.anaconda.com/) and launching Jupyter by typing `jupyter-notebook` in the Anaconda Prompt.

To successfully run the notebook, you need to locate it in the same folder as the `data` directory. In order to do this, you may just extract the ZIP file with the whole repository. Then, launch Jupyter Notebook and select the notebook `confidence.ipynb`. To run a cell, you can just click in the run button (next to the cell number) or click on it and press Ctrl+Enter. You're now ready to go!

#### Authors:

Manuel Bullejos, David Cabezas, Manuel Martín-Martín and Francisco Javier Alcalá
