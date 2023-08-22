## Contents
* [Live Demo on Streamlit](#live-demo-on-streamlit)
* [Tables and Figures](#tables-and-figures)
* [Code Details](#code-details)
* [Data Details](#data-details)

## Live Demo on Streamlit

### [Go to the Demo!](https://brick-kilns-detector.streamlit.app/)

### Screenshots

<img width="1257" alt="Screenshot 2023-08-22 at 12 01 27 PM" src="https://github.com/ouranonymoussubmission/brick-kiln/assets/72247818/89cbb362-e370-4bbf-9585-e8233dce88c6">


<img width="1256" alt="Screenshot 2023-08-22 at 12 03 56 PM" src="https://github.com/ouranonymoussubmission/brick-kiln/assets/72247818/95f05e90-8def-46a2-b33d-84138b26641d">

### Instructions
You can see the brick-kiln detection in action via [this demo](https://brick-kilns-detector.streamlit.app/). All you need is an API key from Google Compute Platform (GCP). You may refer to [this tutorial](https://cloud.google.com/docs/authentication/api-keys#create) on "how to create a GCP API key?" 

## Tables and Figures

### Tables
| Table | Link |
| ------------- | ----- |
| Table 1 | [compare_augmented_models.ipynb](compare_augmented_models.ipynb) |
| Table 2 | [compare_augmented_models.ipynb](compare_augmented_models.ipynb) |
| Table 3 | [compare_models_fine_tune_india.ipynb](compare_models_fine_tune_india.ipynb) |
| Table A | [compare_models.ipynb](compare_models.ipynb) & [compare_augmented_models.ipynb](compare_augmented_models.ipynb) |
| Table B | [compare_models.ipynb](compare_models.ipynb) & [compare_augmented_models.ipynb](compare_augmented_models.ipynb) |

### Figures
| Figure | Link |
| ------------- | ----- |
| Figure 1 | Not Applicable |
| Figure 2 | [Brick Kilns in Delhi-NCR](figure2.ipynb) |
| Figure 3 | [Active Learning for Delhi-NCR Dataset](active_learning/plots.ipynb) |
| Figure 4 | [Model GradCAM](model_gradcam.ipynb) |
| Figure 5 | [Brick Kilns Identified by Model](figure5.ipynb) |
| Figure 6 | [Year-wise Gain](year_wise_gain.ipynb) |
| Figure A, B, C (Appendix) | [Active Learning](active_learning/plots.ipynb) |

## Code Details

We have organized our code into several notebooks and scripts:

1. `compare_models.ipynb`: This notebook showcases a model trained on the Bangladesh training dataset and evaluated on both the Bangladesh and Indian test datasets.
2. `compare_augmented_models.ipynb`: Explore this notebook to see results from a model trained on an augmented Bangladesh training dataset and tested on both the Bangladesh and Indian test datasets. It generates `Table 1` and `Table 2`.
3. `compare_models_fine_tune_india.ipynb`: Check out this notebook to examine a model fine-tuned on the Indian training dataset and tested on the Indian test dataset. It generates `Table 3`.
4. `model_gradcam.ipynb`: In this notebook, we've generated GradCAM heatmaps for images misclassified by our model. `Figure 4` is created using this notebook.
Appendices `Table A` and `Table B` can be generated from `compare_models.ipynb` and `compare_augmented_models.ipynb`, respectively.
5. `utils.py`: This file holds essential functions and model definitions.

## Data Details

To execute our scripts, follow these steps in your terminal:

```bash
python <python_file_name> <csv_file_name> <output_folder_name>
```

For example, to download images of model-identified kilns, use the following command:

```bash
python data.py model_identified_kilns.csv identified_kilns
```

Here's the list of provided CSV files and scripts:

| Script | Description |
| ---------------------- | ----------- |
| data_download.py       | [Script to generate 80,000 images using 188 manually identified kilns](data_download.py) |
| data.py                | [Script to download satellite images](data.py) |


| CSV file            | Description |
| ---------------------- | ----------- |
| Indo_gangetic_dataset.csv | [CSV for generating the 80,000 Indo-gangetic region dataset](Indo_gangetic_dataset.csv) |
| manually_identified_kilns.csv | [Manually identified brick kilns](manually_identified_kilns.csv) |
| model_identified_kilns.csv | [Model identified brick kilns](model_identified_kilns.csv) |

---
