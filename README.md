<div align="center">
  
  <a href="https://dl.acm.org/doi/10.1145/3680121.3697807">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=1e90ff&height=200&section=header&text=iGuard&fontSize=70&fontAlignY=35&desc=Efficient%20Isolation%20Forest%20Design%20for%20Malicious%20Traffic%20Detection%20in%20Programmable%20Switches&descSize=20&descAlignY=55&fontColor=ffffff" alt="iGuard Banner" />
  </a>
  <p>
    <kbd>AI for Network Security</kbd>
    <kbd>P4 Language</kbd>
    <kbd>Programmable Switches (Intel Tofino)</kbd>
    <kbd>Isolation Forest</kbd>
    <kbd>Anomaly Detection</kbd>
    <kbd>Knowledge Distillation</kbd>
    <kbd>Line-Speed Detection</kbd>
  </p>

  <p>
    <img src="https://img.shields.io/badge/Hardware-Intel_Tofino-0071C5?style=for-the-badge&logo=intel&logoColor=white" alt="Intel Tofino" />
    <img src="https://img.shields.io/badge/Language-P4-F05032?style=for-the-badge" alt="P4 Language" />
    <a href="https://dl.acm.org/doi/10.1145/3680121.3697807"><img src="https://img.shields.io/badge/Publication-ACM-CC0000?style=for-the-badge&logo=acm&logoColor=white" alt="ACM Paper" /></a>
  </p>
</div>

---

## 🎯 The Challenge & The Solution

> [!IMPORTANT]
> **The Problem:** Programmable switch data planes face severe memory constraints and minimal support for complex math. While conventional Isolation Forests (iForests) fit these constraints, they yield suboptimal detection for malicious traffic. To achieve higher accuracy, current solutions are forced to punt packets to the software control plane for deeper analysis—creating a severe bottleneck that drastically increases latency and degrades overall network throughput.

> [!TIP]
> **The iGuard Solution:** We introduce the first iForest implementation that accurately detects malicious traffic by distilling the "knowledge" of powerful autoencoders into a minimal set of **whitelist rules** natively installable on data planes.

<br>

## :hammer_and_wrench: System Overview
<img width="1516" height="651" alt="iGuard-overview" src="https://github.com/user-attachments/assets/b6f3b096-d981-486d-a99e-eb5ee6303ba3" />
<br>
<img width="1169" height="740" alt="iGuard-training" src="https://github.com/user-attachments/assets/f78a5bd8-5ccc-4f01-9e66-f3846b1fb1f8" />
<br>
<img width="1187" height="271" alt="iGuard-processing" src="https://github.com/user-attachments/assets/acdaedfa-33e6-48b4-afb0-d4a2323c4026" />

## 🚀 Key Innovations
By bridging the gap between complex ML and strict hardware limits, we developed iGuard. Here are the key contributions:

```diff
+ Unsupervised Detection: Detects anomalies without needing massive, expensively labeled datasets.
+ Autoencoder-Enhanced iForest: Significantly improves separation between benign and malicious traffic compared to conventional iForests.
+ Line-Rate Processing: Evaluates packets entirely in the data plane at massive throughput levels.
+ Hardware Efficient: Maintains strict memory efficiency suitable for Intel Tofino switches.
```

* 📚 **Research Paper:** [ACM Digital Library: iGuard](https://dl.acm.org/doi/10.1145/3680121.3697807)
* 💻 **Official Codebase:** [GitHub: networked-systems-iith/iGuard](https://github.com/networked-systems-iith/iGuard)

> [!TIP]
> If you are using this work in your research, please consider citing our paper.
```
@inproceedings{10.1145/3680121.3697807,
author = {Mittal, Sankalp and V., Harikrishnan and Heetkumar, Patel and Tammana, Praveen},
title = {iGuard: Efficient Isolation Forest Design for Malicious Traffic Detection in Programmable Switches},
year = {2024},
isbn = {9798400711084},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3680121.3697807},
doi = {10.1145/3680121.3697807},
abstract = {Deploying machine learning (ML) models in programmable switch data planes facilitates low latency and high throughput traffic inference at line speed. However, data planes pose significant constraints due to the limited memory and minimal support for mathematical operations and data types. As a result, the only unsupervised ML models implemented in data planes to date are Isolation Forests (iForests). However, conventional iForest models yield suboptimal malicious traffic detection performance in various traffic use cases. To address this limitation, this paper proposes iGuard, the first iForest implementation that can accurately detect malicious traffic by incorporating the "knowledge" of more powerful autoencoders. We deploy iGuard in the form of a small set of whitelist rules that could be easily installed in the switch data planes. We implement iGuard using the P4 language, and assess its performance in an experimental platform based on Intel Tofino switches. Upon evaluating iGuard on various attack traffic use cases, our model can improve accuracy up to 48.3\% while maintaining a similar or lower switch memory footprint over previous approaches to implement iForest models in real-world equipment.},
booktitle = {Proceedings of the 20th International Conference on Emerging Networking EXperiments and Technologies},
pages = {55–64},
numpages = {10},
keywords = {intrusion/anomaly detection, machine learning, network security, programmable switches, software defined networking},
location = {Los Angeles, CA, USA},
series = {CoNEXT '24}
}
```

<br />

## :busts_in_silhouette: Team
<div align="center">
  <table style="border: none; border-collapse: collapse; background-color: transparent;">
    <tr>
      <td align="center" style="border: none; padding: 20px;">
        <a href="https://praveenabt.github.io/">
          <img src="https://img.shields.io/badge/%20-Supervisor-333?style=flat&labelColor=666" alt="Supervisor Badge"/><br/>
          <strong style="font-size: 1.1em;">Dr. Praveen Tammana</strong>
        </a>
      </td>
      <td align="center" style="border: none; padding: 20px;">
        <img src="https://img.shields.io/badge/%20-Mentor-333?style=flat&labelColor=666" alt="Mentor Badge"/><br/>
        <strong style="font-size: 1.1em;">Sankalp Mittal</strong>
      </td>
    </tr>
    <tr>
      <td align="center" colspan="2" style="border: none; padding: 20px;">
        <img src="https://img.shields.io/badge/%20-Key%20Contributors-333?style=flat&labelColor=666" alt="Contributors Badge"/><br/>
        <span style="font-size: 1.1em; font-weight: bold;">Patel Heetkumar &nbsp;&nbsp;|&nbsp;&nbsp; V. Harikrishnan</span>
      </td>
    </tr>
  </table>
</div>
<hr style="border: 1px solid #eee;" />

<div align="center">
  <p style="color: #888;">networked-systems-iith @ Indian Institute of Technology Hyderabad (IITH)</p>
  <a href="#readme-top">Back to top ⬆️</a>
</div>
