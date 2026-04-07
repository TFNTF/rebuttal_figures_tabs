# Rebuttal_figures_tabs


## Table 1. Quantitative Results for High-pass Operator (Motion_deblurring, 256 * 256)  
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
    <td style="text-align: center;">High-pass  (start bound of cutoff-frequency schedule is 0.8)</td>
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

## Table 2. Ablation Studies for Different Wavelets (Motion_deblurring, 256 * 256)
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
    <td style="text-align: center;">Ours (Haar)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">34.70</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.155</td>
  </tr>
</table>
Table 2 shows that Haar achieves better performance in our method than the other two selected wavelet bases, supporting the effectiveness of our design choice.

## Figure 1. Qualitative Results for Different Wavelets (Motion_deblurring, 256 * 256)

Figure 1 shows that Haar is the most effective wavelet basis for our method, producing fewer artifacts and higher-quality coarse and fine features.

![wave_1](figures/wave_1.png)
![wave_2](figures/wave_2.png)

## Table 3. Computational Cost for Compared Methods (Motion_deblurring, 256 * 256)
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

## Table 4. Quantitative Results Under The Same Computational Budget* (Motion_deblurring On FFHQ, 256 * 256)
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
    <td style="text-align: center;">Ours (N=9 & T=90)</td>
    <td style="text-align: center;">27.31</td>
    <td style="text-align: center;">0.603</td>
    <td style="text-align: center;">0.264</td>
    <td style="text-align: center;">~2</td>
  </tr>
</table>
* indicates that, for this experiment, we compare only with methods that are more efficient and provide publicly available official code for this task. We further set N=9 and T=90 to ensure a matched time budget.

Table 4 shows that, under the same compute budget (i.e., time cost), our method outperforms the two fastest baseline methods. Moreover, even when compared with FlowDPS, which is built on a base model trained with flow matching, our method still achieves better performance.

## Figure 2. Qualitative Results for Real-world Blur According to BlindDPS (Motion_deblurring, 256*256)

![real_1](figures/real_1.png)
![real_2](figures/real_2.png)

Figure 2 shows that our method remains robust under nonlinear/real-world blur, and still outperforms the compared baseline.

## Table 5. Qualitative Results for Real-world Blur According to BlindDPS (Motion_deblurring, 256 * 256)
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

For real-world blur, we follow BlindDPS [1]. Table 5 demonstrates our method’s ability to handle real-world blur. On real-world motion blur, our method still substantially outperforms BlindDPS on both FFHQ and ImageNet, indicating that its effectiveness extends beyond matched synthetic settings.

[1] Chung, Hyungjin, et al. Parallel diffusion models of operator and image for blind inverse problems. CVPR, 2023.

## Table 6. Quantitative Results for Operator Mismatch (Motion_deblurring On FFHQ 256 * 256)
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
    <td style="text-align: center;">15.20</td>
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
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
  </tr>
</table>

Table 6 shows that our method cannot produce satisfactory results under operator mismatch, where the estimated and ground-truth images are evaluated using different forward operators A. Specifically, the observation is generated by the true blur operator $A_\text{true}$ (kernel size 61, intensity 0.5), while reconstruction is performed using a perturbed operator $A_\text{mismatch}$ (e.g., kernel size 61, intensity 0.65). Accordingly, under the setting of Eq.(13), the measurement-related first term on the right-hand side of Eq.(12) is computed as $\lVert A_\text{mismatch}(\hat{x_\text{0}})-A_\text{true}(x_\text{gt}) \rVert_2^2$, where $\hat{x_\text{0}}$ and $x_\text{gt}$ denote the estimated image and the ground-truth image, respectively. In this case, the sampler no longer targets the correct posterior $p(\hat{x_\text{0}}\mid y;A_\text{true})$, but instead a biased posterior induced by the misspecified likelihood.

## Table 7. Abaltion Studies of Full-band Strategy (FFHQ 256*256)
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
    <td style="text-align: center;">Ours (Freq. & Haar)</td>
    <td style="text-align: center;">31.88</td>
    <td style="text-align: center;">0.890</td>
    <td style="text-align: center;">0.090</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
  </tr>
</table>

Table 7 presents the quantitative comparison between our full method and its variants without Haar or without frequency continuation, demonstrating the effectiveness of our design.

## Figure 3. Qualitative Results for Ablation Studies (256 * 256)

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

