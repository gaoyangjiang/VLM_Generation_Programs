# Visual Benchmark Generation Tools

Python tools for building vision-language evaluation data with controllable visual perturbations, spatial relations, and optical illusions.

## Main components

| Area | Entry points |
| --- | --- |
| Spatial relations | [`standard_relation_generator.py`](standard_relation_generator.py), [`ultra_relation_generator.py`](ultra_relation_generator.py) |
| Noise and degradation | [`fast_noise_generator.py`](fast_noise_generator.py), [`noise_gradient_generator.py`](noise_gradient_generator.py), [`visual_degradation.py`](visual_degradation.py) |
| Illusion datasets | [`recreate_illusion_dataset.py`](recreate_illusion_dataset.py), [`fix_incomplete_illusions.py`](fix_incomplete_illusions.py) |
| Image collection | [`batch_download_images.py`](batch_download_images.py), [`collect_and_analyze_images.py`](collect_and_analyze_images.py) |
| Dataset organization | [`organize_vlm_benchmark.py`](organize_vlm_benchmark.py), [`merge_datasets.py`](merge_datasets.py), [`create_final_dataset.py`](create_final_dataset.py) |
| Evaluation and statistics | [`evaluation_framework.py`](evaluation_framework.py), [`detailed_dataset_analysis.py`](detailed_dataset_analysis.py) |

## Typical data flow

```text
Source images or synthetic scenes
    → Controlled transformations and parameter sweeps
    → Dataset organization and quality checks
    → Evaluation inputs and summary statistics
```

The scripts cover subject, relation, attribute, and illusion-oriented data preparation. Individual scripts expose different input assumptions and output locations; inspect the relevant script before generating data.

## Python dependencies

The tools use packages such as Pillow, NumPy, Matplotlib, OpenCV, svgwrite, CairoSVG, Requests, Beautiful Soup, and tqdm. Install the packages needed by the selected generator and prepare its source images separately.

## Additional documentation

- [Detailed historical overview](COMPLETE_README.md)
- [Benchmark-specific scripts](VLM_Comprehensive_Benchmark_scripts/)

This repository contains generation and preparation utilities. It is separate from the final data releases and their evaluation protocols.
