# VulTeller: Learning to Locate and Describe Vulnerabilities

This repository provides the dataset used in our ASE 2023 paper on vulnerability localization.

> 📄 **Reference Paper**  
> *Jian Zhang, Shangqing Liu, Xu Wang, Tianlin Li, Yang Liu.*  
> **Learning to Locate and Describe Vulnerabilities.**  
> *Proceedings of the 38th IEEE/ACM International Conference on Automated Software Engineering (ASE 2023).*  
> [PDF link](https://zhangj111.github.io/files/ASE23_VulTeller.pdf)

---

## Overview
The dataset is used for fine-grained vulnerability localization based on BigVul.  
It contains code functions paired with vulnerability metadata collected from real-world open-source projects.

Due to an associated patent application (No.2024102587930) by Desay SV, only the dataset is released here, without code and models.

---

## Contents
The archive `bv_loc.zip` includes:
- `train.csv`, `valid.csv`, `test.csv` with 8 : 1 : 1 splits

**Columns**
| Column | Description |
|---------|--------------|
| `function` | Source code of the vulnerable function |
| `location` | Vulnerable Lines |
| `description` | Vulnerability description |
| `cve` | CVE ID |
| `cwe` | CWE ID |
| `project` | Project / repository name |

---
