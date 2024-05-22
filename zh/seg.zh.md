# ComfyUI-笔记本 20240521

## 总结
在本次测试中，**Impact-Pack + segmentanything**和**Yoloworld ESAM**的表现最好，而**segm**的效果最差。  
默认使用**Impact-Pack + segmentanything**就好，**segm**只能识别全身，**Yoloworld ESAM**可以作为**Impact-Pack + segmentanything**的补充。

## 工作流
工作流在下方，拖入ComfyUI就可以使用。
![workflow](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/92a66bc6-5d29-45ff-b5db-79de57e317cd)

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
   效果也非常好，但是抠图不如**Impact-Pack + segmentanything**精准，裙子还是有白边。
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   效果还行。
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

## 语义分割测试：胳膊(半身照)

在大场景小人物的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **Impact-Pack + segmentanything**  
   这个组合效果依然最佳，图片扣得非常干净。
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   完全不可用。这时候**segm** 明显落后于其他分割了，**segm** 进提供面部，手部，全身的选项，但我这里除了全身不报错意外，其他选项都会报错。
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   效果不错非常好，甚至比**Impact-Pack + segmentanything**还要好。
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)
     
![胳膊](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d3bc41c3-ef8a-4922-ad62-08af65b53d47)

## 语义分割测试：胳膊(全身照)

在大场景小人物的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **Impact-Pack + segmentanything**  
   这个组合效果依然最佳，图片扣得非常干净。
   - [Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack)
   - [segmentanything](https://github.com/storyicon/comfyui_segment_anything)

2. **segm**  
   完全不可用。这时候**segm** 明显落后于其他分割了，**segm** 进提供面部，手部，全身的选项，但我这里除了全身不报错意外，其他选项都会报错。
   - [segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)

3. **Yoloworld ESAM**  
   效果不好，会识别多余的物体。
   - [Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)
     
![胳膊](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d3bc41c3-ef8a-4922-ad62-08af65b53d47)