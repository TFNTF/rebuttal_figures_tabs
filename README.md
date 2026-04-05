# Rebuttal_figures_tabs


## Table 1. Quantitative Results for High-pass Operator (Motion_deblurring, for Reviewer kDyZ)  
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
    <td style="text-align: center;">11.20</td>
    <td style="text-align: center;">0.556</td>
    <td style="text-align: center;">0.430</td>
    <td style="text-align: center;">11.68</td>
    <td style="text-align: center;">0.659</td>
    <td style="text-align: center;">0.513</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (Identical to those in Table 15)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">34.70</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.155</td>
  </tr>
</table>
Table 1 shows that our method (NFC) does not produce satisfactory results when high-frequency information is preserved in the measurements (e.g., under a high-pass filter), which represents one failure mode of NFC.

## Table 2. Ablation Studies for Different Wavelets (Motion_deblurring, for Reviewer sLBM, ZYag)
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

## Figure 1. Qualitative Results for Different Wavelets (Motion_deblurring)

![wave_1](figures/wave_1.png)
![wave_2](figures/wave_2.png)

## Table 3. Computational Cost for Compared Methods (Motion_deblurring)
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
    <td style="text-align: center;">~100</td>
    <td style="text-align: center;">21.56</td>
    <td style="text-align: center;">~150*</td>
    <td style="text-align: center;">57.66</td>
    <td style="text-align: center;">1000</td>
  </tr>
  <tr>
    <td style="text-align: center;">FlowDPS†</td>
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
    <td style="text-align: center;">PSLD</td>
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

† indicates that the reported efficiency partly benefits from using a foundation model trained with Flow Matching, whereas the checkpoints for the other methods are based on DDPM training.

## Table 4. Quantitative Results Under The Same Computational Budget* (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Method</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Runtime (s/img)</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">FlowDPS</td>
    <td style="text-align: center;">22.16</td>
    <td style="text-align: center;">0.655</td>
    <td style="text-align: center;">0.424</td>
    <td style="text-align: center;">~4</td>
  <tr>
  <tr>
    <td style="text-align: center;">DCDP</td>
    <td style="text-align: center;">25.08</td>
    <td style="text-align: center;">0.512</td>
    <td style="text-align: center;">0.364</td>
    <td style="text-align: center;">~2</td>
  <tr>
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">27.31</td>
    <td style="text-align: center;">0.603</td>
    <td style="text-align: center;">0.264</td>
    <td style="text-align: center;">~2</td>
  </tr>
</table>
* indicates that, for this experiment, we compare only with methods that are more efficient and provide publicly available official code for this task. We further set N=9 and T=90 to ensure a matched time budget.



## Figure 2. Qualitative Results for Real-world Blur According to BlindDPS (Motion_deblurring)

![real_1](figures/real_1.png)
![real_2](figures/real_2.png)

## Table 5. Qualitative Results for Real-world Blur According to BlindDPS (Motion_deblurring)
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
    <td style="text-align: center;">BlindDPS</td>
    <td style="text-align: center;">23.58</td>
    <td style="text-align: center;">0.646</td>
    <td style="text-align: center;">0.231</td>
    <td style="text-align: center;">22.17</td>
    <td style="text-align: center;">0.579</td>
    <td style="text-align: center;">0.352</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">29.62</td>
    <td style="text-align: center;">0.785</td>
    <td style="text-align: center;">0.156</td>
    <td style="text-align: center;">26.09</td>
    <td style="text-align: center;">0.704</td>
    <td style="text-align: center;">0.215</td>
  </tr>
</table>


## Table 6. Quantitative Results for Operator Mismatch (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Description</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">kernel size 51 & intensity 0.05 </td>
    <td style="text-align: center;">19.36</td>
    <td style="text-align: center;">0.477</td>
    <td style="text-align: center;">0.416</td>
  </tr>
  <tr>
    <td style="text-align: center;">kernel size 71 & intensity 0.05</td>
    <td style="text-align: center;">15.203</td>
    <td style="text-align: center;">0.286</td>
    <td style="text-align: center;">0.526</td>
  </tr>
  <tr>
    <td style="text-align: center;">kernel size 61 & intensity 0.65</td>
    <td style="text-align: center;">9.69</td>
    <td style="text-align: center;">0.155</td>
    <td style="text-align: center;">0.689</td>
  </tr>
  <tr>
    <td style="text-align: center;">kernel size 61 & intensity 0.08</td>
    <td style="text-align: center;">10.03</td>
    <td style="text-align: center;">0.150</td>
    <td style="text-align: center;">0.672</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (kernel size 61 & intensity 0.50)</td>
    <td style="text-align: center;">27.31</td>
    <td style="text-align: center;">0.603</td>
    <td style="text-align: center;">0.264</td>
  </tr>
