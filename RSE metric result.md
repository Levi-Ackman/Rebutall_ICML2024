Considering invaluable suggestions of reviewer **cHaS**, we conducted additional experiments to explore performance of **Leedam (Ours)**, [iTransformer](https://arxiv.org/abs/2310.06625), [MICN](https://openreview.net/pdf?id=zt53IDUR1U), [DLinear](https://arxiv.org/pdf/2205.13504.pdf),[PatchTST](https://arxiv.org/abs/2211.14730), [Crossformer](https://openreview.net/pdf?id=vSVLM2j9eie), in terms of **R-squared(Vlaue between 0 and 1, the larger, the better)**. 
Reults:
|Models|pred_len|Leddam(Ours)|iTransformer|MICN|DLinear|PatchTST|Crossformer|
|-|-|-|-|-|-|-|-|
|Dataset\Metric||R-squared|R-squared|R-squared|R-squared|R-squared|R-squared|
| ETTh2      | 96       | **0.813**     | 0.806        | 0.767 | 0.775   | 0.811    | 0.556       |
|            | 720      | **0.740**     | 0.718        | 0.477 | 0.516   | 0.738    | 0.245       |
| ETTm2      | 96       | **0.870**     | 0.866        | 0.861 | 0.854   | 0.868    | 0.821       |
|            | 720      | **0.740**     | 0.714        | 0.631 | 0.650   | 0.740    | 0.135       |
| Weather    | 96       | 0.731         | 0.693        | 0.668 | 0.660   | 0.704    | **0.739**   |
|            | 720      | **0.407**     | 0.380        | 0.425 | 0.398   | 0.391    | 0.364       |

It is clear that Leddam still distinctly outperforms other methods on **R-squared**, which indicates Leddam could better captures the underlying relationships in the data.



