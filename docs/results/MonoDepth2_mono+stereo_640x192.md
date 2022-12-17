<img src="../../docs/figs/logo2.png" align="right" width="34%">

# RoboDepth Benchmark
The following metrics are consistently used in our benchmark:
- Absolute Relative Difference: $\text{Abs Rel} = \frac{1}{|D|}\sum_{pred\in D}\frac{|gt - pred|}{gt}$
- Accuracy: $\delta_t = \frac{1}{|D|}|\{\ pred\in D | \max{(\frac{gt}{pred}, \frac{pred}{gt})< 1.25^t}\}| \times 100\\%$
- Depth Estimation Score (DES):
  - $\text{DES}_1 = \text{Abs Rel} - \delta_1 + 1$ 
  - $\text{DES}_2 = \frac{\text{Abs Rel} - \delta_1 + 1}{2}$
  - $\text{DES}_3 = \frac{\text{Abs Rel}}{\delta_1}$

### MonoDepth2, Mono+Stereo, 640x192
| Corruption | Clean | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG | 
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |          
| $\text{DES}_{1}$ | 0.232 | 0.255     | 0.810     | 0.301     | 0.588     | 1.071     | 0.398     | 0.895     | 0.692     | 0.564     | 0.408     | 0.256     | 0.407     | 1.154     | 1.210     | 1.121     | 1.258     | 0.271     | 0.358     |
| $\text{CE}_{1}$  |      -       | 0.985  | 1.441  | 0.971  | 1.063  | 1.046  | 1.067  | 1.838  | 1.430  | 1.291  | 1.015  | 0.992  | 1.057  | 1.503  | 1.555  | 1.646  | 1.623  | 0.938  | 0.916  |
| $\text{RCE}_{1}$ |      -       | 1.095 | 1.784 | 0.958 | 1.130 | 1.067 | 1.230 | 2.663 | 1.870 | 1.668 | 1.073 | 1.200 | 1.190 | 1.740 | 1.811 | 2.007 | 1.911 | 0.765 | 0.824 |
| $\text{DES}_{2}$ | 0.116 | 0.127     | 0.405     | 0.151     | 0.294     | 0.535     | 0.199     | 0.447     | 0.346     | 0.282     | 0.204     | 0.128     | 0.203     | 0.577     | 0.605     | 0.560     | 0.629     | 0.136     | 0.179     |
| $\text{CE}_{2}$  |      -       | 0.977  | 1.441  | 0.974  | 1.061  | 1.045  | 1.070  | 1.832  | 1.430  | 1.294  | 1.015  | 0.992  | 1.052  | 1.503  | 1.555  | 1.647  | 1.621  | 0.938  | 0.913  |
| $\text{RCE}_{2}$ |      -       | 1.000 | 1.784 | 0.972 | 1.127 | 1.066 | 1.239 | 2.648 | 1.870 | 1.677 | 1.073 | 1.200 | 1.176 | 1.740 | 1.811 | 2.009 | 1.907 | 0.769 | 0.818 |
| $\text{DES}_{3}$ | 0.121 | 0.131     | 0.610     | 0.154     | 0.347     | 1.208     | 0.205     | 0.755     | 0.446     | 0.324     | 0.217     | 0.131     | 0.210     | 1.547     | 1.875     | 1.399     | 2.292     | 0.142     | 0.184     |
| $\text{CE}_{3}$  |      -       | 0.936  | 1.843  | 0.933  | 1.061  | 1.136  | 1.030  | 2.786  | 1.652  | 1.356  | 0.982  | 0.936  | 1.005  | 2.808  | 3.342  | 3.158  | 4.122  | 0.899  | 0.856  |
| $\text{RCE}_{3}$ |      -       | 1.111 | 2.445 | 0.971 | 1.153 | 1.166 | 1.235 | 4.529 | 2.338 | 1.880 | 1.067 | 1.111 | 1.141 | 3.395 | 4.079 | 4.096 | 5.108 | 0.778 | 0.750 |

