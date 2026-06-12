# NeuralSpace Colab Templates

Public, secret-free Google Colab notebook templates for NeuralSpace.

## Bootstrap notebook

Open `notebooks/bootstrap.ipynb` through the pinned URL returned by NeuralSpace,
or use the stable Colab template link:
https://colab.research.google.com/github/neuralspace-ai/colab-templates/blob/main/notebooks/bootstrap.ipynb

GitHub repository:
https://github.com/neuralspace-ai/colab-templates.git

Notebook source:
https://github.com/neuralspace-ai/colab-templates/blob/main/notebooks/bootstrap.ipynb

Generate a one-time claim code in the NeuralSpace workspace page, then paste it
into the notebook when prompted.

Set the `API_BASE_URL` field in the bootstrap cell to the current public
NeuralSpace API URL, for example
`https://<your-tunnel>.trycloudflare.com/api/v1`. Bare tunnel roots such as
`https://<your-tunnel>.trycloudflare.com` are normalized to `/api/v1`
automatically. If the field is blank, the notebook falls back to the
`PUBLIC_API_BASE_URL` environment variable. Quick Cloudflare tunnel URLs can
change after restart, so reopen or update the notebook whenever the tunnel URL
changes.

The notebook never reads credentials or private identifiers from its URL.
It includes a second cell that reuses the bootstrap connection to send Colab
lineage, metrics, and runtime logs back to NeuralSpace with the compact helper
flow: `start_run -> use -> log_metrics -> produce -> finish_run`.
