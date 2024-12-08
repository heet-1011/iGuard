<a id="readme-top"></a>
<br />
<div align="center">
  
# <h3 align="center">[**"iGuard : Efficient Isolation Forest Design for Malicious Traffic Detection in Programmable Switches"**](https://dl.acm.org/doi/10.1145/3680121.3697807)</h3>

</div>

 <p align="justify">
    Deploying machine learning (ML) models in programmable switch data planes facilitates low latency and high throughput traffic inference at line speed. However, data planes pose significant constraints due to the limited memory and minimal support for mathematical operations and data types. As a result, the only unsupervised ML models implemented in data planes to date are Isolation Forests (iForests). However, conventional iForest models yield suboptimal malicious traffic detection performance in various traffic use cases. To address this limitation, this paper proposes iGuard, the first iForest implementation that can accurately detect malicious traffic by incorporating the "knowledge" of more powerful autoencoders. We deploy iGuard in the form of a small set of whitelist rules that could be easily installed in the switch data planes. We implement iGuard using the P4 language, and assess its performance in an experimental platform based on Intel Tofino switches. Upon evaluating iGuard on various attack traffic use cases, our model can improve accuracy up to 48.3% while maintaining a similar or lower switch memory footprint over previous approaches to implement iForest models in real-world equipment.

  </p>
<br/>
<br/>
<br/>

## Key Contribution
1. We present a novel iForest model (iGuard) that accurately detects malicious traffic in the data plane at line speed. This model design is achieved through autoencoder-guided training, knowledge distillation from autoencoders to
trained iForest, and conversion of iForest to a small set of whitelist rules that can be installed on target switch.
2. We clarify the challenges of implementing iGuard on Intel’s Tofino switch and developing a working prototype.
3. We extensively evaluate iGuard in a real-world testbed, revealing iGuard’s increasing accuracy gains over previous implementations of iForest models on various attack datasets and normal datasets while maintaining similar or lower switch memory footprint.

## Research Paper
<a href="https://dl.acm.org/doi/10.1145/3680121.3697807">iGuard</a>

## Codebase
<a href="https://github.com/networked-systems-iith/iGuard">Official Codebase</a>

## Under supervision of 
<a href="https://praveenabt.github.io/">Dr. Praveen Tammana </a>

## Mentor
Sankalp Mittal

## Contributors
V. Harikrishnan <br/>
Patel Heetkumar