- **Summary:** $\text{mCE}_1 =$ 1.243, $\text{RmCE}_1 =$ 1.444, $\text{mCE}_2 =$ 1.242, $\text{RmCE}_2 =$ 1.438, $\text{mCE}_3 =$ 1.713, $\text{RmCE}_3 =$ 2.131



### Clean
| $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0.106 | 0.821 | 4.752 | 0.196 | 0.874 | 0.957 | 0.979 |

- **Summary:** $\text{DES}_1=$ 0.232, $\text{DES}_2=$ 0.116, $\text{DES}_3=$ 0.121




### Brightness
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.107 | 0.828 | 4.766 | 0.196 | 0.872 | 0.957 | 0.979 |
|   2   | 0.108 | 0.846 | 4.826 | 0.198 | 0.867 | 0.955 | 0.979 |
|   3   | 0.111 | 0.865 | 4.918 | 0.202 | 0.860 | 0.952 | 0.979 |
|   4   | 0.115 | 0.891 | 5.057 | 0.208 | 0.850 | 0.948 | 0.977 |
|   5   | 0.120 | 0.929 | 5.245 | 0.217 | 0.838 | 0.941 | 0.975 |
|  avg  | 0.112 | 0.872 | 4.962 | 0.204 | 0.857 | 0.951 | 0.978 |

- **Summary:** $\text{DES}_1=$ 0.255, $\text{DES}_2=$ 0.127, $\text{DES}_3=$ 0.131




### Dark
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.141 | 1.108 | 5.748 | 0.249 | 0.790 | 0.919 | 0.966 |
|   2   | 0.163 | 1.320 | 6.392 | 0.284 | 0.733 | 0.891 | 0.952 |
|   3   | 0.223 | 2.019 | 7.908 | 0.390 | 0.586 | 0.796 | 0.895 |
|   4   | 0.381 | 4.204 | 11.077 | 0.683 | 0.274 | 0.499 | 0.668 |
|   5   | 0.577 | 7.457 | 14.523 | 1.084 | 0.051 | 0.151 | 0.291 |
|  avg  | 0.297 | 3.222 | 9.130 | 0.538 | 0.487 | 0.651 | 0.754 |

- **Summary:** $\text{DES}_1=$ 0.810, $\text{DES}_2=$ 0.405, $\text{DES}_3=$ 0.610




### Fog
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.117 | 0.930 | 5.037 | 0.211 | 0.848 | 0.945 | 0.976 |
|   2   | 0.123 | 0.967 | 5.166 | 0.219 | 0.836 | 0.939 | 0.973 |
|   3   | 0.127 | 1.004 | 5.314 | 0.226 | 0.826 | 0.934 | 0.970 |
|   4   | 0.129 | 1.023 | 5.384 | 0.229 | 0.821 | 0.931 | 0.970 |
|   5   | 0.138 | 1.097 | 5.653 | 0.245 | 0.796 | 0.920 | 0.965 |
|  avg  | 0.127 | 1.004 | 5.311 | 0.226 | 0.825 | 0.934 | 0.971 |

- **Summary:** $\text{DES}_1=$ 0.301, $\text{DES}_2=$ 0.151, $\text{DES}_3=$ 0.154




### Frost
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.134 | 1.090 | 5.373 | 0.240 | 0.807 | 0.922 | 0.964 |
|   2   | 0.177 | 1.501 | 6.366 | 0.327 | 0.710 | 0.851 | 0.919 |
|   3   | 0.227 | 2.107 | 7.528 | 0.428 | 0.608 | 0.769 | 0.860 |
|   4   | 0.254 | 2.467 | 8.105 | 0.483 | 0.557 | 0.721 | 0.821 |
|   5   | 0.302 | 3.169 | 9.196 | 0.578 | 0.470 | 0.642 | 0.755 |
|  avg  | 0.219 | 2.067 | 7.314 | 0.411 | 0.630 | 0.781 | 0.864 |

- **Summary:** $\text{DES}_1=$ 0.588, $\text{DES}_2=$ 0.294, $\text{DES}_3=$ 0.347




