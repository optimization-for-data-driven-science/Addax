# **Addax: Utilizing Zeroth-Order Gradients to Improve the Memory Efficiency and Performance of SGD for Fine-Tuning Language Models**
## Zeman Li, Xinwei Zhang, Peilin Zhong, Yuan Deng, Meisam Razaviyayn, Vahab Mirrokn

We post the anonymized version of the codebase that we used during the ICLR review process in case anyone is interested in a preliminary view of our work. We will prepare and release the official codebase to replace this anonymized version soon.

### [Link to the anonymized version of the Addax codebase](https://anonymous.4open.science/r/Addax-62ED)

We would like to share the following pointers to make navigating our code easier. Our implementation is adapted from MeZO (Malladi et al., 2024). We made the following major modifications to create Addax:

* **Dataset Partitioning:** In lines 589–735 of [run_2_loader.py](https://anonymous.4open.science/r/Addax-62ED/large_models/run_2_loader.py), we partition the dataset based on sequence length, which corresponds to lines 2–5 in Algorithm 1 of our paper.
* **In-Place Backward Propagation:** In lines 762–774 of [run_2_loader.py](https://anonymous.4open.science/r/Addax-62ED/large_models/run_2_loader.py), we enable in-place backward propagation, corresponding to lines 9–12 in Algorithm 1.
* **Update Rule Implementation:** In lines 1365–1420 of [trainer_2_loader.py](https://anonymous.4open.science/r/Addax-62ED/large_models/trainer_2_loader.py), we utilize the existing MeZO implementation to implement the update rule described in Equation (3) of our paper.

If you have any questions related to the code or the paper, feel free to email Zeman Li (zemanli@usc.edu). If you encounter any problems when using the code or want to report a bug, you can open an issue. Please try to specify the problem in detail so we can help you better and more quickly!
