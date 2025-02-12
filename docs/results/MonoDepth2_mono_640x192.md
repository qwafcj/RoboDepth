<img src="../../figs/logo2.png" align="right" width="34%">

# RoboDepth Benchmark
The following metrics are consistently used in our benchmark:
- Absolute Relative Difference: $\text{Abs Rel} = \frac{1}{|D|}\sum_{pred\in D}\frac{|gt - pred|}{gt}$
- Accuracy: $\delta_t = \frac{1}{|D|}|\{\ pred\in D | \max{(\frac{gt}{pred}, \frac{pred}{gt})< 1.25^t}\}| \times 100\\%$
- Depth Estimation Score (DES):
  - $\text{DES}_1 = \text{Abs Rel} - \delta_1 + 1$ 
  - $\text{DES}_2 = \frac{\text{Abs Rel} - \delta_1 + 1}{2}$
  - $\text{DES}_3 = \frac{\text{Abs Rel}}{\delta_1}$



### MonoDepth2, Mono, 640x192
| Corruption | Clean | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG | 
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |          
| $\text{DES}_{1}$ | 0.238 | 0.259     | 0.561     | 0.311     | 0.553     | 1.023     | 0.373     | 0.487     | 0.484     | 0.433     | 0.402     | 0.258     | 0.386     | 0.768     | 0.779     | 0.681     | 0.776     | 0.289     | 0.391     |
| $\text{CE}_{1}$  |      -       | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  |
| $\text{RCE}_{1}$ |      -       | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |
| $\text{DES}_{2}$ | 0.119 | 0.130     | 0.280     | 0.155     | 0.277     | 0.511     | 0.187     | 0.244     | 0.242     | 0.216     | 0.201     | 0.129     | 0.193     | 0.384     | 0.389     | 0.340     | 0.388     | 0.145     | 0.196     |
| $\text{CE}_{2}$  |      -       | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  |
| $\text{RCE}_{2}$ |      -       | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |
| $\text{DES}_{3}$ | 0.131 | 0.140     | 0.330     | 0.166     | 0.327     | 1.058     | 0.199     | 0.271     | 0.270     | 0.236     | 0.221     | 0.141     | 0.209     | 0.551     | 0.563     | 0.442     | 0.557     | 0.158     | 0.215     |
| $\text{CE}_{3}$  |      -       | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  | 1.000  |
| $\text{RCE}_{3}$ |      -       | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 | 1.000 |

- **Summary:** $\text{mCE}_1 =$ 1.000, $\text{RmCE}_1 =$ 1.000, $\text{mCE}_2 =$ 1.000, $\text{RmCE}_2 =$ 1.000, $\text{mCE}_3 =$ 1.000, $\text{RmCE}_3 =$ 1.000


### Clean
| $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0.115 | 0.905 | 4.864 | 0.193 | 0.877 | 0.959 | 0.981 |

- **Summary:** $\text{DES}_1=$ 0.238, $\text{DES}_2=$ 0.119, $\text{DES}_3=$ 0.131




### Brightness
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.115 | 0.905 | 4.860 | 0.193 | 0.876 | 0.959 | 0.981 |
|   2   | 0.117 | 0.923 | 4.901 | 0.195 | 0.870 | 0.958 | 0.981 |
|   3   | 0.120 | 0.939 | 4.963 | 0.198 | 0.863 | 0.956 | 0.980 |
|   4   | 0.123 | 0.953 | 5.046 | 0.202 | 0.853 | 0.953 | 0.980 |
|   5   | 0.127 | 0.960 | 5.138 | 0.207 | 0.844 | 0.951 | 0.979 |
|  avg  | 0.120 | 0.936 | 4.982 | 0.199 | 0.861 | 0.955 | 0.980 |

- **Summary:** $\text{DES}_1=$ 0.259, $\text{DES}_2=$ 0.130, $\text{DES}_3=$ 0.140




### Dark
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.149 | 1.190 | 5.683 | 0.230 | 0.806 | 0.936 | 0.973 |
|   2   | 0.164 | 1.299 | 6.037 | 0.248 | 0.771 | 0.923 | 0.968 |
|   3   | 0.194 | 1.534 | 6.667 | 0.282 | 0.700 | 0.897 | 0.957 |
|   4   | 0.249 | 2.050 | 7.863 | 0.347 | 0.569 | 0.840 | 0.932 |
|   5   | 0.323 | 2.926 | 9.527 | 0.432 | 0.428 | 0.742 | 0.889 |
|  avg  | 0.216 | 1.800 | 7.155 | 0.308 | 0.655 | 0.868 | 0.944 |

- **Summary:** $\text{DES}_1=$ 0.561, $\text{DES}_2=$ 0.280, $\text{DES}_3=$ 0.330




