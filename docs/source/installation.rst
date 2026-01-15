Installation & Download
====================================

To ensure the Graph Neural Networks (GNNs) run correctly, PyTorch Geometric (PyG) and its dependencies must be installed strictly matching your PyTorch and CUDA versions.

.. code-block:: bash

   conda create -n mistic_env python==3.8
   conda activate mistic_env

   pip install MISTIC

If you want to use MISTIC with Jupyter Lab/Notebook (e.g., run experimental notebooks, debug with interactive environment), install the `dev` optional dependencies:

.. code-block:: bash

   pip install MISTIC[dev]
   python -m ipykernel install --user --name=mistic_env

Install a version of PyTorch compatible with your CUDA driver (**e.g., CUDA 12.1**):

.. code-block:: bash

   # Install PyTorch (GPU version)
   pip install torch==2.1.0 torchvision==0.16.0 torchaudio==2.1.0 --index-url https://download.pytorch.org/whl/cu121

Note: This is the most critical step. Do not simply use pip install torch-geometric. You must install the sparse libraries (torch_scatter, torch_sparse) that match your PyTorch version to enable GNN acceleration (**e.g., torch-2.1.0 and cu121**).

.. code-block:: bash

   # Install PyG Dependencies (Must match torch version)
   pip install torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-2.1.0+cu121.html

   # Install PyTorch Geometric
   pip install torch_geometric