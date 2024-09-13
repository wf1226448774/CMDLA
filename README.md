# CMDLA： A Chinese Manual Document Layout Analysis dataset
Thank you for your interest in our project.  Currently, the dataset is not publicly available as we are awaiting the results of the related paper's review.  We will promptly release the dataset once the review process is complete and the paper is approved.  We appreciate your understanding and support!

## An example is provided below

### Example of Annotating Data Using LabelImg

<img src="https://github.com/wf1226448774/CMDLA/blob/main/page_100.png" width = "500"  align="center" />


### Sample JSON File
The dataset is stored as json files in folder "CMDLA/json", each entry has the following format:
```
[{
  "image": "page_100.png",
  "annotations": [
    {
      "label": "text",
      "coordinates":{
        "x": 353.8076923076923,
        "y": 79.07692307692307,
        "width": 586.0,
        "height": 73.0}
    },{
      "label": "text",
      "coordinates": {
        "x": 655.3076923076924,
        "y": 208.07692307692307,
        "width": 811.0,
        "height": 85.0}
    }, {
      "label": "text",
      "coordinates": {
        "x": 194.30769230769232,
        "y": 205.57692307692307,
        "width": 83.0,
        "height": 56.0}
    }, {"label": "text", "coordinates": {"x": 302.3076923076923, "y": 303.57692307692304, "width": 167.0, "height": 64.0}}, {"label": "text", "coordinates": {"x": 642.8076923076924, "y": 581.0769230769231, "width": 782.0, "height": 431.00000000000006}}, {"label": "text", "coordinates": {"x": 511.3076923076923, "y": 1087.576923076923, "width": 523.0, "height": 276.0}}, {"label": "text", "coordinates": {"x": 451.3076923076924, "y": 1421.576923076923, "width": 419.00000000000006, "height": 66.0}}, {"label": "text", "coordinates": {"x": 299.3076923076923, "y": 875.5769230769231, "width": 165.0, "height": 62.0}}, {"label": "text", "coordinates": {"x": 295.3076923076923, "y": 1309.076923076923, "width": 165.0, "height": 63.0}}, {"label": "img", "coordinates": {"x": 936.8076923076924, "y": 1070.576923076923, "width": 264.0, "height": 264.0}}, {"label": "img", "coordinates": {"x": 885.8076923076924, "y": 1468.076923076923, "width": 308.0, "height": 231.0}}, {"label": "img", "coordinates": {"x": 132.80769230769232, "y": 212.57692307692307, "width": 52.0, "height": 48.0}}, {"label": "text", "coordinates": {"x": 155.80769230769232, "y": 307.07692307692304, "width": 56.0, "height": 63.0}}, {"label": "text", "coordinates": {"x": 156.80769230769232, "y": 875.5769230769231, "width": 50.0, "height": 70.0}}, {"label": "text", "coordinates": {"x": 153.30769230769232, "y": 1305.076923076923, "width": 47.0, "height": 79.0}}]}]
```

### Sample KG File

We input the instruction manual document into the RPLM model to obtain both textual and visual representations of the document.  These representations are then used for image-text matching and structured text information extraction, which together help in constructing a knowledge graph for the manual. Using the data mentioned above as an example, the constructed manual knowledge graph is shown as follows.

```
安装步骤,Contain,注意事项
安装步骤,Contain,连接电源
安装步骤,Contain,调整底脚
注意事项,Contain,1.检查干衣护理机在运输过程中是否有损坏，损坏的干衣护理机不得进行通电，若出现损坏，请联络产品供应商。
注意事项,Contain,2.干衣护理机应安装在干燥、通风的环境中，不能安装在湖湿、充满蒸汽和水能够淋到的地方(如浴室、露天阳台、水龙头旁)，不能放置在阳光直射的地方。
注意事项,Contain,3.干衣护理机附近请勿使用烤火炉、瓦斯器具等，避免危险
注意事项,Contain,4.为了干衣护理机能够更好的工作，环境温度不要低于5℃，也不要高于35℃。
注意事项,Contain,5.干衣护理机应水平安装，其底部装有可调底脚，在使用之前应将四个底脚调节成水平状态。
注意事项,Next,连接电源
连接电源,Contain,接通电源需注意以下几点
连接电源,Contain,1.电源插座是否能承受干衣护理机的最大功率
连接电源,Contain,2.电源电压符合要求。
连接电源,Contain,3.电源插座应与千农护理机插头一致。
连接电源,Contain,4.干衣护理机必须可靠接地。
连接电源,Next,调整底脚
调整底脚,Contain,使用之前需调整四个底脚
1.检查干衣护理机在运输过程中是否有损坏，损坏的干衣护理机不得进行通电，若出现损坏，请联络产品供应商。,Next,2.干衣护理机应安装在干燥、通风的环境中，不能安装在湖湿、充满蒸汽和水能够淋到的地方(如浴室、露天阳台、水龙头旁)，不能放置在阳光直射的地方。
2.干衣护理机应安装在干燥、通风的环境中，不能安装在湖湿、充满蒸汽和水能够淋到的地方(如浴室、露天阳台、水龙头旁)，不能放置在阳光直射的地方。,Next,3.干衣护理机附近请勿使用烤火炉、瓦斯器具等，避免危险
3.干衣护理机附近请勿使用烤火炉、瓦斯器具等，避免危险,Next,4.为了干衣护理机能够更好的工作，环境温度不要低于5℃，也不要高于35℃。
4.为了干衣护理机能够更好的工作，环境温度不要低于5℃，也不要高于35℃。,Next,5.干衣护理机应水平安装，其底部装有可调底脚，在使用之前应将四个底脚调节成水平状态。
接通电源需注意以下几点,Contain,图像1
接通电源需注意以下几点,Next,1.电源插座是否能承受干衣护理机的最大功率
1.电源插座是否能承受干衣护理机的最大功率,Next,2.电源电压符合要求。
2.电源电压符合要求。,Next,3.电源插座应与千农护理机插头一致。
3.电源插座应与千农护理机插头一致。,Next,4.干衣护理机必须可靠接地。
使用之前需调整四个底脚,Contain,图像2
```

The above data has been stored on the Neo4j platform and visualized as shown in the following diagram.

<img src="https://github.com/wf1226448774/CMDLA/blob/main/graph.svg" width = "600"  align="center" />




Please note that the dataset will be made publicly available after the paper review results are released.  Thank you for your understanding and support!
