Overview
====================================

.. image:: _static/figure1.png
   :width: 600

**a.** MISTIC accommodates integration of multi-slice omics data from the same or distinct tissues. For each spatial transcriptomic slice, three core matrices are derived via the BANKSY algorithm. **b.** Two distinct matrices are built for each slice: (i) Spatial distance matrix; (ii) Expression similarity matrix. Global intra-slice matrices are formed by block-diagonal concatenation of slice-specific matrices across all slices. **c.** Inter-slice mutual nearest neighbor (MNN) pairs are detected in the global feature matrix. The final inter-slice adjacency matrix retains only high-confidence MNN pairs. **d.** Inputs include gene expression data and microenvironment data combined with adjacency matrices, outputting batch-corrected latent features. **e.** The integrated latent features support three core applications: Batch effect removal(I), Condition-specific niche identification(II), Microenvironmental interaction analysis(III).