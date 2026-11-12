# Dataset Builder · Colab notebooks

Training notebooks the Dataset Builder app opens in Google Colab from its Train button.

- [train-polygon.ipynb](https://colab.research.google.com/github/Luisbvi/dataset-builder-colab/blob/main/train-polygon.ipynb): YOLOv8n-seg, for a zip saved as Polygon.
- [train-box.ipynb](https://colab.research.google.com/github/Luisbvi/dataset-builder-colab/blob/main/train-box.ipynb): YOLOv8n, for a zip saved as Box.

In Colab: Runtime → Change runtime type → GPU, paste the Google Drive link of the dataset zip (shared as Anyone with the link) in the Dataset zip cell, then Runtime → Run all. Downloading from Drive is far faster than an upload; left empty, the cell asks for the zip to be uploaded instead. At the end it downloads best.onnx and best.pt (best.pt trains on later), and copies both to My Drive / Dataset Builder unless save_to_drive is unticked. Training runs into My Drive / Dataset Builder / runs (keep_on_drive): if the session stops, Runtime → Run all with the same zip resumes each training from its last.pt and skips one that finished; once the weights are saved, those runs are removed from Drive.

They are written by desktop-core/src/notebook.rs in Dataset Builder (tests/fixtures/notebook-published-*.ipynb); publish them again from there when it changes.