</table>

## Table 7. Abaltion Studies of Full-band Strategy (FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Strategy</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Super-resolution</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Motion Deblurring</th>
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
    <td style="text-align: center;">Ours (w/o. Freq. & Haar)</td>
    <td style="text-align: center;">29.79</td>
    <td style="text-align: center;">0.818</td>
    <td style="text-align: center;">0.173</td>
    <td style="text-align: center;">29.67</td>
    <td style="text-align: center;">0.839</td>
    <td style="text-align: center;">0.163</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (used)</td>
    <td style="text-align: center;">31.88</td>
    <td style="text-align: center;">0.890</td>
    <td style="text-align: center;">0.090</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
  </tr>
</table>

## Figure 3. Qualitative Results for Ablation Studies

![abl_1](figures/ablation.png)

## Table 8. Quantitative Results of Box-inpainting
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
    <td style="text-align: center;">DAPS</td>
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
    <td style="text-align: center;">LatentDAPS</td>
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

## Figure 4. Qualitative Results for Box-inpainting

![box_1](figures/box_1.png)
![box_2](figures/box_2.png)

## Table 9. Ablation Studies of Measurement-consistency Updates with Different Strengths Across Frequency Components (Motion_deblurring)
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
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">14.88</td>
    <td style="text-align: center;">0.179</td>
    <td style="text-align: center;">0.583</td>
    <td style="text-align: center;">15.02</td>
    <td style="text-align: center;">0.244</td>
    <td style="text-align: center;">0.482</td>
  </tr>
</table>


## Table 10. Ablation Studies of Noise Schedule (N) (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">N (Diffusion Steps in Line 2 of Alg.1)</th>
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
    <td style="text-align: center;">Ours (200)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">~130</td>
  </tr>
</table>

## Table 11. Ablation Studies of Optimization Steps (T) (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">T (Optimization Steps in Line 8 of Alg.1)</th>
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
    <td style="text-align: center;">35.81</td>
    <td style="text-align: center;">0.943</td>
    <td style="text-align: center;">0.047</td>
    <td style="text-align: center;">~70</td>
  </tr>
  <tr>
    <td style="text-align: center;">100</td>
    <td style="text-align: center;">36.86</td>
    <td style="text-align: center;">0.945</td>
    <td style="text-align: center;">0.050</td>
    <td style="text-align: center;">~110</td>
  </tr>

  <tr>
    <td style="text-align: center;">300</td>
    <td style="text-align: center;">36.95</td>
    <td style="text-align: center;">0.950</td>
    <td style="text-align: center;">0.041</td>
    <td style="text-align: center;">~160</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (200)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">~130</td>
  </tr>
</table>

## Table 12. Ablation Studies of $\sigma$ of Eq.(5) (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">$\sigma$</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">0.0</td>
    <td style="text-align: center;">38.53</td>
    <td style="text-align: center;">0.971</td>
    <td style="text-align: center;">0.034</td>
  </tr>
  <tr>
    <td style="text-align: center;">0.03</td>
    <td style="text-align: center;">37.49</td>
    <td style="text-align: center;">0.963</td>
    <td style="text-align: center;">0.042</td>
  </tr>

  <tr>
    <td style="text-align: center;">0.07</td>
    <td style="text-align: center;">34.95</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.082</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (0.05)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
  </tr>
</table>

## Table 13. Ablation Studies of Other Parameters (Motion_deblurring On FFHQ)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Parameters</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">$w_{k,L}=0.8$ (All remaining parameters are kept identical to those in Table 15)</td> 
    <td style="text-align: center;">35.21</td>
    <td style="text-align: center;">0.942</td>
    <td style="text-align: center;">0.045</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\lambda_k$ starts at 0.30 and decays to 0. (All remaining parameters are kept identical to those in Table 15)</td>
    <td style="text-align: center;">35.33</td>
    <td style="text-align: center;">0.943</td>
    <td style="text-align: center;">0.045</td>
  </tr>

  <tr>
    <td style="text-align: center;">$d_s=0.3$ (All remaining parameters are kept identical to those in Table 15)</td>
    <td style="text-align: center;">30.78</td>
    <td style="text-align: center;">0.813</td>
    <td style="text-align: center;">0.187</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (Identical to those in Table 15)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
  </tr>
