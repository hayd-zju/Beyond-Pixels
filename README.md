<div align="center">

# Beyond Pixels: From Video Priors to 4D Worlds

[Zihao Liu](https://scholar.google.com/citations?user=2q-92DsAAAAJ), [Xiaolong Shen](https://scholar.google.com/citations?user=vAMMc8EAAAAJ), [Zhenglin Zhou](https://scholar.google.com/citations?user=6v7tOfEAAAAJ), [Ruijie Quan](https://scholar.google.com/citations?user=WKLRPsAAAAAJ), [Yi Yang](https://scholar.google.com/citations?user=RMSuNFwAAAAJ)<sup>*</sup>

**ReLER, CCAI, Zhejiang University**

<sup>*</sup>Corresponding author

<p>
  <a href="https://hayd-zju.github.io/Beyond-Pixels/"><img src="https://img.shields.io/badge/Project-Page-2563EB?style=flat&amp;logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPGRlZnM%2BPGxpbmVhckdyYWRpZW50IGlkPSJnIiB4MT0iMiIgeTE9IjIiIHgyPSIyMiIgeTI9IjIyIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSI%2BPHN0b3Agc3RvcC1jb2xvcj0iIzI1NjNlYiIvPjxzdG9wIG9mZnNldD0iLjU0IiBzdG9wLWNvbG9yPSIjN2MzYWVkIi8%2BPHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjZjk3MzE2Ii8%2BPC9saW5lYXJHcmFkaWVudD48L2RlZnM%2BPHBhdGggZmlsbD0idXJsKCNnKSIgZD0iTTEyIDEuNWMuOSA1LjkgNC42IDkuNiAxMC41IDEwLjUtNS45LjktOS42IDQuNi0xMC41IDEwLjVDMTEuMSAxNi42IDcuNCAxMi45IDEuNSAxMiA3LjQgMTEuMSAxMS4xIDcuNCAxMiAxLjVaIi8%2BPGNpcmNsZSBjeD0iMTkiIGN5PSI1IiByPSIyIiBmaWxsPSIjZjk3MzE2Ii8%2BPC9zdmc%2B" alt="Project Page"></a>
  <a href="https://arxiv.org/abs/2608.10744"><img src="https://img.shields.io/badge/arXiv-2608.10744-B31B1B?style=flat&amp;logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAMAAABEpIrGAAAABGdBTUEAALGPC%2FxhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAACr1BMVEUAAACzICWzICSyrKazrKWzqaKzraazR0mzTE6zaGizBQiz49uzZmSzEBazHySzsam0ICmzICWzICWzICWzICWzICWzICWzICWzICWzICWzICWzICWzICWzICWzICWzICWzrKWzrKWzICWzICWzICWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzICWzrKWzrKWzrKWzICWzICWzICWzHySz4dWzrKWzrKWzrKWzICWzICWzHySzgX2zrqezrKWzrKWzICWzPD%2BzrKWzrKWzrKWzICWzHySzjYmzr6izraazT1CzLjKzMDSzQUOzrKWzrqezgH2zKi6zHySzICWzrKWzrKWzcW%2BzICWzICWzrKWzrKWzYWGzICWzrKWzUVKzICWzrKWzrKWznZezQkSzICWzICWzrKWzraazkY2zHiOzICWzICWzjYmzm5WzhIGzODuzAACzHySzHSKzOz6zrqazs6yzICWzICWzODuzrKWzrKWzrKWzICWzICWzODuzo5yzrKWzrKWzICWzICWzICWzGyCzr6ezrKWzrKWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzrKWzrKWzrKWzrKWzrKWzICWzICWzICWzrKWzrKWzrKWzrKWzICWzICWzICWzrKWzrKWzrKWzICWzICWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzrKWzICWzrKWzHySzkYyzrqezHiOzODuzJCmzqaOzISazraazpZ6zNTizkIuzi4ezraX%2F%2F%2F8A%2FVYjAAAA1HRSTlMAAAAAAAAAAAAAAAAAAAAAAAGA95kOB7X6kQ9W8fyaEQIBA3z9oRUllnUKDJz%2BqBgwxuwxGbquHD3SpQwt1CBL3cEeR%2Be7JFvm1mX0wSgEbO5HBYXFkfPyYaX%2B%2Bn0EHsH9lwtO8%2FNRJrr8%2FttFGb7%2B3jpk%2Fv6ecv6sK9j%2B%2FvVcQNf%2B8nUGSfD7dQMHivyVCmr2%2Fvl3A0np28zvWS7V0joht%2BHJMR2vzCcLvygYp7IVc7QhFJ%2F9lQkSzhoRl%2Ft2lu0UDY9XDSoLhvjgOwh89a4GB4L2i8A61lMAAAABYktHROQvYjspAAAAB3RJTUUH5wETDS455INCLAAAAgZJREFUOMt10%2FdfTXEYB%2FDz6Ilst3lFueWmjDIysmdkF0Kyyd7Ze5WZcc2ErIhKISops6zs73Pda1zrH%2FEcoXPqe8%2Bvn%2Ffre57z%2BT5HURQwuHt4eoHi9AFvH2Fs6gu1nAJo1lz4%2BbeAqkNc0BSAGhHY0ijMQa3%2BC8TgkNZttKJtOyFCw9r%2FFYgdOlKncC2Azl2EEF27%2FRGIEd2JevRE3Ri9erPw6cMCA%2Fr2I%2Bo%2FAFE%2F6MBBLCIHg6tpSBTR0HB9rophw1mMGDlqdDRRVEz1nMWYsX4sxsWOJ5owsWbOwjeOgXXSR1v85CmSnF8ydZpVCPun6TNm1pY2Wsdt1mwW1oQ5devJcsS58%2BYvUMXCRSC7Oly8hGjpZxZi2XKJQFyRSPRl5VcGYpVBBlYTkePbGvWItYGSd%2BC69arYsNEuNm2WDYG4ZauDyLbt%2B%2FYdO6X7Vb9BUjILx67dexpKe2i0d9%2F%2BHzYWKQcay3IwHDxkP%2FyT57AcOSq7Cjh2nIs%2BcfIXUeopyWVC2mn%2BvjNn08%2FxGecjaojKpbtwEVwvZbC4fKWagEx%2Fzq9eA0DMyuZKc67rN65JrlGIvBtqP4g3b%2BVT4u07uqUtKBTmsKLK%2FhDvFt8jS4lJu%2Ffepfc9H1T9OA8fxVPqY80YAE%2FKMjX9Y%2FnTZ%2FT8hWwz%2F4mXFa%2Fo9RvnQMG3795%2FUKf4DUwCyzJ9eBcsAAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDIzLTAxLTE5VDEzOjQ2OjU3KzAwOjAwqJ4w4AAAACV0RVh0ZGF0ZTptb2RpZnkAMjAyMy0wMS0xOVQxMzo0Njo1NyswMDowMNnDiFwAAABXelRYdFJhdyBwcm9maWxlIHR5cGUgaXB0YwAAeJzj8gwIcVYoKMpPy8xJ5VIAAyMLLmMLEyMTS5MUAxMgRIA0w2QDI7NUIMvY1MjEzMQcxAfLgEigSi4A6hcRdPJCNZUAAAAASUVORK5CYII%3D" alt="arXiv 2608.10744"></a>
  <a href="https://huggingface.co/papers/2608.10744"><img src="https://img.shields.io/badge/HF_Daily_Papers-%231-FFD21E?style=flat&amp;logo=huggingface&amp;logoColor=FFD21E" alt="Hugging Face Daily Papers No. 1"></a>
  <a href="https://hayd-zju.github.io/Beyond-Pixels/paper.pdf"><img src="https://img.shields.io/badge/PDF-Available-FF8C42?style=flat&amp;logo=adobeacrobatreader&amp;logoColor=white" alt="PDF"></a>
  <a href="#release-status"><img src="https://img.shields.io/badge/Code-Soon-6F42C1?style=flat&amp;logo=github&amp;logoColor=white" alt="Code coming soon"></a>
  <a href="#release-status"><img src="https://img.shields.io/badge/Hugging_Face-Soon-F5C542?style=flat&amp;logo=huggingface&amp;logoColor=FFD21E" alt="Hugging Face coming soon"></a>
  <a href="#release-status"><img src="https://img.shields.io/badge/ModelScope-Soon-1F6FEB?style=flat&amp;logo=modelscope&amp;logoColor=white" alt="ModelScope coming soon"></a>
</p>

</div>

<div align="center">
  <img src="https://hayd-zju.github.io/media/teaser-figure-original.webp?v=pdf-replacement-20260810" alt="Beyond Pixels teaser" width="100%">
</div>

> **TL;DR:** Beyond Pixels provides a unified latent-to-4D interface that lifts terminal video DiT latents into explicit dynamic 3D scenes across compatible generation tasks.

## 🔥 News

- **[2026/08/12]** 🔥 *Beyond Pixels* currently ranks **1st** on [Hugging Face Daily Papers](https://huggingface.co/papers/2608.10744)! Thank you all for your support and love! 🤗
- **[2026/08/12]** 🤗 Many thanks to [taesiri](https://huggingface.co/taesiri) for submitting our paper to [Hugging Face Daily Papers](https://huggingface.co/papers/2608.10744)!
- **[2026/08/11]** 📄 Our paper is now available on [arXiv](https://arxiv.org/abs/2608.10744)!
- **[2026/08/11]** The official repository and project page are available. Code and model release are under preparation.

## 🚧 TODO List

- [x] [Project Page](https://hayd-zju.github.io/Beyond-Pixels/)
- [ ] Inference Code
- [ ] Training Code
- [ ] Pretrained Weights

## 📚 Citation

```bibtex
@misc{liu2026pixelsvideopriors4d,
      title={Beyond Pixels: From Video Priors to 4D Worlds}, 
      author={Zihao Liu and Xiaolong Shen and Zhenglin Zhou and Ruijie Quan and Yi Yang},
      year={2026},
      eprint={2608.10744},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2608.10744}, 
}
```
