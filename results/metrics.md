# Metrics (final)

## Lightbar Model (V1 vs V2)
| Metric   | V1     | V2     |
|:---------|:------:|:------:|
| mAP50    | 0.7821 | 0.8575 |
| mAP50-95 | 0.4693 | 0.5017 |
| Box Loss | 1.7702 | 1.9790 |
| Cls Loss | 1.2951 | 1.8427 |
| DFL Loss | 1.5848 | 1.7639 |

Notes: V1 had slightly better class accuracy (~78% vs ~76%); we prefer V1 for the ensemble. :contentReference[oaicite:1]{index=1}

## Vehicle Model
| mAP50 | mAP50-95 | Box Loss | Cls Loss | DFL Loss |
|:-----:|:--------:|:--------:|:--------:|:--------:|
| 0.6369| 0.4823   | 0.9779   | 1.0329   | 1.2653   |

Observation: strong snowplow bias and false positives; likely learned snow context. :contentReference[oaicite:2]{index=2}