### Fog
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.128 | 1.036 | 5.203 | 0.209 | 0.846 | 0.949 | 0.978 |
|   2   | 0.132 | 1.069 | 5.331 | 0.215 | 0.839 | 0.947 | 0.976 |
|   3   | 0.137 | 1.098 | 5.466 | 0.220 | 0.827 | 0.942 | 0.975 |
|   4   | 0.139 | 1.096 | 5.502 | 0.223 | 0.822 | 0.941 | 0.975 |
|   5   | 0.149 | 1.181 | 5.727 | 0.235 | 0.798 | 0.933 | 0.972 |
|  avg  | 0.137 | 1.096 | 5.446 | 0.220 | 0.826 | 0.942 | 0.975 |

- **Summary:** $\text{DES}_1=$ 0.311, $\text{DES}_2=$ 0.155, $\text{DES}_3=$ 0.166




### Frost
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.149 | 1.224 | 5.518 | 0.227 | 0.805 | 0.937 | 0.974 |
|   2   | 0.192 | 1.648 | 6.351 | 0.276 | 0.714 | 0.899 | 0.957 |
|   3   | 0.230 | 2.106 | 7.127 | 0.314 | 0.633 | 0.863 | 0.942 |
|   4   | 0.243 | 2.282 | 7.333 | 0.327 | 0.611 | 0.850 | 0.936 |
|   5   | 0.272 | 2.560 | 7.765 | 0.356 | 0.556 | 0.820 | 0.923 |
|  avg  | 0.217 | 1.964 | 6.819 | 0.300 | 0.664 | 0.874 | 0.946 |

- **Summary:** $\text{DES}_1=$ 0.553, $\text{DES}_2=$ 0.277, $\text{DES}_3=$ 0.327




### Snow
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.265 | 2.786 | 7.380 | 0.359 | 0.593 | 0.818 | 0.911 |
|   2   | 0.409 | 5.183 | 10.302 | 0.481 | 0.372 | 0.666 | 0.841 |
|   3   | 0.444 | 6.263 | 11.051 | 0.507 | 0.353 | 0.635 | 0.818 |
|   4   | 0.504 | 7.673 | 12.456 | 0.555 | 0.304 | 0.573 | 0.776 |
|   5   | 0.449 | 5.969 | 11.141 | 0.519 | 0.335 | 0.619 | 0.810 |
|  avg  | 0.414 | 5.575 | 10.466 | 0.484 | 0.391 | 0.662 | 0.831 |

- **Summary:** $\text{DES}_1=$ 1.023, $\text{DES}_2=$ 0.511, $\text{DES}_3=$ 1.058




### Contrast
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.123 | 0.994 | 5.082 | 0.203 | 0.860 | 0.954 | 0.979 |
|   2   | 0.127 | 1.027 | 5.213 | 0.209 | 0.848 | 0.950 | 0.977 |
|   3   | 0.138 | 1.092 | 5.505 | 0.223 | 0.824 | 0.941 | 0.975 |
|   4   | 0.169 | 1.341 | 6.528 | 0.266 | 0.752 | 0.909 | 0.961 |
|   5   | 0.222 | 2.078 | 8.676 | 0.352 | 0.629 | 0.841 | 0.920 |
|  avg  | 0.156 | 1.306 | 6.201 | 0.251 | 0.783 | 0.919 | 0.962 |

- **Summary:** $\text{DES}_1=$ 0.373, $\text{DES}_2=$ 0.187, $\text{DES}_3=$ 0.199




### Defocus Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.152 | 1.283 | 6.179 | 0.246 | 0.797 | 0.926 | 0.965 |
|   2   | 0.171 | 1.449 | 6.712 | 0.274 | 0.751 | 0.907 | 0.956 |
|   3   | 0.195 | 1.687 | 7.480 | 0.311 | 0.689 | 0.879 | 0.941 |
|   4   | 0.213 | 1.930 | 8.241 | 0.338 | 0.651 | 0.854 | 0.928 |
|   5   | 0.223 | 2.118 | 8.769 | 0.356 | 0.630 | 0.839 | 0.919 |
|  avg  | 0.191 | 1.693 | 7.476 | 0.305 | 0.704 | 0.881 | 0.942 |

- **Summary:** $\text{DES}_1=$ 0.487, $\text{DES}_2=$ 0.244, $\text{DES}_3=$ 0.271




