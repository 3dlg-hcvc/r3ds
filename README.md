# R3DS

### R3DS: Reality-linked 3D Scenes for Panoramic Scene Understanding

#### ECCV 2024

[Qirui Wu](https://qiruiw.github.io/), [Sonia Raychaudhuri](https://sonia-raychaudhuri.github.io/), [Daniel Ritchie](https://dritchie.github.io/), [Manolis Savva](https://msavva.github.io/), [Angel X. Chang](http://angelxuanchang.github.io/)

[Project](https://3dlg-hcvc.github.io/r3ds/) | [arXiv](https://arxiv.org/abs/2403.12301) | [Data]()

<img src="docs/static/images/teaser.webp" alt="drawing" style="width:100%"/>

We introduce the Reality-linked 3D Scenes (R3DS) dataset of synthetic 3D scenes mirroring the real-world scene arrangements from Matterport3D. Compared to prior work, R3DS has more complete and densely populated scenes with objects linked to real-world observations in panoramas. R3DS also provides an object support hierarchy, and matching object sets (e.g., same chairs around a dining table) for each scene.
Overall, R3DS contains 19K objects represented by 3784 distinct CAD models from over 100 object categories. We demonstrate the effectiveness of R3DS on the Panoramic Scene Understanding task. We find that: 1) training on R3DS enables better generalization; 2) support relation prediction trained with R3DS improves performance compared to heuristically calculated support; and 3) R3DS offers a challenging benchmark for future work on panoramic scene understanding.


## Data

<img src="docs/static/images/scenes_model_color.webp" alt="drawing" style="width:100%"/>

R3DS has been hosted on HuggingFace at https://huggingface.co/datasets/3dlg-hcvc/rlsd. You can request access from the HuggingFace page and proceed to checkout the data:
```
git clone git@hf.co:datasets/3dlg-hcvc/rlsd
```

The dataset is structured into different folders:
```
mp3d_arch -- contains a subset of the Matterport3D architecture files that we have used
scenes -- contains the annotated json files for each scene
renderings -- contains various renderings of the annotated scene
    original_panoramas -- original panoramas (without annotations) from Matterport3D
    annotated_panoramas -- panorama renderings colored by object instance ids
    annotated_scene_hierarchy -- hierarchy of the annotated objects for each scene
    annotated_topdown -- topdown images of each annotated scene colored by object instance ids
annotated_model_ids.txt -- list of all model ids used to annotate the scenes
```

## TODO

- [ ] Add code reference to DPC experiments.

## Bibtex
If you find our work useful, please cite
```
@article{wu2024r3ds,
    title={R3DS: Reality-linked 3D Scenes for Panoramic Scene Understanding}, 
    author={Qirui Wu and Sonia Raychaudhuri and Daniel Ritchie and Manolis Savva and Angel X Chang},
    year={2024},
    eprint={2403.12301},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
```
