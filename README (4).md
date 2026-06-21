# Seeing the SVM Decision Boundary

**How `C` and `γ` control the bias–variance tradeoff in an RBF-kernel Support Vector Machine.**

This repository contains a short, visual tutorial on Support Vector Machines (SVMs) with the
RBF kernel, plus the complete, runnable code that produces every figure in it. The whole thing
works in two dimensions on purpose, so you can *draw* the decision boundary and watch it change
as you turn the two most important hyperparameters.





## What the tutorial covers

1. Why a linear model fails on non-linearly-separable data, and what the RBF kernel adds.
2. `γ` (gamma) as a **complexity dial** — from underfitting to overfitting.
3. The **overfitting signature**: training accuracy rises while test accuracy turns over.
4. `C` as the **soft-margin dial**, and why `C` and `γ` interact.
5. Tuning both together honestly with **5-fold cross-validation**.
6. **Support vectors** — the handful of points that actually define the model.






# 1. Clone
git clone https://github.com/<username>/svm-rbf-tutorial.git
cd svm-rbf-tutorial

# 2. (Recommended) create a virtual environment
python -m venv .venv
source .venv/bin/activate        # on Windows: .venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt   # or: pip install numpy matplotlib scikit-learn jupyter

# 4. Launch
jupyter notebook svm_rbf_tutorial.ipynb


Then run all cells from top to bottom. No manual steps or downloads are required — the dataset
(`make_moons`) is generated in code.





numpy
matplotlib
scikit-learn
jupyter


## Reproducibility

All randomness is seeded (`random_state = 42`) so the figures are identical on every run.
The notebook is deterministic end-to-end.

## Accessibility

This project takes several steps to be accessible:

- Classes are encoded by **both colour and marker shape** (circle vs triangle), so plots are
  readable in greyscale and for colour-vision deficiency.
- Figures use the **Okabe–Ito** colourblind-safe palette and the perceptually-uniform
  **viridis** colourmap.
- The written tutorial uses real heading styles (screen-reader navigable) and provides
  descriptive **alt text** and captions for every figure.

## Licence

Released under the **MIT Licence**  see [`LICENSE`](LICENSE). You are free to use, modify, and
share this material, including for your own teaching, provided the licence and copyright notice
are included.

## References

1. Cortes, C. & Vapnik, V. (1995). *Support-Vector Networks.* Machine Learning, 20(3), 273–297.
2. Boser, B., Guyon, I. & Vapnik, V. (1992). *A Training Algorithm for Optimal Margin Classifiers.* Proceedings of COLT '92, 144–152.
3. Hastie, T., Tibshirani, R. & Friedman, J. (2009). *The Elements of Statistical Learning* (2nd ed.), Ch. 12. Springer.
4. Pedregosa et al. (2011). *Scikit-learn: Machine Learning in Python.* JMLR, 12, 2825–2830.
5. scikit-learn user guide — [Support Vector Machines](https://scikit-learn.org/stable/modules/svm.html)
   and [RBF SVM parameters](https://scikit-learn.org/stable/auto_examples/svm/plot_rbf_parameters.html).


