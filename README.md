# Attribute Switching Mechanism

This repository contains code for the Attribute Switching mechanism, which allows you to perform attribute manipulation in images.

Please refer the paper "Fair Sampling in Diffusion Models through Switching Mechanism" (AAAI24 accepted paper) for more details about the mechanism.

You can access the full version of the paper at https://arxiv.org/abs/2401.03140
## Introduction
We base our training on the code available at https://github.com/VSehwag/minimal-diffusion. To ensure the utilization of the FairFace dataset, we implemented modifications to the 'data.py' file from the minimal-diffusion repository. For more details about the training process, please refer to the [minimal-diffusion repository](https://github.com/VSehwag/minimal-diffusion).

If you plan to use this code for attribute switching, you can do so without cloning the [minimal-diffusion repository](https://github.com/VSehwag/minimal-diffusion). However, if you choose to use that code, please make sure to give credit to the original repository.

## How to Use

To use this code, follow these steps:

1. **Train the Diffusion Model**:
   - You can choose to use a pre-trained diffusion model or train your own. Use the `train_diffusion_based_on_minimal_diffusion.ipynb` file for training.
   - Ensure you prepare the necessary data and enter the file path when running the notebook.
   - In the paper, we used the FairFace dataset [^1], CelebA dataset [^2], and CIFAR-10 dataset [^3]. Minimal-diffusion supports additional datasets.

2. **Search for Optimal Tau ($\tau$)**:
   - Run the `tau_searching.ipynb` notebook to find the optimal value of $\tau$ for your trained model.
   - Enter the path to your trained model during this step.

3. **Sample Data with Attribute Switching**:
   - Finally, use the `sampling_with_attribute_switching.ipynb` notebook to sample data with attribute switching.
   - Provide the model path and the $\tau$ value obtained in the previous step.

To run the code using pre-trained models from the [Stable diffusion with Hugging Face Diffuser](https://huggingface.co/blog/stable_diffusion), use the `pretrained_diffuser_switching.ipynb` notebook.

## Contact
If you have any questions about code or would like access to the models I've used in my paper, feel free to e-mail me at uznhigh [AT] snu.ac.kr 

## Citation
If you gained insights from this paper, please cite the following work:

```bibtex
@inproceedings{choi2024fair,
  title={Fair sampling in diffusion models through switching mechanism},
  author={Choi, Yujin and Park, Jinseong and Kim, Hoki and Lee, Jaewook and Park, Saerom},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={38},
  number={20},
  pages={21995--22003},
  year={2024}
}
```
## References

- Karkkainen, K., & Joo, J. (2021). FairFace: Face Attribute Dataset for Balanced Race, Gender, and Age for Bias Measurement and Mitigation. In Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (pp. 1548-1558) [^1].

- Liu, Z., Luo, P., Wang, X., & Tang, X. (2018). Large-scale CelebFaces Attributes (CelebA) dataset. Retrieved August 15, 2018 [^2].

- Krizhevsky, A., & Hinton, G. (2009). Learning multiple layers of features from tiny images [^3].