Table 8 reports the quantitative comparison between our method and the baselines. For box inpainting, the gain of our method is expected to be smaller than in deblurring or super-resolution. Under a contiguous box mask, the measurement only constrains the visible context, while the masked operator mixes frequencies in Fourier space; as a result, the low-pass residual mainly regularizes visible-region consistency and boundary compatibility, rather than revealing the true structure of the missing region. In this regime, Haar Fusion cannot create missing semantics and can only prevent premature commitment to unreliable details. Nevertheless, NFC still maintains competitive performance.

## Figure 4. Qualitative Results for Box-inpainting (256 * 256)

![box_1](figures/box_1.png)
![box_2](figures/box_2.png)

Figure 4 shows that, for the box inpainting task, our method preserves the unmasked content while generating plausible completions for the masked region.

## Table 9. Ablation Studies of Measurement-consistency Updates with Different Strengths Across Frequency Components (Motion_deblurring, 256 * 256)
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
    <td style="text-align: center;">Ours (w/o. Haar & Measurement-consistency Updates with Different Strengths Across Frequency Components)</td>
    <td style="text-align: center;">14.88</td>
    <td style="text-align: center;">0.179</td>
    <td style="text-align: center;">0.583</td>
    <td style="text-align: center;">15.02</td>
    <td style="text-align: center;">0.244</td>
    <td style="text-align: center;">0.482</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (Full: Haar & Freq.)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">34.70</td>
    <td style="text-align: center;">0.935</td>
  <td style="text-align: center;">0.155</td>
  </tr>
</table>

Table 9 demonstrates the effectiveness of Haar. The results show that it cannot be replaced by measurement-consistency updates with different strengths across frequency components. The results show that the weights assigned to different frequency components cannot be chosen arbitrarily, as they may significantly affect performance.

## Table 10. Quantitative Comparison of Different Noise Schedule (N) (Motion_deblurring On FFHQ 256 * 256)
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

Table 10 shows how the quantitative performance varies with the number of noise-schedule steps N. The results indicate that our method continues to benefit from increasing N, although this also incurs higher time cost. We therefore choose N=200 as a trade-off between efficiency and generation quality.

## Table 11. Quantitative Comparison of Different Optimization Steps (T) (Motion_deblurring On FFHQ 256 * 256)
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

Table 11 shows how the quantitative performance varies with the number of optimization steps T. The results indicate that our method continues to benefit from increasing T, although this also leads to higher time cost. We therefore choose T=200 as a trade-off between efficiency and generation quality.

## Table 12. Quantitative Comparison of Different $\sigma$ of Eq.(5) (Motion_deblurring On FFHQ 256 * 256)
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

Table 12 reflects how the quantitative performance varies with the value of $\sigma$. To maintain fair competition, $\sigma$ is set to 0.05 in our method.

## Table 13. Quantitative Results of Other Parameters (Motion_deblurring On FFHQ 256 * 256)
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

We vary the remaining parameters as shown in Table 15 to verify the effectiveness of the adopted settings. The results show that the default configuration of Table 15 achieves the best performance.

## Figure 5. Qualitative Comparison Between DPS (1000 Steps) and Ours on FFHQ 256 * 256

![dps_1](figures/comp_dps_1.png)
![dps_2](figures/comp_dps_2.png)

Our method significantly outperforms DPS (strength=0.3/0.5 (i.e., step size in Appendix C of DPS)) in both coarse and fine semantics.

## Figure 6. Qualitative Comparison Between SILO (512 * 512) and Ours (256 * 256) on FFHQ 

![silo](figures/silo.png)

Since SILO is based on Stable Diffusion and generates images at a resolution of 512 * 512, whereas our method operates at 256 * 256, we present the qualitative comparison separately to avoid confounding the visual results with the resolution difference.

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
    <td style="text-align: center;">SILO (512 * 512)</td>
    <td style="text-align: center;">26.53</td>
    <td style="text-align: center;">0.745</td>
    <td style="text-align: center;">0.317</td>
    <td style="text-align: center;">26.79</td>
    <td style="text-align: center;">0.761</td>
    <td style="text-align: center;">0.297</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (256 * 256)</td>
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