### Snow
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.240 | 2.166 | 7.221 | 0.477 | 0.595 | 0.741 | 0.826 |
|   2   | 0.412 | 4.636 | 10.688 | 0.830 | 0.316 | 0.458 | 0.572 |
|   3   | 0.410 | 4.483 | 10.247 | 0.849 | 0.336 | 0.466 | 0.571 |
|   4   | 0.510 | 6.120 | 12.149 | 1.072 | 0.217 | 0.319 | 0.411 |
|   5   | 0.480 | 5.781 | 12.120 | 0.984 | 0.235 | 0.354 | 0.461 |
|  avg  | 0.410 | 4.637 | 10.485 | 0.842 | 0.340 | 0.468 | 0.568 |

- **Summary:** $\text{DES}_1=$ 1.071, $\text{DES}_2=$ 0.535, $\text{DES}_3=$ 1.208




### Contrast
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.112 | 0.892 | 4.934 | 0.204 | 0.858 | 0.951 | 0.978 |
|   2   | 0.117 | 0.928 | 5.063 | 0.211 | 0.846 | 0.946 | 0.976 |
|   3   | 0.128 | 1.010 | 5.386 | 0.228 | 0.822 | 0.934 | 0.971 |
|   4   | 0.167 | 1.429 | 6.809 | 0.290 | 0.725 | 0.886 | 0.947 |
|   5   | 0.252 | 2.917 | 10.189 | 0.455 | 0.535 | 0.746 | 0.855 |
|  avg  | 0.155 | 1.435 | 6.476 | 0.278 | 0.757 | 0.893 | 0.945 |

- **Summary:** $\text{DES}_1=$ 0.398, $\text{DES}_2=$ 0.199, $\text{DES}_3=$ 0.205




### Defocus Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.154 | 1.341 | 6.355 | 0.280 | 0.764 | 0.898 | 0.949 |
|   2   | 0.210 | 1.946 | 7.700 | 0.375 | 0.636 | 0.821 | 0.901 |
|   3   | 0.331 | 3.673 | 10.564 | 0.613 | 0.371 | 0.615 | 0.751 |
|   4   | 0.441 | 5.677 | 13.129 | 0.870 | 0.213 | 0.420 | 0.571 |
|   5   | 0.487 | 6.643 | 14.199 | 0.987 | 0.165 | 0.344 | 0.490 |
|  avg  | 0.325 | 3.856 | 10.389 | 0.625 | 0.430 | 0.620 | 0.732 |

- **Summary:** $\text{DES}_1=$ 0.895, $\text{DES}_2=$ 0.447, $\text{DES}_3=$ 0.755




### Glass_blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.135 | 1.174 | 5.920 | 0.242 | 0.806 | 0.922 | 0.966 |
|   2   | 0.162 | 1.495 | 6.829 | 0.291 | 0.739 | 0.886 | 0.945 |
|   3   | 0.248 | 2.620 | 9.161 | 0.443 | 0.532 | 0.747 | 0.859 |
|   4   | 0.296 | 3.388 | 10.452 | 0.540 | 0.435 | 0.661 | 0.793 |
|   5   | 0.397 | 5.170 | 12.862 | 0.756 | 0.264 | 0.487 | 0.641 |
|  avg  | 0.248 | 2.769 | 9.045 | 0.454 | 0.555 | 0.741 | 0.841 |

- **Summary:** $\text{DES}_1=$ 0.692, $\text{DES}_2=$ 0.346, $\text{DES}_3=$ 0.446




### Motion Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.123 | 1.006 | 5.427 | 0.224 | 0.833 | 0.937 | 0.972 |
|   2   | 0.145 | 1.229 | 6.199 | 0.263 | 0.780 | 0.910 | 0.958 |
|   3   | 0.197 | 1.877 | 7.668 | 0.357 | 0.661 | 0.836 | 0.911 |
|   4   | 0.267 | 2.816 | 9.289 | 0.491 | 0.515 | 0.723 | 0.829 |
|   5   | 0.312 | 3.533 | 10.343 | 0.583 | 0.437 | 0.646 | 0.765 |
|  avg  | 0.209 | 2.092 | 7.785 | 0.384 | 0.645 | 0.810 | 0.887 |

