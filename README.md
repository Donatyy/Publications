# Research Publications

Collection of my academic publications, papers, and research projects.

---

## 2026

### RETRIX at CheckThat! 2026: Source Retrieval for Scientific Web Claims
**Authors:** Fabio Baldan, **Davide Donati**, Alvise Garberino, Giancarlo Padoan, Marco Tessari, Nicola Ferro  
**Venue:** *Working Notes of CLEF 2026 - Conference and Labs of the Evaluation Forum* (CEUR-WS Vol. 4283, pp. 883–896)  
**Result: 5th place** overall in the challenge

· 🔗 [Official Proceedings (CEUR-WS)](https://ceur-ws.org/Vol-4283/)
· 📄 [Local PDF](./2026-clef-checkthat-retrix/RETRIX%20paper.pdf)
· 💻 [System Codebase](https://github.com/Donatyy/CLEF2026-SE.git)

<details>
<summary><b>Abstract & System Overview</b></summary>
<br>
We present <b>RETRIX</b>, a multi-stage multilingual Information Retrieval pipeline developed for Task 1 of the CLEF 2026 CheckThat! Lab. To retrieve authoritative scientific papers verifying social media claims across English, German, and French, our architecture combines cross-lingual query translation, semantic query expansion, hybrid multi-representation retrieval via <b>BGE-M3</b> (dense, sparse, and ColBERT-style scoring), and fine-tuned <b>Cross-Encoder</b> reranking.
</details>

<details>
<summary><b>BibTeX Citation</b></summary>

```bibtex
@inproceedings{Baldan2026RETRIX,
  author    = {Fabio Baldan and Davide Donati and Alvise Garberino and Giancarlo Padoan and Marco Tessari and Nicola Ferro},
  title     = {{RETRIX at CheckThat! 2026: Source Retrieval for Scientific Web Claims}},
  booktitle = {Working Notes of CLEF 2026 - Conference and Labs of the Evaluation Forum},
  series    = {CEUR Workshop Proceedings},
  volume    = {4283},
  pages     = {883--896},
  publisher = {CEUR-WS.org},
  year      = {2026},
  url       = {[https://ceur-ws.org/Vol-4283/](https://ceur-ws.org/Vol-4283/)}
}

---

## 📝 Technical Essays & Coursework

### NotPetya (2017): The Most Destructive Attack in History
**Author:** Davide Donati · **Year:** 2026 · **Type:** Technical Security Analysis (Unpublished)

📄 [Read PDF](./2026-notpetya-technical-analysis/NotPetya_Technical_Analysis.pdf) · 📁 [Folder & Summary](./2026-notpetya-technical-analysis/)

<details>
<summary><b>Abstract & Topics Covered</b></summary>
<br>
An in-depth technical and architectural analysis of the June 2017 NotPetya cyberattack. The paper dissects the full kill chain—from the compromised M.E.Doc accounting software update (<code>EzData.dll</code>) and dual SMBv1 exploit vectors (EternalBlue/EternalRomance) to in-memory LSASS credential harvesting (Mimikatz), WMI/PsExec lateral movement, and irreversible low-level disk wiping via <code>\\.\PhysicalDrive0</code> MBR overwrites and Salsa20-based MFT corruption. Concludes with infrastructure casualty analyses (Maersk, Merck) and Zero-Trust resilience principles.
</details>
