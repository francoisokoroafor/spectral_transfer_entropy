# Transfer Entropy Analysis Pipeline

A standalone, Colab-ready pipeline for computing transfer entropy (TE) on EDF/FIF files, based on IDTxl and spectral multivariate transfer entropy by Edoardo Pinzuti.
(Run's best in GPU environment)

## Features

- **Delay Scan**: Fast Gaussian-TE/GC to select optimal source→target lag per link.
- **Band-wise TE**: Analysis on filter bank: delta, theta, alpha, beta, gamma, broadband.
- **Surrogates**: Phase-randomized surrogates for source-only and target-only p-values; FDR-corrected.
- **Visualizations**: Heatmaps (TE and significance), winning band map, nested pie charts, polar plots for meta-analysis.
- **Batch Mode**: Analyze one or many EDFs; match annotation TXT by EDF prefix.
- **Output**: Per-EDF subfolder with delay scan results, figures, summaries, and text files.

## Usage

1. Upload your EDF/FIF files and annotation TXT files to Colab or local.
2. Run the notebook cells sequentially.
3. Use the main entry cell to select mode: single folder, batch, or meta-analysis.
4. Outputs are saved in subfolders with figures and summaries.

## Dependencies

- Python 3.7+
- MNE
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Joblib
- Numba (optional for GPU acceleration)

Install via pip: `pip install mne numpy scipy matplotlib seaborn joblib numba`

## References

- IDTxl GitHub: https://github.com/pwollstadt/IDTxl
- Spectral TE branch: https://github.com/pwollstadt/IDTxl/tree/feature_spectral_te/
- Wollstadt, P., Lizier, J. T., Vicente, R., Finn, C., Martinez-Zarzuela, M., Mediano, P., Novelli, L., & Wibral, M. (2018). IDTxl: The Information Dynamics Toolkit xl: a Python package for the efficient analysis of multivariate information dynamics in networks. Journal of Open Source Software, 4(34), 1081. https://doi.org/10.21105/joss.01081

## License

MIT License - see LICENSE file.

