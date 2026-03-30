# Rebuttal_figures_tabs

## Table 1. Quantitative Results for High-pass Operator (Motion_deblurring)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Operator</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">ImageNet</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">High-pass</td>
    <td style="text-align: center;">10.82</td>
    <td style="text-align: center;">0.533</td>
    <td style="text-align: center;">0.492</td>
    <td style="text-align: center;">24.26</td>
    <td style="text-align: center;">0.856</td>
    <td style="text-align: center;">0.142</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (used)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">34.70</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.155</td>
  </tr>
</table>

## Table 2. Ablation Studies for Different Wavelets (Motion_deblurring)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Wavelet</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">ImageNet</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">Daubechies-2</td>
    <td style="text-align: center;">26.82</td>
    <td style="text-align: center;">0.890</td>
    <td style="text-align: center;">0.119</td>
    <td style="text-align: center;">24.26</td>
    <td style="text-align: center;">0.856</td>
    <td style="text-align: center;">0.142</td>
  </tr>
  <tr>
    <td style="text-align: center;">Biorthogonal 4.4</td>
    <td style="text-align: center;">30.59</td>
    <td style="text-align: center;">0.876</td>
    <td style="text-align: center;">0.151</td>
    <td style="text-align: center;">27.64</td>
    <td style="text-align: center;">0.811</td>
    <td style="text-align: center;">0.186</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (used)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">34.70</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.155</td>
  </tr>
</table>

## Figure 1. Qualitative results for Different Wavelets (Motion_deblurring)

![wave_1](figures/wave_1.png)
![wave_2](figures/wave_2.png)

## Table 3. Quantitative Results of Box-inpainting
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Method</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">ImageNet</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>

  <tr>
    <td style="text-align: center;">DAPS(ours)</td>
    <td style="text-align: center;">24.07</td>
    <td style="text-align: center;">0.814</td>
    <td style="text-align: center;">0.133</td>
    <td style="text-align: center;">21.43</td>
    <td style="text-align: center;">0.725</td>
    <td style="text-align: center;">0.214</td>
  </tr>
  <tr>
    <td style="text-align: center;">DPS</td>
    <td style="text-align: center;">22.51</td>
    <td style="text-align: center;">0.792</td>
    <td style="text-align: center;">0.209</td>
    <td style="text-align: center;">18.94</td>
    <td style="text-align: center;">0.722</td>
    <td style="text-align: center;">0.257</td>
  </tr>
  <tr>
    <td style="text-align: center;">DDRM</td>
    <td style="text-align: center;">22.26</td>
    <td style="text-align: center;">0.801</td>
    <td style="text-align: center;">0.207</td>
    <td style="text-align: center;">18.63</td>
    <td style="text-align: center;">0.733</td>
    <td style="text-align: center;">0.254</td>
  </tr>
  <tr>
    <td style="text-align: center;">DDNM</td>
    <td style="text-align: center;">24.47</td>
    <td style="text-align: center;">0.837</td>
    <td style="text-align: center;">0.235</td>
    <td style="text-align: center;">21.64</td>
    <td style="text-align: center;">0.748</td>
    <td style="text-align: center;">0.319</td>
  </tr>
  <tr>
    <td style="text-align: center;">DCDP</td>
    <td style="text-align: center;">23.89</td>
    <td style="text-align: center;">0.760</td>
    <td style="text-align: center;">0.163</td>
    <td style="text-align: center;">-</td>
    <td style="text-align: center;">-</td>
    <td style="text-align: center;">-</td>
  </tr>
  <tr>
    <td style="text-align: center;">FPS-SMC</td>
    <td style="text-align: center;">24.86</td>
    <td style="text-align: center;">0.823</td>
    <td style="text-align: center;">0.146</td>
    <td style="text-align: center;">22.16</td>
    <td style="text-align: center;">0.726</td>
    <td style="text-align: center;">0.208</td>
  </tr>

  <tr>
    <td style="text-align: center;">LatentDAPS(ours)</td>
    <td style="text-align: center;">23.99</td>
    <td style="text-align: center;">0.802</td>
    <td style="text-align: center;">0.194</td>
    <td style="text-align: center;">17.19</td>
    <td style="text-align: center;">0.624</td>
    <td style="text-align: center;">0.340</td>
  </tr>
  <tr>
    <td style="text-align: center;">PSLD</td>
    <td style="text-align: center;">24.22</td>
    <td style="text-align: center;">0.813</td>
    <td style="text-align: center;">0.158</td>
    <td style="text-align: center;">20.10</td>
    <td style="text-align: center;">0.694</td>
    <td style="text-align: center;">0.465</td>
  </tr>
  <tr>
    <td style="text-align: center;">ReSample</td>
    <td style="text-align: center;">20.06</td>
    <td style="text-align: center;">0.749</td>
    <td style="text-align: center;">0.184</td>
    <td style="text-align: center;">18.29</td>
    <td style="text-align: center;">0.631</td>
    <td style="text-align: center;">0.262</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">24.57</td>
    <td style="text-align: center;">0.838</td>
    <td style="text-align: center;">0.126</td>
    <td style="text-align: center;">21.58</td>
    <td style="text-align: center;">0.739</td>
    <td style="text-align: center;">0.207</td>
  </tr>
