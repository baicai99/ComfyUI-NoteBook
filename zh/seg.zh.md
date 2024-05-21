# ComfyUI-笔记本 20240521

## 总结
在本次测试中，**Impact-Pack + segmentanything**和**segm**的表现最好，而**Yoloworld ESAM**的效果最差。

## 语义分割测试：超大场景超小人物（复杂背景）

在超大场景超小人物的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **Impact-Pack + segmentanything**  
   这两者的结合效果最佳，分割精准，无多余分割，适合复杂场景下的小目标识别。
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   效果次之，能识别目标，但会多识别一些不必要的部分。
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   效果最差，分割不够精准，容易识别多余部分，不推荐用于此类场景。
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)

![复杂背景测试](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/5bfa483c-7a50-4aa3-8084-ad69f0dd014a)

## 语义分割测试：大场景小人物（简单背景）

在大场景小人物的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **Impact-Pack + segmentanything**  
   这两者的结合效果最佳，分割精准，无多余分割，适合复杂场景下的小目标识别。
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   效果次之，能识别目标，但会多识别一些不必要的部分。
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   效果最差，分割不够精准，容易识别多余部分，不推荐用于此类场景。
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)

![简单背景测试](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/35bb681b-f647-457c-94c2-b4682eddc4f1)

## 语义分割测试：半身照

在半身照的测试中，我们比较了几种不同的语义分割工具的表现，三者表现都非常好：

1. **Impact-Pack + segmentanything**  
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)

![半身照测试](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d67f0559-8bca-4c14-9773-b70cf57b79d1)
