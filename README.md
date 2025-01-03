# [Lightweight G-YOLOv11: Advancing Efficient Fracture Detection in Pediatric Wrist X-rays](https://arxiv.org/abs/2501.00647)


<p align="center">
  <img src="figures/CAD diagram.png" width=48%>
  <img src="figures/G-yolov11 architecture.png" width=48%> <br>
  Schematic diagram of the proposed CAD system (left) based on the G-YOLOv11 detector (right) for localizing pediatric wrist trauma in X-ray images.
</p>

[Lightweight G-YOLOv11: Advancing Efficient Fracture Detection in Pediatric Wrist X-rays](https://arxiv.org/abs/2501.00647).\
Abdesselam Ferdi\
[![arXiv](https://arxiv.org/abs/2501.00647)]

<details>
  <summary>
  <font size="+1">Abstract</font>
  </summary>
Computer-aided diagnosis (CAD) systems have greatly improved the interpretation of medical images by radiologists and surgeons. However, current CAD systems for fracture detection in X-ray images primarily rely on large, resource-intensive detectors, which limits their practicality in clinical settings. To address this limitation, we propose a novel lightweight CAD system based on the YOLO detector for fracture detection. This system, named ghost convolution-based YOLOv11 (G-YOLOv11), builds on the latest version of the YOLO detector family and incorporates the ghost convolution operation for feature extraction. The ghost convolution operation generates the same number of feature maps as traditional convolution but requires fewer linear operations, thereby reducing the detector’s computational resource requirements. We evaluated the performance of the proposed G-YOLOv11 detector on the GRAZPEDWRI-DX dataset, achieving an mAP@0.5 of 0.535 with an inference time of 2.4 ms on an NVIDIA A10 GPU. Compared to the standard YOLOv11l, GYOLOv11l achieved reductions of 13.6% in mAP@0.5 and 68.7% in size. These results establish a new state-of-the-art benchmark in terms of efficiency, outperforming existing detectors.
</details>


## Performance
GRAZPEDWRI-DX dataset

| Model | Test Size | #Params | FLOPs | FScore | mAP<sup>{50}</sup> | mAP<sup>{50:95}</sup> | Inference Time |
|:---------------|:----:|:---:|:--:|:--:|:--:|:--:|
| [YOLOv8] |   			 640  |  43.636M  |  165.4G  |  69.8%  |  67.2%  |  40.3%  |  6.2ms  |
| [YOLOv9-C] | 			 640  |  25.536M  |  103.7G  |  68.2%  |  61.7%  |  38.9%  |  5.8ms  |
| [YOLOv9-E] | 			 640  |  58.152M  |  192.7G  |  71.1%  |  65.7%  |  44.2%  |  13.0ms |
| [YOLOv10] |   		 640  |  25.779M  |  127.3G  |  60.4%  |  56.8%  |  36%    |  6.7ms  |
| [YOLOv11] |   		 640  |  25.317M  |  87.3G   |  67.3%  |  61.9%  |  38.5%  |  5.5ms  |
| [G-YOLOv11 (ours)] |   640  |  7.794M   |  21.0G   |  61.2%  |  53.5%  |  34.1%  |  2.4ms  |


## Acknowledgement

The code is built with [ultralytics](https://github.com/ultralytics/ultralytics) and [YOLOv9-Fracture-Detection](https://github.com/RuiyangJu/YOLOv9-Fracture-Detection).

Great thanks to them! 

## Citation

If the code or models help your work, please cite my paper:
```BibTeX
@misc{ferdi2024lightweightgyolov11advancingefficient,
      title={Lightweight G-YOLOv11: Advancing Efficient Fracture Detection in Pediatric Wrist X-rays}, 
      author={Abdesselam Ferdi},
      year={2024},
      eprint={2501.00647},
      archivePrefix={arXiv},
      primaryClass={eess.IV},
      url={https://arxiv.org/abs/2501.00647}, 
}
```