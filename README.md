# LSTM-Based Remaining Useful Life(RUL) Prediction

This repository contains the implementation of a predictive maintenance model that estimates the Remaining Useful Life (RUL) of turbofan engines using Long Short-Term Memory (LSTM) networks. The model is trained and evaluated on the NASA C-MAPSS FD001 dataset.

## Dataset

We use the **NASA C-MAPSS FD001** subset, which includes:

- 100 training trajectories
- 100 test trajectories
- 21 sensor measurements
- 3 operational settings
- Single fault mode: HPC Degradation
- Single operating condition: Sea Level

Dataset source: [NASA Prognostics Data Repository](https://ti.arc.nasa.gov/tech/dash/groups/pooe/prognostic-data-repository/)


### Model Architecture
- **Three-layer LSTM network**:
  - First LSTM layer for pattern learning
  - Second LSTM layer (32 units) for deeper feature extraction
  - Dense layers for final RUL regression output
- Dropout (20%) for regularization
- Loss function: **Mean Squared Error (MSE)**
- Optimizer: Adam


## Results

The model achieved:

- **RMSE on test set**: ~44.29 cycles
- Training loss decreased consistently
- Validation loss plateaued early, indicating some overfitting