## Table 16. Quantitative Comparison of Different Noise Schedule (N) and Optimization Steps (T) (Motion_deblurring On FFHQ 256 * 256)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Values of N and T: (N, T)</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">FFHQ</th>
    <th rowspan="2" style="text-align: center; white-space: nowrap;">Efficiency (s/img)</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">(50, 200)</td>
    <td style="text-align: center;">35.82</td>
    <td style="text-align: center;">0.924</td>
    <td style="text-align: center;">0.069</td>
    <td style="text-align: center;">~35</td>
  </tr>
  <tr>
    <td style="text-align: center;">(100, 200)</td>
    <td style="text-align: center;">36.28</td>
    <td style="text-align: center;">0.935</td>
    <td style="text-align: center;">0.055</td>
    <td style="text-align: center;">~65</td>
  </tr>
  <tr>
    <td style="text-align: center;">(300, 200)</td>
    <td style="text-align: center;">37.08</td>
    <td style="text-align: center;">0.953</td>
    <td style="text-align: center;">0.039</td>
    <td style="text-align: center;">~195</td>
  </tr>
  <tr>
    <td style="text-align: center;">(500, 200)</td>
    <td style="text-align: center;">37.04</td>
    <td style="text-align: center;">0.949</td>
    <td style="text-align: center;">0.046</td>
    <td style="text-align: center;">~280</td>
  </tr>
   <tr>
    <td style="text-align: center;">(200, 50)</td>
    <td style="text-align: center;">35.81</td>
    <td style="text-align: center;">0.943</td>
    <td style="text-align: center;">0.047</td>
    <td style="text-align: center;">~70</td>
  </tr>
  <tr>
    <td style="text-align: center;">(200, 100)</td>
    <td style="text-align: center;">36.86</td>
    <td style="text-align: center;">0.945</td>
    <td style="text-align: center;">0.050</td>
    <td style="text-align: center;">~110</td>
  </tr>
  <tr>
    <td style="text-align: center;">(200, 300)</td>
    <td style="text-align: center;">36.95</td>
    <td style="text-align: center;">0.950</td>
    <td style="text-align: center;">0.041</td>
    <td style="text-align: center;">~160</td>
  </tr>
  <tr>
    <td style="text-align: center;">(200, 500)</td>
    <td style="text-align: center;">35.80</td>
    <td style="text-align: center;">0.913</td>
    <td style="text-align: center;">0.075</td>
    <td style="text-align: center;">~215</td>
  </tr>
  <tr>
    <td style="text-align: center;">(300, 100)</td>
    <td style="text-align: center;">35.34</td>
    <td style="text-align: center;">0.938</td>
    <td style="text-align: center;">0.053</td>
    <td style="text-align: center;">~175</td>
  </tr>
  <tr>
    <td style="text-align: center;">(400, 50)</td>
    <td style="text-align: center;">35.84</td>
    <td style="text-align: center;">0.943</td>
    <td style="text-align: center;">0.046</td>
    <td style="text-align: center;">~200</td>
  </tr>
  <tr>
    <td style="text-align: center;">(500, 25)</td>
    <td style="text-align: center;">36.40</td>
    <td style="text-align: center;">0.950</td>
    <td style="text-align: center;">0.040</td>
    <td style="text-align: center;">~240</td>
  </tr>
  <tr>
    <td style="text-align: center;">(300, 300)</td>
    <td style="text-align: center;">36.97</td>
    <td style="text-align: center;">0.948</td>
    <td style="text-align: center;">0.047</td>
    <td style="text-align: center;">~225</td>
  </tr>
  <tr>
    <td style="text-align: center;">(400, 400)</td>
    <td style="text-align: center;">36.80</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">~320</td>
  </tr>
  <tr>
    <td style="text-align: center;">(500, 500)</td>
    <td style="text-align: center;">36.41</td>
    <td style="text-align: center;">0.928</td>
    <td style="text-align: center;">0.063</td>
    <td style="text-align: center;">~425</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (200, 200)</td>
    <td style="text-align: center;">36.69</td>
    <td style="text-align: center;">0.940</td>
    <td style="text-align: center;">0.054</td>
    <td style="text-align: center;">~130</td>
  </tr>
</table>

We have list the quantitative results on FFHQ 256 * 256 for different combinations of N and T. And the other parameters settings are the same with those of Table 15. We have also clarified the interaction between N and T in the rebuttal according to this Table.

