# Automobile Regression Challenge
## Content:

This **data set** consists of three types of entities:

(a) the specification of an auto in terms of various characteristics,

(b) its assigned insurance risk rating,

(c) its normalized losses in use as compared to other cars.

The second rating corresponds to the degree to which the auto is more risky than its price indicates. Cars are initially assigned a risk factor symbol associated with its price. Then, if it is more risky (or less), this symbol is adjusted by moving it up (or down) the scale. Actuarians call this process "symboling". A value of +3 indicates that the auto is risky, -3 that it is probably pretty safe.

The third factor is the relative average loss payment per insured vehicle year. This value is normalized for all autos within a particular size classification (two-door small, station wagons, sports/speciality, etc…), and represents the average loss per car per year.

**Note**: Several of the attributes in the database could be used as a "class" attribute.

### Problem statement:

Perform exploratory data analysis and select three key plots, explain your takeaways. Please note that there is no need to explain how you have generated your plots, only the inference and findings need to be explained.
Perform multiple correspondence analysis (MCA) on the dataset and briefly describe your findings.
Build a model for predicting the price of the automobile. Explain your choices on encoding, model selection etc.
Explain the high-level plan of action if the above model is to be used as the backend for a web application for B2B use at an automobile manufacturing firm. Please write in bullet points the steps needed and explain your technological choices.


## How to run
### Download dataset from Kaggle:
```shell
# MacOS/Linux
curl -o output.file.name.here 'https://www.kaggle.com/datasets/toramky/automobile-dataset/data'

# Windows 10 terminal
curl.exe --output output.file.name.here --url https://www.kaggle.com/datasets/toramky/automobile-dataset/data

# Windows 10 PowerShell
Invoke-WebRequest -OutFile output.file.name.here -Uri https://www.kaggle.com/datasets/toramky/automobile-dataset/data
```
### Google Colab
 - Uncomment the following code snippets in the notebook (_1st three cells from start_):
   - Configure Colab.
   - Mount the drive.
   - Install packages.
   - Set correct path to data set in ```DATA_PATH``` variable.
```python
# # Uncomment if running in Google Colab
# gpu_info = !nvidia-smi
# gpu_info = '\n'.join(gpu_info)
# if gpu_info.find('failed') >= 0:
#   print('Not connected to a GPU')
# else:
#   print(gpu_info)

# # Uncomment if running in Google Colab
# from google.colab import drive
# drive.mount('/content/drive', force_remount=True)

# # Uncomment if running in Google Colab
# !pip install bayesian-optimization
# !pip install mca
# !pip install prince
# !pip install scikit-learn
# !pip install scikit-optimize
# !pip install shap
# !pip install tabulate
```

### Local Environment
 - Create Virtual Env ([how to create virtual environment with python](https://docs.python.org/3/library/venv.html))
```shell
python -m venv /path/to/new/virtual/environment
```
 - Activate the virtual environment
```shell
# MacOS/Linux
source .venv/bin/activate

# Windows
.\venv\Scripts\activate
```
 - Install required packages using pip
```shell
pip install -r requirements.txt
```
 - Validate all packages are successfully installed
```shell
pip list
```
 - Start Jupiter Lab your preferred way and load the notebook ([Start Jupiter Lab](https://jupyterlab.readthedocs.io/en/stable/getting_started/starting.html))
```shell
# MacOS/Linux
jupyter lab --notebook-dir=/var/ --preferred-dir /var/www/html/example-app/

# Windows
jupyter lab --notebook-dir=E:/ --preferred-dir E:/Documents/Somewhere/Else
```
 - Set correct path to data set in ```DATA_PATH``` variable.

## Notes
- Results and insights are included into inline notebook's comments.
- Notebook contains some charts and tables. More can be found in ```./images``` folder.
- Dumping trained model - just set correct paths for the model and the metadata.
- Predictions can be made by feeding ```predict_price``` method with valid data, model path and model metadata path
  - model metadata is actually a list with all the features used to train the model
  - see notebook's last cell for working example 
- Local development can be done using **VSCode** or **PyCharm**. The latter may have some issues showing inline charts and visual elements. Also the latter requires subscripton to use **_Data Science_** tools.
- Ultimately the best way to do development in a productive way is by using **Google Colab**.