</table>


## Figure 5. Qualitative Comparison Between DPS (1000 Steps) and Ours

![dps_1](figures/comp_dps_1.png)
![dps_2](figures/comp_dps_2.png)

## Figure 6. Qualitative Comparison Between SILO and Ours

![silo](figures/silo.png)

## Table 14. Quantitative Comparison Between SILO and Ours on FFHQ*
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Methods</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Gaussian Deblurring</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Super-resolution</th>
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
    <td style="text-align: center;">SILO</td>
    <td style="text-align: center;">26.53</td>
    <td style="text-align: center;">0.745</td>
    <td style="text-align: center;">0.317</td>
    <td style="text-align: center;">26.79</td>
    <td style="text-align: center;">0.761</td>
    <td style="text-align: center;">0.297</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours</td>
    <td style="text-align: center;">29.99</td>
    <td style="text-align: center;">0.821</td>
    <td style="text-align: center;">0.175</td>
    <td style="text-align: center;">31.88</td>
    <td style="text-align: center;">0.890</td>
    <td style="text-align: center;">0.090</td>
  </tr>
</table>

* indicates that, based on the publicly available SILO codebase, only Gaussian deblurring and super-resolution on the FFHQ dataset are supported. 

## Table 15. Parameters Config of Our Method
<table>
  <tr>
    <th style="text-align: center;">Parameter</th>
    <th style="text-align: center; white-space: nowrap;">Default</th>
    <th style="text-align: center;">Description</th>
  </tr>
  <tr>
    <td style="text-align: center;">N</td>
    <td style="text-align: center;">200</td>
    <td style="text-align: center;">Num_steps, which determines the total number of diffusion iterations of line 2 in Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma_{\max}$</td>
    <td style="text-align: center;">100</td>
    <td style="text-align: center;">Initial noise level of $\sigma$ shown in Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma_{\min}$</td>
    <td style="text-align: center;">0.1</td>
    <td style="text-align: center;">Final noise level of $\sigma$ shown in Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma$ shown in Eq.(5)</td>
    <td style="text-align: center;">0.05</td>
    <td style="text-align: center;">Noise level for measearment.</td>
  </tr>
  <tr>
    <td style="text-align: center;">timestep</td>
    <td style="text-align: center;">poly-7</td>
    <td style="text-align: center;">Time-step discretization scheme, polynomial with $\rho = 7$.</td>
  </tr>
  <tr>
    <td style="text-align: center;">T</td>
    <td style="text-align: center;">200</td>
    <td style="text-align: center;">Inner loop of optimization steps shown in line 8 of Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">n</td>
    <td style="text-align: center;">5</td>
    <td style="text-align: center;">Denoising step of the PF-ODE in line 3 of Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">Cutoff-frequency schedule</td>
    <td style="text-align: center;">linear</td>
    <td style="text-align: center;">Coupled to the noise level, the start and end bounds are set to 0.4 and 1.0, respectively.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\lambda_k$ shown in Eq.17 </td>
    <td style="text-align: center;">Cosine schedule</td>
    <td style="text-align: center;">Starts at 0.35 and decays to 0. </td>
  </tr>
  <tr>
    <td style="text-align: center;">$w_{k,L}$ show in Eq.(16)</td>
    <td style="text-align: center;">1.0</td>
    <td style="text-align: center;">Weight for the low-frequency approximation subband, where a value of 1.0 means the refinement result is fully adopted.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$w_{k,H}$ show in Eq.(16)</td>
    <td style="text-align: center;">0.2</td>
    <td style="text-align: center;">Base weight for the high-frequency subband.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$d_s$ show in Eq.(16)</td>
    <td style="text-align: center;">0.05</td>
    <td style="text-align: center;">Initial value for detail unlocking.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$d_e$ show in Eq.(16)</td>
    <td style="text-align: center;">1.0</td>
    <td style="text-align: center;">Final value for detail unlocking.</td>
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
