# RobustVision

**End-to-end adversarial robustness research framework for image classifiers**

---

## Overview
RobustVision is a research framework designed to train and evaluate image classifiers under strong adversarial threat models. It implements modern adversarial training methods and provides tools for diagnosing and mitigating common failure modes such as gradient masking and robust overfitting.

## Key Capabilities
- **Adversarial Training**: Projected Gradient Descent (PGD) and TRADES formulations
- **Robust Evaluation**: AutoAttack and standard threat-model evaluation suites
- **Diagnosis**: Detection of gradient masking and overestimation of robust accuracy
- **Mitigation**: Techniques for reducing robust overfitting while preserving clean accuracy
- **Trade-off Management**: Explicit handling of the robustness–accuracy trade-off under compute constraints

## Methods Implemented
| Method | Description |
|--------|-------------|
| PGD Training | Multi-step projected gradient descent adversarial training |
| TRADES | Trade-off inspired adversarial defense with KL-divergence regularization |
| AutoAttack | Ensemble evaluation (APGD-CE, APGD-DLR, FAB, Square) |
| Robust Overfitting Mitigation | Early stopping + regularization strategies on the robust loss |

## Research Focus
This work targets the practical challenges of deploying robust models:
- Maintaining high robust accuracy without severe clean-accuracy degradation
- Avoiding gradient masking that leads to false security
- Training under realistic compute and data budgets

## Tech Stack
- PyTorch
- Standard vision datasets and architectures (ResNet, WideResNet, etc.)
- Adversarial attack libraries compatible with AutoAttack

## Status
Active research codebase (updated August 2026). Core training and evaluation loops are implemented and used for empirical studies on robust overfitting and threat-model generalization. Ongoing work focuses on improved evaluation diagnostics and practical deployment constraints.

---

**Author**: Gopar Beji  
**Related work**: EdgeGen (generative + compression), AlignEval-LLM (post-training alignment)
