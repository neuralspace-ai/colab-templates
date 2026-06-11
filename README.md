# NeuralSpace Colab Templates

Public, secret-free Google Colab notebook templates for NeuralSpace.

## Bootstrap notebook

Open `notebooks/bootstrap.ipynb` through the pinned URL returned by NeuralSpace.
Generate a one-time claim code in the NeuralSpace workspace page, then paste it
into the notebook when prompted.

The notebook never reads credentials or private identifiers from its URL.

## Logging notebook

Open `notebooks/logging.ipynb` when you want to send Colab metrics and runtime
logs back to NeuralSpace. Generate a one-time claim code in the NeuralSpace
workspace page, run each cell in order, then call `logger.log_metrics(...)` and
`logger.log(...)` from your training loop.
