# O2AT6: PID from clusters to neural networks

A three-hour tutorial covering k-means, Gaussian mixtures, neural networks and ONNX inference.

## Run

Install the Python dependencies in your preferred environment:

```sh
pip install numpy pandas matplotlib scipy scikit-learn torch onnx onnxruntime uproot jupyterlab nbformat nbclient
jupyter lab gmm_neural_network_exercise.ipynb
```

Start Jupyter from this repository directory and run the notebook from top to bottom. CPU execution is supported. The final O2Physics benchmark requires a separately prepared O2 environment; the notebook explains the commands.

## Included data

`tutorial_tpcskimv0_git.root` is approximately 307 KiB and contains 20,000 selected real tracks in the `O2tpcskimv0tree` TTree. It preserves the six variables required by the notebook and the default **0.8 <= p < 1.0 GeV/c** momentum slice: 12,236 pions, 992 kaons and 6,772 protons.

This is the existing seed-42 uniform reservoir sample from `first_df_tpcskimv0.root`, after the notebook's quality and PID selections. It supports the default real-data training, architecture exercises and ONNX export. The introductory momentum-range exercise uses synthetic data. Changing the real-data momentum interval requires a larger input skim and updating `ROOT_PATH`.