## Table 17. Quantitative Comparison of Different $\sigma$ of Eq.(5) (Gaussian_deblurring On FFHQ)
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
    <td style="text-align: center;">Ours (0, 256 * 256)</td>
    <td style="text-align: center;">32.55</td>
    <td style="text-align: center;">0.876</td>
    <td style="text-align: center;">0.163</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (0.03, 256 * 256)</td>
    <td style="text-align: center;">30.62</td>
    <td style="text-align: center;">0.843</td>
    <td style="text-align: center;">0.172</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (0.05, 256 * 256)</td>
    <td style="text-align: center;">29.99</td>
    <td style="text-align: center;">0.821</td>
    <td style="text-align: center;">0.175</td>
  </tr>

  <tr>
    <td style="text-align: center;">Ours (0.07, 256 * 256)</td>
    <td style="text-align: center;">29.02</td>
    <td style="text-align: center;">0.817</td>
    <td style="text-align: center;">0.175</td>
  </tr>
  <tr>
    <td style="text-align: center;">SILO (0, 512 * 512)</td>
    <td style="text-align: center;">26.59</td>
    <td style="text-align: center;">0.825</td>
    <td style="text-align: center;">0.311</td>
  </tr>
  <tr>
    <td style="text-align: center;">SILO (0.03, 512 * 512)</td>
    <td style="text-align: center;">26.59</td>
    <td style="text-align: center;">0.825</td>
    <td style="text-align: center;">0.311</td>
  </tr>
  <tr>
    <td style="text-align: center;">SILO (0.05, 512 * 512)</td>
    <td style="text-align: center;">26.58</td>
    <td style="text-align: center;">0.825</td>
    <td style="text-align: center;">0.311</td>
  </tr>
  <tr>
    <td style="text-align: center;">SILO (0.07, 512 * 512)</td>
    <td style="text-align: center;">26.57</td>
    <td style="text-align: center;">0.824</td>
    <td style="text-align: center;">0.312</td>
  </tr>
  <tr>
    <td style="text-align: center;">Resample (0, 256 * 256)</td>
    <td style="text-align: center;">27.26</td>
    <td style="text-align: center;">0.751</td>
    <td style="text-align: center;">0.250</td>
  </tr>
  <tr>
    <td style="text-align: center;">Resample (0.03, 256 * 256)</td>
    <td style="text-align: center;">25.98</td>
    <td style="text-align: center;">0.661</td>
    <td style="text-align: center;">0.301</td>
  </tr>
  <tr>
    <td style="text-align: center;">Resample (0.05, 256 * 256)</td>
    <td style="text-align: center;">25.33</td>
    <td style="text-align: center;">0.611</td>
    <td style="text-align: center;">0.332</td>
  </tr>
  <tr>
    <td style="text-align: center;">Resample (0.07, 256 * 256)</td>
    <td style="text-align: center;">24.57</td>
    <td style="text-align: center;">0.552</td>
    <td style="text-align: center;">0.375</td>
  </tr>
</table>

Table 17 shows that our method consistently achieves the best performance across different values of $\sigma$ in Eq.(5).

## Figure 7. Qualitative Comparison Between DPS (strength=1 (i.e., step size in Appendix C of DPS [2])) and Ours on FFHQ 256 * 256

![s1](figures/s1.png)

[2] Chung, Hyungjin, et al. Diffusion posterior sampling for general noisy inverse problems. ICLR, 2023.


## Table 18. Quantitative Comparison Between SILO and Ours on FFHQ* (512 * 512)
<table>
  <tr>
    <th rowspan="2" style="text-align: center;">Methods</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Gaussian Deblurring</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Super-resolution</th>
    <th colspan="3" style="text-align: center; white-space: nowrap;">Box Inpainting</th>
  </tr>
  <tr>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
    <th style="text-align: center; white-space: nowrap;">PSNR ↑</th>
    <th style="text-align: center; white-space: nowrap;">SSIM ↑</th>
    <th style="text-align: center; white-space: nowrap;">LPIPS ↓</th>
  </tr>
  <tr>
    <td style="text-align: center;">SILO (512 * 512)</td>
    <td style="text-align: center;">26.53</td>
    <td style="text-align: center;">0.745</td>
    <td style="text-align: center;">0.317</td>
    <td style="text-align: center;">26.79</td>
    <td style="text-align: center;">0.761</td>
    <td style="text-align: center;">0.297</td>
    <td style="text-align: center;">22.73</td>
    <td style="text-align: center;">0.782</td>
    <td style="text-align: center;">0.237</td>
  </tr>
  <tr>
    <td style="text-align: center;">Ours (512 * 512)</td>
    <td style="text-align: center;">27.29</td>
    <td style="text-align: center;">0.762</td>
    <td style="text-align: center;">0.232</td>
    <td style="text-align: center;">28.04</td>
    <td style="text-align: center;">0.803</td>
    <td style="text-align: center;">0.177</td>
    <td style="text-align: center;">22.62</td>
    <td style="text-align: center;">0.785</td>
    <td style="text-align: center;">0.232</td>
  </tr>
</table>

* indicates that, based on the publicly available SILO codebase, only Gaussian deblurring and super-resolution on the FFHQ dataset are supported. 

