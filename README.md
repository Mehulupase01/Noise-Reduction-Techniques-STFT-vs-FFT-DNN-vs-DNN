# Noise Reduction Techniques STFT vs FFT+ DNN vs DNN
 This project compares three audio denoising techniques—Short-Time Fourier Transform (STFT), a hybrid Fast Fourier Transform + Deep Neural Networks (FFT+DNN), and Deep Neural Networks (DNN) for noise reduction in speech. Using metrics like SNR, PESQ, MSE, and STOI, the project evaluates the effectiveness of each technique in improving audio clarity under different noise conditions

## Description
This project compares three audio denoising techniques—Short-Time Fourier Transform (STFT), a hybrid Fast Fourier Transform + Deep Neural Networks (FFT+DNN), and Deep Neural Networks (DNN) for noise reduction in speech. Using metrics like SNR, PESQ, MSE, and STOI, the project evaluates the effectiveness of each technique in improving audio clarity under different noise conditions.

## Task / Problem Statement
Noise reduction is essential for improving audio quality in telecommunications, speech processing, and multimedia applications. This project focuses on comparing three popular audio denoising methods: STFT, FFT+DNN, and DNN. The goal is to determine which method provides the best noise suppression and clarity, especially under various noisy conditions, using performance metrics like Signal-to-Noise Ratio (SNR), Perceptual Evaluation of Speech Quality (PESQ), Mean Squared Error (MSE), and Short-Time Objective Intelligibility (STOI).

## Sub-Tasks
1. **Implement STFT-based Denoising**: Apply spectral decomposition to reduce stationary noise.
2. **Implement FFT+DNN-based Denoising**: Use FFT for feature extraction followed by DNN for noise suppression.
3. **Implement DNN-based Denoising**: Employ deep learning to directly map noisy audio to clean audio.
4. **Evaluate each method**: Assess the denoising performance using SNR, PESQ, MSE, and STOI metrics.
5. **Compare results across metrics**: Analyze the strengths and weaknesses of each technique in different noise scenarios.
6. **Visualize the results**: Present spectrograms and metrics comparisons to understand the impact of each technique.

## Implementation Details
### 1. **Short-Time Fourier Transform (STFT)**
   - **Method**: STFT splits the signal into overlapping frames, applies FFT, suppresses noise in the spectral domain, and then reconstructs the denoised audio.
   - **Strengths**: Computationally efficient and effective for stationary noise.
   - **Weaknesses**: Performs poorly under non-stationary noise conditions.

### 2. **FFT + DNN**
   - **Method**: The hybrid method combines FFT-based feature extraction with DNN-based noise suppression.
   - **Strengths**: Improves noise suppression, especially for non-stationary noise, while balancing computational efficiency.
   - **Weaknesses**: Loss of temporal information due to FFT preprocessing.

### 3. **Deep Neural Networks (DNN)**
   - **Method**: DNN directly learns mappings from noisy audio to clean audio, providing an end-to-end denoising solution.
   - **Strengths**: Excellent performance across both stationary and non-stationary noise conditions.
   - **Weaknesses**: Computationally expensive and requires large datasets.

## Results
- **SNR (Signal-to-Noise Ratio)**: DNN achieves the highest SNR (7.22 dB), providing the best signal clarity.
- **MSE (Mean Squared Error)**: DNN minimizes reconstruction errors, with the lowest MSE value (0.000004).
- **PESQ (Perceptual Quality)**: DNN achieves the highest perceptual quality score (3.74), indicating that the denoised audio sounds the most natural.
- **STOI (Speech Intelligibility)**: DNN also leads in intelligibility, with an STOI of 0.92, ensuring high speech clarity.

## Algorithms Used
- **STFT**: Transforms the signal into the time-frequency domain and performs noise suppression through spectral filtering.
- **FFT + DNN**: Uses FFT to extract frequency-domain features and applies DNN to suppress noise in the spectral coefficients.
- **DNN**: A deep learning model trained to map noisy audio directly to clean audio, learning complex noise patterns.

## Results Summary
- **DNN** outperforms both **STFT** and **FFT+DNN** in all metrics, achieving the highest clarity, perceptual quality, and intelligibility.
- **FFT+DNN** provides a middle ground, balancing computational efficiency with improved performance over STFT.
- **STFT** is computationally efficient but struggles with non-stationary noise and exhibits residual artifacts.

## Visualizations
The results of this comparison are visually presented through spectrograms and averaged performance metrics. The following metrics were plotted:
- **SNR**: Higher values indicate better signal clarity.
- **MSE**: Lower values indicate better reconstruction accuracy.
- **PESQ**: Higher values indicate better speech quality.
- **STOI**: Higher values indicate better intelligibility.

## Future Work
- Explore hybrid models combining DNN and traditional methods to enhance real-time processing efficiency.
- Investigate lightweight DNN architectures to reduce computational costs.
- Extend the dataset to include more complex noise conditions, such as dynamic noise or overlapping noise sources.

## Conclusion
- **DNN** is the most effective method for audio denoising, particularly in non-stationary noise conditions, but it requires significant computational resources.
- **FFT+DNN** offers a good trade-off between performance and computational efficiency.
- **STFT** remains useful for simpler, computationally constrained environments, but it has limitations in handling dynamic noise.

## References
- [Noise-Reduction GitHub Repository](https://github.com/Dhriti03/Noise-Reduction)
- [Audio Denoising Using FFT and CNN](https://github.com/YasinRezvani/Audio_Denoising_Using_FFT_And_CNN)
- [Audio Denoising - Final Code](https://github.com/stephen-harmon-newman/Audio-Denoising/tree/master)