- **Summary:** $\text{DES}_1=$ 0.564, $\text{DES}_2=$ 0.282, $\text{DES}_3=$ 0.324




### Zoom Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.147 | 1.243 | 5.897 | 0.259 | 0.784 | 0.910 | 0.960 |
|   2   | 0.163 | 1.398 | 6.245 | 0.285 | 0.750 | 0.890 | 0.947 |
|   3   | 0.161 | 1.352 | 6.100 | 0.265 | 0.765 | 0.903 | 0.957 |
|   4   | 0.172 | 1.464 | 6.334 | 0.282 | 0.742 | 0.891 | 0.949 |
|   5   | 0.176 | 1.542 | 6.371 | 0.280 | 0.739 | 0.891 | 0.949 |
|  avg  | 0.164 | 1.400 | 6.189 | 0.274 | 0.756 | 0.897 | 0.952 |

- **Summary:** $\text{DES}_1=$ 0.408, $\text{DES}_2=$ 0.204, $\text{DES}_3=$ 0.217




### Elastic Transform
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.109 | 0.860 | 4.872 | 0.200 | 0.866 | 0.953 | 0.979 |
|   2   | 0.110 | 0.859 | 4.907 | 0.202 | 0.864 | 0.952 | 0.978 |
|   3   | 0.112 | 0.883 | 5.010 | 0.206 | 0.859 | 0.950 | 0.977 |
|   4   | 0.114 | 0.912 | 5.116 | 0.210 | 0.853 | 0.946 | 0.976 |
|   5   | 0.118 | 0.931 | 5.226 | 0.216 | 0.843 | 0.942 | 0.974 |
|  avg  | 0.113 | 0.889 | 5.026 | 0.207 | 0.857 | 0.949 | 0.977 |

- **Summary:** $\text{DES}_1=$ 0.256, $\text{DES}_2=$ 0.128, $\text{DES}_3=$ 0.131




### Color Quant
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.106 | 0.825 | 4.768 | 0.196 | 0.873 | 0.957 | 0.979 |
|   2   | 0.108 | 0.840 | 4.805 | 0.198 | 0.870 | 0.956 | 0.979 |
|   3   | 0.118 | 0.911 | 5.049 | 0.214 | 0.845 | 0.946 | 0.975 |
|   4   | 0.164 | 1.360 | 6.344 | 0.297 | 0.726 | 0.878 | 0.944 |
|   5   | 0.294 | 3.128 | 9.713 | 0.540 | 0.443 | 0.658 | 0.796 |
|  avg  | 0.158 | 1.413 | 6.136 | 0.289 | 0.751 | 0.879 | 0.935 |

- **Summary:** $\text{DES}_1=$ 0.407, $\text{DES}_2=$ 0.203, $\text{DES}_3=$ 0.210




### Gaussian Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.189 | 1.562 | 6.799 | 0.335 | 0.677 | 0.844 | 0.920 |
|   2   | 0.290 | 2.876 | 9.321 | 0.520 | 0.455 | 0.669 | 0.795 |
|   3   | 0.448 | 5.349 | 12.574 | 0.818 | 0.196 | 0.376 | 0.531 |
|   4   | 0.580 | 7.682 | 14.855 | 1.103 | 0.065 | 0.156 | 0.278 |
|   5   | 0.676 | 9.674 | 16.529 | 1.372 | 0.018 | 0.049 | 0.109 |
|  avg  | 0.437 | 5.429 | 12.016 | 0.830 | 0.282 | 0.419 | 0.527 |

- **Summary:** $\text{DES}_1=$ 1.154, $\text{DES}_2=$ 0.577, $\text{DES}_3=$ 1.547




