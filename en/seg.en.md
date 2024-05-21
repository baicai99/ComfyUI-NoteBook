# ComfyUI-Notebook 20240521

## Summary
In this test, **Impact-Pack + segmentanything** and **segm** performed the best, while **Yoloworld ESAM** had the worst performance.

## Semantic Segmentation Test: Large Scene with Small Figures (Complex Background)

In the test with large scenes and small figures, we compared the performance of several different semantic segmentation tools, with the following results:

1. **Impact-Pack + segmentanything**  
   This combination had the best results, with precise segmentation and no redundant segmentation, making it suitable for small target recognition in complex scenes.
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   This tool was the second-best, capable of identifying targets but also recognizing some unnecessary parts.
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   This tool had the worst performance, with imprecise segmentation and a tendency to recognize unnecessary parts, not recommended for such scenes.
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)

![Complex Background Test](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/5bfa483c-7a50-4aa3-8084-ad69f0dd014a)

## Semantic Segmentation Test: Large Scene with Small Figures (Simple Background)

In the test with large scenes and small figures, we compared the performance of several different semantic segmentation tools, with the following results:

1. **Impact-Pack + segmentanything**  
   This combination had the best results, with precise segmentation and no redundant segmentation, making it suitable for small target recognition in complex scenes.
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   This tool was the second-best, capable of identifying targets but also recognizing some unnecessary parts.
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   This tool had the worst performance, with imprecise segmentation and a tendency to recognize unnecessary parts, not recommended for such scenes.
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)

![Simple Background Test](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/35bb681b-f647-457c-94c2-b4682eddc4f1)

## Semantic Segmentation Test: Half-Body Portrait

In the test with half-body portraits, we compared the performance of several different semantic segmentation tools, with all three performing very well:

1. **Impact-Pack + segmentanything**  
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)

![Half-Body Portrait Test](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d67f0559-8bca-4c14-9773-b70cf57b79d1)