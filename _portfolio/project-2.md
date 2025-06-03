---
title: "In-Context Learning Enhanced Molecule Property Prediction via LLMs"
excerpt: "Improved the performance of LLMs in molecule property prediction task by in-context learning."
collection: portfolio
start_date: Jul.2024
end_date: Aug.2024
code: https://github.com/onlyairnopods/ICL4MPP
image: "https://gh-card.dev/repos/onlyairnopods/ICL4MPP.svg"
images:
  # - /images/500x300.png
  # - /images/500x300.png
---

This project investigates the performance of specialized large language models (LLMs) that can understand and predict the molecule property, and in-context learning method was applied to enhance.

- Experimented with LLMs using zero-shot and few-shot In-Context Learning in an unsupervised manner to select samples across various settings, including random selection and fingerprint-based methods (MACCS, RDKit, Morgan) with Tanimoto and Cosine similarities.

- Adapted the Efficient Prompt Retrieval algorithm for supervised sample selection. Trained a retriever with contrastive learning to select more accurate ICL samples during testing, yielding modest improvements.

- **Temperature**: 0.9  
- **Task**: ClinTox CT_TOX  
- **Metric**: AUC-ROC

- **ChemLLM 20B SFT**

  | Prompt Setting                                  | 0-shot            | 2-shot                 | 4-shot                 | 8-shot             |
  | ----------------------------------------------- | ----------------- | ---------------------- | ---------------------- | ------------------ |
  | zero-shot                                       | 0.463768115942029 | \\                     | \\                     | \\                 |
  | Few-shot random sample                          | \\                | **0.5884057971014492** | 0.5072463768115941     | 0.6231884057971014 |
  | Few-shot MACCS Fingerprint Tanimoto Similarity  | \\                | 0.5427536231884058     | 0.5891304347826086     | \\                 |
  | Few-shot MACCS Fingerprint Cosine Similarity    | \\                | 0.5394927536231885     | 0.5463768115942029     | \\                 |
  | Few-shot MACCS Fingerprint Dice Similarity      | \\                | 0.5427536231884058     | 0.5891304347826086     | \\                 |
  | Few-shot RDK Fingerprint Tanimoto Similarity    | \\                | 0.5286231884057971     | 0.6380434782608696     | \\                 |
  | Few-shot RDK Fingerprint Cosine Similarity      | \\                | 0.572463768115942      | 0.5746376811594203     | \\                 |
  | Few-shot RDK Fingerprint Dice Similarity        | \\                | 0.5286231884057971     | 0.6380434782608696     | \\                 |
  | Few-shot Morgan Fingerprint Tanimoto Similarity | \\                | **0.6463768115942029** | **0.6463768115942029** | \\                 |
  | Few-shot Morgan Fingerprint Dice Similarity     | \\                | **0.6463768115942029** | **0.6463768115942029** | \\                 |

- **ChemDFM 13B SFT**

  | Prompt Setting                     | 0-shot                   | 2-shot                   | 4-shot                   | 8-shot                   |
  |------------------------------------|--------------------------|--------------------------|--------------------------|--------------------------|
  | zero-shot                          | 0.4601449275362319       | \                        | \                        | \                        |
  | Few-shot random sample             | \                        | 0.5804347826086957       | 0.3586956521739131       | 0.5405797101449276       |
  | Few-shot MACCS Fingerprint Tanimoto Similarity | \                        | 0.618840579710145        | 0.5094202898550725       | 0.5340579710144927       |
  | Few-shot MACCS Fingerprint Cosine Similarity  | \                        | 0.668840579710149        | 0.552536231884058        | 0.5514492753623188       |
  | Few-shot MACCS Fingerprint Dice Similarity   | \                        | 0.618840579710145        | 0.5094202898550725       | 0.5340579710144927       |
  | Few-shot RDK Fingerprint Tanimoto Similarity | \                        | 0.4797101449275363       | 0.48695652173913045      | 0.4840579710144927       |
  | Few-shot RDK Fingerprint Cosine Similarity   | \                        | 0.48043478260869565      | 0.49130434782608695      | 0.5311594202898551       |
  | Few-shot RDK Fingerprint Dice Similarity     | \                        | 0.4797101449275363       | 0.48695652173913045      | 0.4840579710144927       |
  | Few-shot Morgan Fingerprint Tanimoto Similarity | \                        | 0.5434782608695652       | 0.49710144927536226      | 0.4442028985507246       |
  | Few-shot Morgan Fingerprint Dice Similarity   | \                        | 0.5434782608695652       | 0.49710144927536226      | 0.4442028985507246       |

---

*This research project was completed during my summer research camp in the NLP group at Nanjing University.*