# ComfyUI-Notebook 20240522

## Summary
In this test, **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)** and **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)** performed the best, while **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)** showed the poorest performance.

It is recommended to use **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)** by default. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)** can only recognize the whole body, and **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)** can serve as a supplement to **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**.

## Workflow
The workflow is shown below and can be used by dragging it into ComfyUI.
![workflow](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/92a66bc6-5d29-45ff-b5db-79de57e317cd)

## Semantic Segmentation Test: Large Scene with Tiny Person (Complex Background)
In the test of large scenes with tiny persons, we compared the performance of different semantic segmentation tools. The results are as follows:

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**
   This combination performed the best, with precise segmentation and no unnecessary segments, suitable for identifying small targets in complex scenes.

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**
   The performance was moderate, recognizing the target but also some unnecessary parts.

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**
   The performance was the worst, with imprecise segmentation and recognition of extra parts, not recommended for such scenarios.

![Complex Background Test](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/5bfa483c-7a50-4aa3-8084-ad69f0dd014a)

## Semantic Segmentation Test: Large Scene with Small Person (Simple Background)
In the test of large scenes with small persons, we compared the performance of different semantic segmentation tools. The results are as follows:

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**
   This combination performed the best, with precise segmentation and no unnecessary segments, suitable for identifying small targets in complex scenes.

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**
   The performance was also very good, but the cutout was not as precise as **Impact-Pack + segmentanything**, with some white edges on the skirt.

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**
   The performance was acceptable.

![Simple Background Test](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/35bb681b-f647-457c-94c2-b4682eddc4f1)

## Semantic Segmentation Test: Half-Body Photos
In the test of half-body photos, we compared the performance of different semantic segmentation tools, and all three performed very well:

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**

![Half-Body Photo Test](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d67f0559-8bca-4c14-9773-b70cf57b79d1)

## Semantic Segmentation Test: Arm (Landscape Half-Body Photo)
In the test of landscape half-body photos, we compared the performance of different semantic segmentation tools. The results are as follows:

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**
   This combination performed the best, with very clean cutouts.

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**
   Completely unusable. In this case, **segm** clearly lags behind the other segmentation tools, providing options for face, hand, and whole body, but except for the whole body, other options will result in errors.

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**
   The performance was very good, even better than **Impact-Pack + segmentanything**.

![Arm](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d3bc41c3-ef8a-4922-ad62-08af65b53d47)

## Semantic Segmentation Test: Arm (Full-Body Photo)
In the test of full-body photos, we compared the performance of different semantic segmentation tools. The results are as follows:

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**
   This combination performed the best, with very clean cutouts.

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**
   Completely unusable. In this case, **segm** clearly lags behind the other segmentation tools, providing options for face, hand, and whole body, but except for the whole body, other options will result in errors.

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**
   The performance was poor, recognizing extra objects.

![Arm (Smaller Full-Body Photo)](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/7a3eda69-5bf1-4c3e-99eb-af9605f95e66)

## Semantic Segmentation Test: Arm (Full-Body Photo)
In the test of scenarios with smaller persons and smaller arms, we compared the performance of different semantic segmentation tools. The results are as follows:

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**
   Although there are some extra parts, it is still perfect compared to the other two.

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**
   Completely unusable.

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**
   The performance was poor, directly recognizing the whole body.

![image](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/dda4205e-cb60-4d50-a5b0-66261a515d78)

```git add .```
```git commit -m "update seg.zh.md"```
```git push```