### Glass Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.142 | 1.282 | 5.902 | 0.227 | 0.824 | 0.938 | 0.972 |
|   2   | 0.161 | 1.457 | 6.483 | 0.253 | 0.785 | 0.921 | 0.963 |
|   3   | 0.202 | 1.838 | 7.487 | 0.303 | 0.684 | 0.885 | 0.946 |
|   4   | 0.215 | 1.920 | 7.935 | 0.325 | 0.647 | 0.866 | 0.936 |
|   5   | 0.236 | 2.187 | 8.736 | 0.361 | 0.596 | 0.836 | 0.918 |
|  avg  | 0.191 | 1.737 | 7.309 | 0.294 | 0.707 | 0.889 | 0.947 |

- **Summary:** $\text{DES}_1=$ 0.484, $\text{DES}_2=$ 0.242, $\text{DES}_3=$ 0.270




### Motion Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.129 | 1.083 | 5.414 | 0.211 | 0.851 | 0.949 | 0.976 |
|   2   | 0.142 | 1.170 | 5.838 | 0.231 | 0.815 | 0.936 | 0.972 |
|   3   | 0.168 | 1.437 | 6.647 | 0.269 | 0.752 | 0.908 | 0.958 |
|   4   | 0.208 | 1.891 | 7.562 | 0.316 | 0.672 | 0.863 | 0.937 |
|   5   | 0.230 | 2.096 | 8.006 | 0.343 | 0.623 | 0.839 | 0.926 |
|  avg  | 0.175 | 1.535 | 6.693 | 0.274 | 0.743 | 0.899 | 0.954 |

- **Summary:** $\text{DES}_1=$ 0.433, $\text{DES}_2=$ 0.216, $\text{DES}_3=$ 0.236




### Zoom Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.158 | 1.329 | 5.815 | 0.242 | 0.794 | 0.928 | 0.968 |
|   2   | 0.171 | 1.434 | 6.047 | 0.259 | 0.763 | 0.915 | 0.962 |
|   3   | 0.166 | 1.339 | 5.969 | 0.250 | 0.774 | 0.919 | 0.965 |
|   4   | 0.176 | 1.451 | 6.140 | 0.260 | 0.753 | 0.910 | 0.962 |
|   5   | 0.177 | 1.476 | 6.154 | 0.260 | 0.753 | 0.910 | 0.961 |
|  avg  | 0.170 | 1.406 | 6.025 | 0.254 | 0.767 | 0.916 | 0.964 |

- **Summary:** $\text{DES}_1=$ 0.402, $\text{DES}_2=$ 0.201, $\text{DES}_3=$ 0.221




### Elastic Transform
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.118 | 0.977 | 5.007 | 0.197 | 0.872 | 0.956 | 0.980 |
|   2   | 0.119 | 0.979 | 5.046 | 0.199 | 0.870 | 0.955 | 0.980 |
|   3   | 0.121 | 0.993 | 5.114 | 0.201 | 0.864 | 0.954 | 0.979 |
|   4   | 0.123 | 1.018 | 5.193 | 0.204 | 0.860 | 0.953 | 0.978 |
|   5   | 0.126 | 1.055 | 5.298 | 0.208 | 0.852 | 0.949 | 0.977 |
|  avg  | 0.121 | 1.004 | 5.132 | 0.202 | 0.864 | 0.953 | 0.979 |

- **Summary:** $\text{DES}_1=$ 0.258, $\text{DES}_2=$ 0.129, $\text{DES}_3=$ 0.141




### Color Quant
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.115 | 0.909 | 4.881 | 0.193 | 0.876 | 0.959 | 0.981 |
|   2   | 0.117 | 0.928 | 4.915 | 0.195 | 0.873 | 0.958 | 0.981 |
|   3   | 0.129 | 1.029 | 5.135 | 0.208 | 0.849 | 0.951 | 0.978 |
|   4   | 0.172 | 1.367 | 5.932 | 0.252 | 0.755 | 0.921 | 0.968 |
|   5   | 0.278 | 2.479 | 7.903 | 0.360 | 0.530 | 0.823 | 0.930 |
|  avg  | 0.162 | 1.342 | 5.753 | 0.242 | 0.777 | 0.922 | 0.968 |

- **Summary:** $\text{DES}_1=$ 0.386, $\text{DES}_2=$ 0.193, $\text{DES}_3=$ 0.209




### Gaussian Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.176 | 1.361 | 6.104 | 0.258 | 0.738 | 0.913 | 0.966 |
|   2   | 0.225 | 1.806 | 7.104 | 0.315 | 0.627 | 0.864 | 0.945 |
|   3   | 0.296 | 2.524 | 8.518 | 0.392 | 0.470 | 0.781 | 0.911 |
|   4   | 0.350 | 3.231 | 9.869 | 0.456 | 0.388 | 0.692 | 0.869 |
|   5   | 0.376 | 3.668 | 10.720 | 0.494 | 0.359 | 0.649 | 0.839 |
|  avg  | 0.285 | 2.518 | 8.463 | 0.383 | 0.516 | 0.780 | 0.906 |

