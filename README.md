# BCI-GAN: EEG Data Augmentation for P300-Based Brain-Computer Interfaces

This repository explores the application of Generative Adversarial Networks (GANs) to augment EEG Event-Related Potential (ERP) data, specifically focusing on the P300 component, to enhance the performance of Brain-Computer Interface (BCI) systems.([researchgate.net][1])

## Features

* **Multiple GAN Architectures**: Implementation of various GAN models, including Deep Convolutional GAN (DCGAN), Wasserstein GAN with Gradient Penalty (WGAN-GP), and Variational Autoencoder (VAE).
* **Training Modes**: Support for subject-specific and subject-independent training paradigms.
* **Baseline Comparisons**: Scripts to train models without GAN-based data augmentation for performance benchmarking.
* **Data Handling**: Utilities for importing and preprocessing EEG data.([researchgate.net][1])

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/berdakh/bci-gan-master.git
   cd bci-gan-master
   ```



2. **Create a virtual environment (optional but recommended)**:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```



3. **Install required packages**:

   ```bash
   pip install -r requirements.txt
   ```



*Note: Ensure that [PyTorch](https://pytorch.org/) is installed, as it's central to the functionalities provided.*

## Usage

The repository includes several scripts to facilitate different stages of the BCI-GAN pipeline:

* **Training with GANs**:

  * `train_subject_specific.py`: Train models on subject-specific data with GAN augmentation.
  * `train_subject_independent.py`: Train models on subject-independent data with GAN augmentation.
  * `train_gan_test.py`: Evaluate different GAN models for data augmentation.

* **Training without GANs**:

  * `train_without_gans.py`: Train models without any data augmentation for baseline comparison.

* **GAN Implementations**:

  * `dcgan.py`: Implementation of Deep Convolutional GAN.
  * `wgan_gp.py`: Implementation of Wasserstein GAN with Gradient Penalty.
  * `vae.py`: Implementation of Variational Autoencoder.([researchgate.net][1])

* **Utilities**:

  * `data_import.py`: Functions for importing and preprocessing EEG data.
  * `cnn.py`: Convolutional Neural Network architecture for classification.
  * `gan_test.py`: Script to test GAN-generated data.

*To execute a training script, navigate to the repository directory and run:*

```bash
python train_subject_specific.py --gan_type dcgan
```



*Replace `dcgan` with `wgan_gp` or `vae` to use different GAN models.*

## Dataset

The implementation uses EEG datasets containing P300 ERP components. Ensure that your dataset is properly formatted and placed in the appropriate directory. Update the paths in the scripts as necessary.

## Contribution

Contributions are welcome! If you have suggestions, bug reports, or enhancements, please open an issue or submit a pull request.

## License

This project is open-source and available under the [MIT License](LICENSE).

## Acknowledgments

This repository was developed by [Berdakh Abibullaev](https://github.com/berdakh), focusing on EEG data augmentation using GANs for Brain-Computer Interface applications.

---

*For detailed explanations and methodologies, refer to the scripts and documentation included in the repository.*

If you need further assistance or have specific questions about any script or functionality, feel free to ask!