</table>

## Table 4. Computational Cost for Compared Methods (Motion_deblurring)
<table>
  <tr>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Method</th>
    <th colspan="2" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="2" style="text-align: center; white-space: nowrap;">ImageNet</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Diffusion NFE</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">Runtime (s/img)</th>
    <th style="text-align: center; white-space: nowrap;">Peak Mem (GB)</th>
    <th style="text-align: center; white-space: nowrap;">Runtime (s/img)</th>
    <th style="text-align: center; white-space: nowrap;">Peak Mem (GB)</th>
  </tr>
  <tr>
    <td style="text-align: center;">DPS</td>
    <td style="text-align: center;">~65</td>
    <td style="text-align: center;">9.44</td>
    <td style="text-align: center;">~200</td>
    <td style="text-align: center;">9.44</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">DDRM</td>
    <td style="text-align: center;">~5</td>
    <td style="text-align: center;">4.77</td>
    <td style="text-align: center;">~5</td>
    <td style="text-align: center;">6.44</td>
    <td style="text-align: center;">20</td>
  </tr>
  <tr>
    <td style="text-align: center;">DDNM</td>
    <td style="text-align: center;">~5</td>
    <td style="text-align: center;">4.70</td>
    <td style="text-align: center;">~15</td>
    <td style="text-align: center;">6.37</td>
    <td style="text-align: center;">100</td>
  </tr>
  <tr>
    <td style="text-align: center;">DAPS</td>
    <td style="text-align: center;">~80</td>
    <td style="text-align: center;">2.28</td>
    <td style="text-align: center;">~160</td>
    <td style="text-align: center;">4.68</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FGPS</td>
    <td style="text-align: center;">~110</td>
    <td style="text-align: center;">4.65</td>
    <td style="text-align: center;">~375</td>
    <td style="text-align: center;">11.08</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FPS</td>
    <td style="text-align: center;"><strong>~100</strong></td>
    <td style="text-align: center;">21.56</td>
    <td style="text-align: center;"><strong>~150*</strong></td>
    <td style="text-align: center;">57.66</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FlowDPS</td>
    <td style="text-align: center;">~4</td>
    <td style="text-align: center;">12.96</td>
    <td style="text-align: center;">~4</td>
    <td style="text-align: center;">12.96</td>
    <td style="text-align: center;">28</td>
  </tr>
  <tr>
    <td style="text-align: center;">DCDP</td>
    <td style="text-align: center;">~2</td>
    <td style="text-align: center;">4.93</td>
    <td style="text-align: center;">~5</td>
    <td style="text-align: center;">12.55</td>
    <td style="text-align: center;">181</td>
  </tr>
  <tr>
    <td style="text-align: center;">ReSample</td>
    <td style="text-align: center;">~780</td>
    <td style="text-align: center;">6.77</td>
    <td style="text-align: center;">~780</td>
    <td style="text-align: center;">6.77</td>
    <td style="text-align: center;">500</td>
  </tr>
  <tr>
    <td style="text-align: center;">PSLD*</td>
    <td style="text-align: center;">~790</td>
    <td style="text-align: center;">21.32</td>
    <td style="text-align: center;">~790</td>
    <td style="text-align: center;">21.32</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">~130</td>
    <td style="text-align: center;">2.23</td>
    <td style="text-align: center;">~200</td>
    <td style="text-align: center;">4.56</td>
    <td style="text-align: center;">1000</td>
  </tr>