- **Summary:** $\text{DES}_1=$ 0.768, $\text{DES}_2=$ 0.384, $\text{DES}_3=$ 0.551




### Impulse Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.191 | 1.457 | 6.557 | 0.279 | 0.701 | 0.897 | 0.959 |
|   2   | 0.240 | 1.946 | 7.785 | 0.341 | 0.579 | 0.843 | 0.933 |
|   3   | 0.280 | 2.401 | 8.700 | 0.386 | 0.490 | 0.796 | 0.913 |
|   4   | 0.343 | 3.184 | 10.012 | 0.455 | 0.394 | 0.700 | 0.871 |
|   5   | 0.369 | 3.614 | 10.752 | 0.492 | 0.365 | 0.655 | 0.842 |
|  avg  | 0.285 | 2.520 | 8.761 | 0.391 | 0.506 | 0.778 | 0.904 |

- **Summary:** $\text{DES}_1=$ 0.779, $\text{DES}_2=$ 0.389, $\text{DES}_3=$ 0.563




### Shot Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.139 | 1.035 | 5.468 | 0.218 | 0.821 | 0.944 | 0.978 |
|   2   | 0.178 | 1.317 | 6.433 | 0.264 | 0.723 | 0.908 | 0.965 |
|   3   | 0.251 | 2.068 | 8.180 | 0.350 | 0.549 | 0.826 | 0.929 |
|   4   | 0.338 | 3.138 | 9.979 | 0.450 | 0.398 | 0.704 | 0.871 |
|   5   | 0.361 | 3.492 | 10.570 | 0.481 | 0.373 | 0.668 | 0.849 |
|  avg  | 0.253 | 2.210 | 8.126 | 0.353 | 0.573 | 0.810 | 0.918 |

- **Summary:** $\text{DES}_1=$ 0.681, $\text{DES}_2=$ 0.340, $\text{DES}_3=$ 0.442




### ISO Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.207 | 1.581 | 6.993 | 0.298 | 0.656 | 0.879 | 0.952 |
|   2   | 0.234 | 1.848 | 7.520 | 0.328 | 0.592 | 0.852 | 0.940 |
|   3   | 0.280 | 2.339 | 8.410 | 0.378 | 0.493 | 0.798 | 0.917 |
|   4   | 0.328 | 2.930 | 9.401 | 0.430 | 0.414 | 0.728 | 0.887 |
|   5   | 0.360 | 3.415 | 10.288 | 0.473 | 0.375 | 0.673 | 0.855 |
|  avg  | 0.282 | 2.423 | 8.522 | 0.381 | 0.506 | 0.786 | 0.910 |

- **Summary:** $\text{DES}_1=$ 0.776, $\text{DES}_2=$ 0.388, $\text{DES}_3=$ 0.557




### Pixelate
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.121 | 1.005 | 5.027 | 0.198 | 0.868 | 0.956 | 0.979 |
|   2   | 0.122 | 1.019 | 5.078 | 0.200 | 0.866 | 0.955 | 0.979 |
|   3   | 0.130 | 1.096 | 5.260 | 0.208 | 0.852 | 0.949 | 0.978 |
|   4   | 0.144 | 1.215 | 5.574 | 0.223 | 0.824 | 0.940 | 0.974 |
|   5   | 0.150 | 1.278 | 5.778 | 0.231 | 0.812 | 0.934 | 0.972 |
|  avg  | 0.133 | 1.123 | 5.343 | 0.212 | 0.844 | 0.947 | 0.976 |

- **Summary:** $\text{DES}_1=$ 0.289, $\text{DES}_2=$ 0.145, $\text{DES}_3=$ 0.158




### JPEG Compression
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.132 | 1.126 | 5.282 | 0.212 | 0.846 | 0.948 | 0.977 |
|   2   | 0.143 | 1.217 | 5.441 | 0.223 | 0.823 | 0.940 | 0.974 |
|   3   | 0.152 | 1.304 | 5.603 | 0.233 | 0.805 | 0.934 | 0.972 |
|   4   | 0.184 | 1.627 | 6.117 | 0.268 | 0.739 | 0.907 | 0.960 |
|   5   | 0.225 | 2.222 | 6.855 | 0.307 | 0.667 | 0.874 | 0.944 |
|  avg  | 0.167 | 1.499 | 5.860 | 0.249 | 0.776 | 0.921 | 0.965 |

- **Summary:** $\text{DES}_1=$ 0.391, $\text{DES}_2=$ 0.196, $\text{DES}_3=$ 0.215