Table 18 reports the quantitative comparison between SILO and our method under the same resolution setting, both based on Stable Diffusion v1.5. Compared with the quantitative results in pixel space, we believe that Langevin sampling in latent space is more susceptible to the combined effects of posterior geometry, decoder distortion, representation bottlenecks, and text conditioning. We will explore alternative optimization strategies in future work to further improve the performance of our method. For box inpainting, the gain of our method is expected to be smaller than in deblurring or super-resolution. Under a contiguous box mask, the measurement only constrains the visible context, while the masked operator mixes frequencies in Fourier space; as a result, the low-pass residual mainly regularizes visible-region consistency and boundary compatibility, rather than revealing the true structure of the missing region. In this regime, Haar Fusion cannot create missing semantics and can only prevent premature commitment to unreliable details. Nevertheless, our method still maintains competitive performance.

## Figure 8. Qualitative Comparison Between SILO and Ours on FFHQ 512 * 512

![silo2](figures/silo_2.png)

## Table 19. Parameters Config of Our Method Based on Stable-diffusion-v1.5 (512 * 512)
<table>
  <tr>
    <th style="text-align: center;">Parameter</th>
    <th style="text-align: center; white-space: nowrap;">Default</th>
    <th style="text-align: center;">Description</th>
  </tr>
  <tr>
    <td style="text-align: center;">N</td>
    <td style="text-align: center;">100</td>
    <td style="text-align: center;">Number of noise schedule of line 2 in Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma_{\max}$</td>
    <td style="text-align: center;">10</td>
    <td style="text-align: center;">Initial noise level of the noise scheduler.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma_{\min}$</td>
    <td style="text-align: center;">0.001</td>
    <td style="text-align: center;">Final noise level of the noise scheduler.</td>
  </tr>
  <tr>
    <td style="text-align: center;">timestep</td>
    <td style="text-align: center;">poly-7</td>
    <td style="text-align: center;">Time-step discretization scheme of the noise scheduler.</td>
  </tr>

  <tr>
    <td style="text-align: center;">n</td>
    <td style="text-align: center;">5</td>
    <td style="text-align: center;">Number of PF-ODE / diffusion steps in the diffusion reverse process.</td>
  </tr>
  <tr>
    <td style="text-align: center;">timestep (diffusion)</td>
    <td style="text-align: center;">poly-7</td>
    <td style="text-align: center;">Time-step discretization scheme of the diffusion scheduler.</td>
  </tr>
  <tr>
    <td style="text-align: center;">T</td>
    <td style="text-align: center;">130</td>
    <td style="text-align: center;">Number of optimization steps of line 8 in Alg.1.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\sigma$ shown in Eq.(5)</td>
    <td style="text-align: center;">0.02</td>
    <td style="text-align: center;">Measurement noise level.</td>
  </tr>
  <tr>
    <td style="text-align: center;">Guidance scale</td>
    <td style="text-align: center;">7.5</td>
    <td style="text-align: center;">Classifier-free guidance scale of Stable Diffusion.</td>
  </tr>
  <tr>
    <td style="text-align: center;">Prompt</td>
    <td style="text-align: center;">a natural looking image</td>
    <td style="text-align: center;">Text prompt used by the Stable Diffusion prior.</td>
  </tr>

  <tr>
    <td style="text-align: center;">Cutoff-frequency schedule</td>
    <td style="text-align: center;">linear</td>
    <td style="text-align: center;">Frequency-exposure schedule in the SD sampler, with start and end bounds set to 0.25 and 1.0, respectively.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$\lambda_k$ shown in Eq.(17)</td>
    <td style="text-align: center;">Cosine schedule</td>
    <td style="text-align: center;">Blending weight schedule for frequency guidance, starting from 0.6 and decaying to 0.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$w_{k,L}$ show in Eq.(16)</td>
    <td style="text-align: center;">1.0</td>
    <td style="text-align: center;">Weight for the low-frequency approximation subband, where a value of 1.0 means the refinement result is fully adopted.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$w_{k,H}$ show in Eq.(16)</td>
    <td style="text-align: center;">0.12</td>
    <td style="text-align: center;">Base weight for the high-frequency subband.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$d_s$ show in Eq.(16)</td>
    <td style="text-align: center;">0.0</td>
    <td style="text-align: center;">Initial value of detail unlocking in the wavelet fusion module.</td>
  </tr>
  <tr>
    <td style="text-align: center;">$d_e$ show in Eq.(16)</td>
    <td style="text-align: center;">1.0</td>
    <td style="text-align: center;">Final value of detail unlocking in the wavelet fusion module.</td>
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