</table>
* indicates that this experiment was conducted on a single RTX Pro 6000 Blackwell because it exceeded the memory capacity of a single NVIDIA A6000. The RTX Pro 6000 Blackwell also delivers substantially higher computational speed, approximately 2.5× that of the NVIDIA A6000.

## Table 5. Ablation Studies of Noise Schedule (N) (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Steps</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Efficiency (/s)</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">50</td>
    <td style="text-align: center;">35.82</td>
    <td style="text-align: center;">0.924</td>
    <td style="text-align: center;">0.069</td>
    <td style="text-align: center;">~35</td>
  </tr>
  <tr>
    <td style="text-align: center;">100</td>
    <td style="text-align: center;">36.28</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.055</td>
    <td style="text-align: center;">~65</td>
  </tr>

  <tr>
    <td style="text-align: center;">300</td>
    <td style="text-align: center;">37.08</td>
    <td style="text-align: center;">0.953</td>
    <td style="text-align: center;">0.039</td>
    <td style="text-align: center;">~195</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (used)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">~130</td>
  </tr>
</table>

## Figure 2. Qualitative results for DPS (1000 Steps)

![dps_1](figures/comp_dps_1.png)
![dps_2](figures/comp_dps_2.png)

## Table 6. Noise and Diffusion Scheduler Config of Our Method
<table>
  <tr>
    <th style="text-align: center;">Parameter</th>
    <th style="text-align: center; white-space: nowrap;">Default</th>
    <th style="text-align: center;">Description</th>
  </tr>
  <tr>
    <td style="text-align: center;">N</td>
    <td style="text-align: center;">200</td>
    <td style="text-align: center;">Num_steps, which determines the total number of diffusion iterations of line 2 in Alg.1</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma_{\max}$</td>
    <td style="text-align: center;">100</td>
    <td style="text-align: center;">Initial noise level of $\sigma$ shown in Alg.1 </td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma_{\min}$</td>
    <td style="text-align: center;">0.1</td>
    <td style="text-align: center;">Final noise level pf $\sigma$ shown in Alg.1</td>
  </tr>
  <tr>
    <td style="text-align: center;">timestep</td>
    <td style="text-align: center;">poly-7</td>
    <td style="text-align: center;">Time-step discretization scheme, polynomial with $\rho = 7$ </td>
  </tr>
  <tr>
    <td style="text-align: center;">T</td>
    <td style="text-align: center;">200</td>
    <td style="text-align: center;">Inner loop of optimization steps shown in line 8 of Alg.1</td>
  </tr>
  <tr>
    <td style="text-align: center;">n</td>
    <td style="text-align: center;">5</td>
    <td style="text-align: center;">Denoising step of the PF-ODE in line 3 of Alg.1</td>
  </tr>
</table>

**Discretization Formula (EDM Scheduler):**

$\[
\sigma_i = \left( \sigma_{\max}^{1/\rho} + \frac{i}{N-1}\left(\sigma_{\min}^{1/\rho} - \sigma_{\max}^{1/\rho}\right) \right)^{\rho}
\]$

## Parameter Settings of DPS
```yaml
Global diffusion setting:
   Sampler: `ddpm`
   Steps: `1000`
   Noise schedule: `linear`
   Model mean type: `epsilon`
   Model var type: `learned_range`
   Dynamic threshold: `False`
   Clip denoised: `True`
   Rescale timesteps: `False`
   Timestep respacing: `1000`

1. Super-resolution (4x):
   scale: 0.3

  measurement:
     in_shape: [1, 3, 256, 256]
     scale_factor: 4
  
  noise:
     name: gaussian
     sigma: 0.05

2. Motion_blur 
   scale: 0.3

  measurement:
     kernel_size: 61
     intensity: 0.5

  noise:
     name: gaussian
     sigma: 0.05

3. Gaussian_blur
   scale: 0.3

  measurement:
    kernel_size: 61
    intensity: 3.0

  noise:
    name: gaussian
    sigma: 0.05

4. Inpainting
    scale: 0.5

  measurement:
    operator:
      mask_prob_range: [0.3, 0.7] 
      image_size: 256

  noise:
    name: gaussian
    sigma: 0.05
