# Rebuttal_figures_tabs

## Table 1. Quantitative Results for High-pass Operator (Motion_deblurring)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Operator</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">ImageNet</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Efficiency</th>
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
    <td style="text-align: center;">26.82</td>
    <td style="text-align: center;">0.890</td>
    <td style="text-align: center;">0.119</td>
    <td style="text-align: center;">24.26</td>
    <td style="text-align: center;">0.856</td>
    <td style="text-align: center;">0.142</td>
    <td style="text-align: center;"></td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (used)</td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;">~90s</td>
  </tr>
</table>

## Table 2. Ablation Studiew for Different Wavelets (Motion_deblurring)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Wavelet</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">ImageNet</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Efficiency</th>
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
    <td style="text-align: center;"></td>
  </tr>
  <tr>
    <td style="text-align: center;">Biorthogonal 4.4</td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (used)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">34.70</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.155</td>
    <td style="text-align: center;">~90s</td>
  </tr>
</table>


## Table 3. Quantitative Results of Box-inpainting **
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Dataset</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">ImageNet</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Efficiency</th>
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
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">24.57</td>
    <td style="text-align: center;">0.838</td>
    <td style="text-align: center;">0.126</td>
    <td style="text-align: center;">21.58</td>
    <td style="text-align: center;">0.739</td>
    <td style="text-align: center;">0.207</td>
    <td style="text-align: center;">~90s</td>
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
    <td style="text-align: center;">DPS*</td>
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
    <td style="text-align: center;">DAPS*</td>
    <td style="text-align: center;">~80</td>
    <td style="text-align: center;">2.28</td>
    <td style="text-align: center;">~160</td>
    <td style="text-align: center;">4.68</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FGPS*</td>
    <td style="text-align: center;">~110</td>
    <td style="text-align: center;">4.65</td>
    <td style="text-align: center;">~375</td>
    <td style="text-align: center;">11.08</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FPS*</td>
    <td style="text-align: center;"><strong>~100</strong></td>
    <td style="text-align: center;">21.56</td>
    <td style="text-align: center;"><strong>~150&#8224;</strong></td>
    <td style="text-align: center;">57.66</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FlowDPS*</td>
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
    <td style="text-align: center;">ReSample*</td>
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
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
    <td style="text-align: center;"></td>
  </tr>
</table>

## Parameter Settings of DPS
```yaml
Global diffusion setting:
  - Sampler: `ddpm`
  - Steps: `1000`
  - Noise schedule: `linear`
  - Model mean type: `epsilon`
  - Model var type: `learned_range`
  - Dynamic threshold: `False`
  - Clip denoised: `True`
  - Rescale timesteps: `False`
  - Timestep respacing: `1000`

1. Super-resolution (4x):
  - scale: 0.3

measurement:
  - in_shape: [1, 3, 256, 256]
  - scale_factor: 4

noise:
  - name: gaussian
  - sigma: 0.05

2. Motion_blur 
  - scale: 0.3

measurement:
  - kernel_size: 61
  - intensity: 0.5

noise:
  - name: gaussian
  - sigma: 0.05
