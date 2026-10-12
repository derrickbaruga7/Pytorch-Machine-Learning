# Sales prediction with PyTorch

A notebook experiment using a feed-forward neural network to predict the `Sales` column from purchase-history features. It includes exploratory plots, an 80/20 train/test split, feature scaling fitted on the training set, and test mean squared error.

The implementation is in [model 2.ipynb](model%202.ipynb). It uses PyTorch; no LSTM, TensorFlow pipeline, web API, Docker deployment, or production serving system is included.

## Setup

Use Python 3.10 or newer from the repository root:

```bash
git clone https://github.com/derrickbaruga7/Pytorch-Machine-Learning.git
cd Pytorch-Machine-Learning
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab "model 2.ipynb"
```

On Windows, activate with `.venv\Scripts\activate` instead. The default PyTorch installation is sufficient for the notebook's CPU workflow.

## Input data

The sales CSV is **not included**. Place an authorized copy at `data/Sales Data.csv`, or set `SALES_DATA_PATH` to its location before starting Jupyter. Local data is ignored by Git.

The original workflow references `Product Category`, `Product`, `Quantity Ordered`, `Month`, `Sales`, `City`, `Time of Day`, `Order Date`, `Order ID`, and `Purchase Address`. An exported `Unnamed: 0` index column is optional. Dates use `%d-%m-%Y %H:%M`. Other retained feature columns must be numeric after encoding.

## Model and interpretation

The network has hidden layers of 128 and 64 units, ReLU activations, Adam optimization, and MSE loss. The notebook trains for 200 epochs with a batch size of 64. NumPy and PyTorch seeds are set for repeatability; results can still vary across library versions and hardware.

This is a row-level regression exercise, not a validated future-sales forecast. Review predictors such as quantity and unit price for target leakage before interpreting model performance. Time-based validation and comparison with a simple baseline are useful next steps. Saved outputs are cleared to avoid distributing row-level purchase data. Re-run the notebook with an authorized source CSV to generate results.
