# Attribute Switching Mechanism

This repository contains code for the Attribute Switching mechanism.

## How it works?

1. First, we train a diffusion model using two datasets:
   - FairFace dataset by Karkkainen, K., & Joo, J. [^1]
   - CelebA dataset by Liu, Z., Luo, P., Wang, X., & Tang, X [^2]
   
   We base our training on the code available at https://github.com/VSehwag/minimal-diffusion.

2. To ensure the utilization of the FairFace dataset, we implemented modifications to the 'data.py' file from the minimal-diffusion repository.

3. Other training details, please refer https://github.com/VSehwag/minimal-diffusion repository.

If you plan to use this code for attribute switching, you can do so without cloning the https://github.com/VSehwag/minimal-diffusion repository. However, if you choose to use that code, please make sure to give credit to the original repository: https://github.com/VSehwag/minimal-diffusion.

## References

- Karkkainen, K., & Joo, J. (2021). FairFace: Face Attribute Dataset for Balanced Race, Gender, and Age for Bias Measurement and Mitigation. In Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (pp. 1548-1558) [^1].

- Liu, Z., Luo, P., Wang, X., & Tang, X. (2018). Large-scale CelebFaces Attributes (CelebA) dataset. Retrieved August 15, 2018 [^2].
