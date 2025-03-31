## Response Figure 1 to answer questions about interpretability
#### K (latent dimension) was set to 2 for sciLaMA on a sample of fetal liver atlas dataset
![alt text](https://github.com/anonymous-ICML2025/rebuttal_April1st/blob/main/Figures/Interpretability.png)
##### Captions: The visualization cell embedding (middle-left, dots are cells, colored by cell type annotations) and contexutal gene embedding (middle-right, dots are genes), both are 2D (latent node number = 2). The cell embedding visualizations on the top and bottom are colored by the expression level of genes that are sampled from different regions of contexutal gene embedding.

---
## Response Tables 1-2 to answer questions about dataset scope (two more benchmarking datasets)
#### mouse P0 cortical data
|Methods| ARI (↑) | NMI (↑) | ASW (↑) | cLISI (↑) |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
|scVI	              |0.284	|0.291	|0.501	|0.501 |
|cellPLM            |0.216	|0.281	|0.513	|0.684 |
|GenePT-w	          |0.000	|0.017	|0.409	|0.514 |
|scGPT	            |0.275	|0.310	|0.530	|0.716 |
|scGPT-finetuned	  |0.033	|0.061	|0.449	|0.535 |
|sciLaMA-scGPT	    |0.341	|0.374	|0.523	|0.738 |
|sciLaMA-ESM	      |0.299	|0.369	|0.530	|0.833 |
|sciLaMA-ProtTrans	|0.355	|0.366	|0.529	|0.775 |
|sciLaMA-GenePT	    |0.237	|0.321	|0.514	|0.776 |
|sciLaMA-ChatGPT	  |0.316	|0.351	|0.518	|0.738 |
|sciLaMA-CellPLM	  |0.343	|0.381	|0.524	|0.793 |

#### mouse skin data
|Methods| ARI (↑) | NMI (↑) | ASW (↑) | cLISI (↑) |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
|scVI	              |0.263	|0.316	|0.506	|0.678 |
|cellPLM	          |0.134	|0.175	|0.515	|0.698 |
|GenePT-w	          |0.001	|0.003	|0.468	|0.481 |
|scGPT	            |0.162	|0.179	|0.500	|0.677 |
|scGPT-finetuned	  |0.176	|0.166	|0.506	|0.718 |
|sciLaMA-scGPT	    |0.267	|0.215	|0.502	|0.668 |
|sciLaMA-ProtTrans	|0.187	|0.215	|0.500	|0.669 |
|sciLaMA-ESM	      |0.198	|0.219	|0.496	|0.634 |
|sciLaMA-CellPLM	  |0.190	|0.217	|0.500	|0.657 |
|sciLaMA-ChatGPT	  |0.275	|0.219	|0.503	|0.696 |
|sciLaMA-GenePT	    |0.223	|0.211	|0.505	|0.687 |

---

## Response Figure 2 to answer questions about sensitivity to hyperparameters (alignment loss weight γ)
![alt text](https://github.com/anonymous-ICML2025/rebuttal_April1st/blob/main/Figures/Sensitivity_gamma.png)
### corresponding Response Table 3
|gamma|	ARI_mean|	ARI_std	|NMI_mean|	NMI_std|	ASW_mean	|ASW_std	|cLISI_mean|	cLISI_std|
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | 
|`0`|	0.464 |0.371	|0.513	|0.390	|0.589	|0.087	|0.881	|0.170|
|`0.01`|	0.582	|0.021	|0.734	|0.022	|0.645	|0.010	|0.990	|0.002|
|`0.05`|	0.665	|0.114	|0.763	|0.041	|0.654	|0.005	|0.991	|0.002|
|`0.1`|	0.634	|0.088	|0.751	|0.023	|0.658	|0.012	|0.992	|0.002|
|`0.25`|	0.581	|0.024	|0.743	|0.013	|0.655	|0.006	|0.990	|0.002|
|`0.5`|	0.592	|0.010	|0.747	|0.004	|0.658	|0.012	|0.993	|0.001|
|`0.75`|	0.590	|0.015	|0.748	|0.013	|0.656	|0.012	|0.992	|0.002|
|`1`|	0.647	|0.107	|0.762	|0.038	|0.651	|0.025	|0.993	|0.003|

---

## Response Figure 3 to answer questions about sensitivity to hyperparameters (latent dimensionality K)
![alt text](https://github.com/anonymous-ICML2025/rebuttal_April1st/blob/main/Figures/Sensitivity_K.png)
### corresponding Response Table 4
|K (latent dim)|	ARI_mean|	ARI_std	|NMI_mean|	NMI_std|	ASW_mean	|ASW_std	|cLISI_mean|	cLISI_std|
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | 
|`10`|	0.651|	0.110|	0.756|	0.042|	0.654|	0.005|	0.991|	0.002 |
|`20`|	0.627|  0.082|	0.761|	0.025|	0.631|	0.015|	0.991|	0.000 |
|`30`|	0.583|	0.017|	0.742|	0.022|	0.633|	0.014|	0.991|	0.001 |
|`40`|	0.680|	0.114|	0.771|	0.039|	0.637|	0.009|	0.991|	0.002 |
|`50`|	0.606|	0.085|	0.743|	0.023|	0.631|	0.010|	0.990|	0.002 |
|`60`|	0.649|	0.100|	0.757|	0.030|	0.631|	0.015|	0.990|	0.002 |
|`70`|	0.590|	0.037|	0.738|	0.017|	0.635|	0.009|	0.991|	0.001 |
|`80`|	0.649|	0.095|	0.753|	0.020|	0.632|	0.009|	0.991|	0.001 |
|`90`|	0.656|	0.102|	0.756|	0.030|	0.637|	0.008|	0.991|	0.001 |
|`100`|	0.641|	0.108|	0.751|	0.027|	0.635|	0.006|	0.991|	0.002 |

---

## Response Table 5 to quantitative measure of gene trajectory in addition to visualization and cluster-level metrics
| |Raw external gene embedding	| Gene embedding before alignment	| Gene embedding after alignment |
| ------------- | ------------- | ------------- | ------------- | 
| Curvature-Based Smoothness Score	| 1.06 | 0.39	| 0.17 |