### Impulse Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.227 | 2.097 | 8.180 | 0.399 | 0.582 | 0.782 | 0.884 |
|   2   | 0.340 | 3.680 | 10.760 | 0.600 | 0.344 | 0.575 | 0.728 |
|   3   | 0.430 | 5.071 | 12.443 | 0.770 | 0.200 | 0.404 | 0.570 |
|   4   | 0.575 | 7.511 | 14.726 | 1.078 | 0.057 | 0.153 | 0.285 |
|   5   | 0.674 | 9.544 | 16.424 | 1.349 | 0.015 | 0.043 | 0.105 |
|  avg  | 0.449 | 5.581 | 12.507 | 0.839 | 0.240 | 0.391 | 0.514 |

- **Summary:** $\text{DES}_1=$ 1.210, $\text{DES}_2=$ 0.605, $\text{DES}_3=$ 1.875




### Shot Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.149 | 1.114 | 5.921 | 0.252 | 0.768 | 0.919 | 0.968 |
|   2   | 0.251 | 2.274 | 8.489 | 0.419 | 0.510 | 0.746 | 0.871 |
|   3   | 0.432 | 4.946 | 12.130 | 0.757 | 0.189 | 0.395 | 0.569 |
|   4   | 0.612 | 8.102 | 15.156 | 1.151 | 0.035 | 0.098 | 0.204 |
|   5   | 0.676 | 9.539 | 16.393 | 1.345 | 0.013 | 0.039 | 0.094 |
|  avg  | 0.424 | 5.195 | 11.618 | 0.785 | 0.303 | 0.439 | 0.541 |

- **Summary:** $\text{DES}_1=$ 1.121, $\text{DES}_2=$ 0.560, $\text{DES}_3=$ 1.399




### ISO Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.309 | 3.088 | 9.744 | 0.529 | 0.394 | 0.636 | 0.784 |
|   2   | 0.364 | 3.936 | 10.910 | 0.638 | 0.301 | 0.527 | 0.690 |
|   3   | 0.448 | 5.286 | 12.520 | 0.804 | 0.180 | 0.369 | 0.534 |
|   4   | 0.539 | 6.873 | 14.129 | 0.997 | 0.089 | 0.213 | 0.358 |
|   5   | 0.630 | 8.609 | 15.630 | 1.223 | 0.035 | 0.090 | 0.183 |
|  avg  | 0.458 | 5.558 | 12.587 | 0.838 | 0.200 | 0.367 | 0.510 |

- **Summary:** $\text{DES}_1=$ 1.258, $\text{DES}_2=$ 0.629, $\text{DES}_3=$ 2.292




### Pixelate
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.111 | 0.878 | 4.854 | 0.197 | 0.869 | 0.955 | 0.980 |
|   2   | 0.112 | 0.895 | 4.926 | 0.200 | 0.866 | 0.954 | 0.979 |
|   3   | 0.117 | 0.931 | 5.039 | 0.204 | 0.857 | 0.950 | 0.978 |
|   4   | 0.128 | 1.035 | 5.388 | 0.219 | 0.834 | 0.941 | 0.975 |
|   5   | 0.133 | 1.078 | 5.628 | 0.229 | 0.820 | 0.934 | 0.972 |
|  avg  | 0.120 | 0.963 | 5.167 | 0.210 | 0.849 | 0.947 | 0.977 |

- **Summary:** $\text{DES}_1=$ 0.271, $\text{DES}_2=$ 0.136, $\text{DES}_3=$ 0.142




### JPEG Compression
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.118 | 0.964 | 5.139 | 0.212 | 0.848 | 0.946 | 0.976 |
|   2   | 0.126 | 1.034 | 5.291 | 0.222 | 0.830 | 0.939 | 0.973 |
|   3   | 0.132 | 1.076 | 5.394 | 0.230 | 0.815 | 0.932 | 0.971 |
|   4   | 0.157 | 1.280 | 5.882 | 0.269 | 0.756 | 0.902 | 0.957 |
|   5   | 0.189 | 1.591 | 6.529 | 0.320 | 0.683 | 0.856 | 0.932 |
|  avg  | 0.144 | 1.189 | 5.647 | 0.251 | 0.786 | 0.915 | 0.962 |

- **Summary:** $\text{DES}_1=$ 0.358, $\text{DES}_2=$ 0.179, $\text{DES}_3=$ 0.184


