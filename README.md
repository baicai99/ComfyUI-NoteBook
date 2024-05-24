# 中文
- [depth](zh/depth.zh.md)
- [line_art](zh/line_art.zh.md)
- [seg](zh/seg.zh.md)

# English
- [depth](en/depth.zh.md)
- [line_art](en/line_art.zh.md)
- [seg](en/seg.zh.md)

# ComfyUI-笔记本 20240522

## 总结
在本次测试中，  **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  和  **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**的表现最好，而  **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  的效果最差。

默认使用  **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  就好，  **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  只能识别全身，  **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  可以作为  **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  的补充。

## 工作流
工作流在下方，拖入ComfyUI就可以使用。
![workflow](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/92a66bc6-5d29-45ff-b5db-79de57e317cd)

## 语义分割测试：超大场景超小人物（复杂背景）

在超大场景超小人物的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  
   这两者的结合效果最佳，分割精准，无多余分割，适合复杂场景下的小目标识别。

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  
   效果次之，能识别目标，但会多识别一些不必要的部分。

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  
   效果最差，分割不够精准，容易识别多余部分，不推荐用于此类场景。

![复杂背景测试](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/5bfa483c-7a50-4aa3-8084-ad69f0dd014a)

## 语义分割测试：大场景小人物（简单背景）

在大场景小人物的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  
   这两者的结合效果最佳，分割精准，无多余分割，适合复杂场景下的小目标识别。

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  
   效果也非常好，但是抠图不如**Impact-Pack + segmentanything**精准，裙子还是有白边。

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  
   效果还行。

![简单背景测试](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/35bb681b-f647-457c-94c2-b4682eddc4f1)

## 语义分割测试：半身照

在半身照的测试中，我们比较了几种不同的语义分割工具的表现，三者表现都非常好：

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  

![半身照测试](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d67f0559-8bca-4c14-9773-b70cf57b79d1)

## 语义分割测试：胳膊(横屏半身照)

在横屏半身照测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  
   这个组合效果依然最佳，图片扣得非常干净。

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  
   完全不可用。这时候**segm** 明显落后于其他分割了，**segm** 进提供面部，手部，全身的选项，但我这里除了全身不报错意外，其他选项都会报错。

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  
   效果不错非常好，甚至比**Impact-Pack + segmentanything**还要好。
     
![胳膊](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/d3bc41c3-ef8a-4922-ad62-08af65b53d47)

## 语义分割测试：胳膊(全身照)

在全身照的测试中，我们比较了几种不同的语义分割工具的表现，结果如下：

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  
   这个组合效果依然最佳，图片扣得非常干净。

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  
   完全不可用。这时候**segm** 明显落后于其他分割了，**segm** 进提供面部，手部，全身的选项，但我这里除了全身不报错意外，其他选项都会报错。

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  
   效果不好，会识别多余的物体。
     
![胳膊(更小的全身照)](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/7a3eda69-5bf1-4c3e-99eb-af9605f95e66)

## 语义分割测试：胳膊(全身照)

在人物更小手臂更小的场景下，我比较了几种不同的语义分割工具的表现，结果如下：

1. **[Impact-Pack](https://github.com/ltdrdata/ComfyUI-Impact-Pack) + [segmentanything](https://github.com/storyicon/comfyui_segment_anything)**  
   虽然有多余的，但是对比与其他两个也是完美的存在。

2. **[segm](https://github.com/ltdrdata/ComfyUI-Impact-Pack)**  
   完全不可用。

3. **[Yoloworld ESAM](https://github.com/ZHO-ZHO-ZHO/ComfyUI-YoloWorld-EfficientSAM)**  
   效果不好，直接识别全身了。
     
![image](https://github.com/baicai99/ComfyUI-NoteBook/assets/101706274/dda4205e-cb60-4d50-a5b0-66261a515d78)




```git add .```  
```git commit -m "update seg.zh.md"```  
```git push```  