# CMDLA： A Chinese Manual Document Layout Analysis dataset
Thank you for your interest in our project.  Currently, the dataset is not publicly available as we are awaiting the review results of the related paper.  Once the review process is complete and the paper is approved, we will promptly release the dataset.  We appreciate your understanding and support!

## An example is provided below

### Example of Annotating Data Using LabelImg

![图片1](https://github.com/user-attachments/assets/cd6d9ae5-28b2-44bc-a4e4-d49313b42f77)

### Sample JSON File

```
[{"image": "page_100.png", "annotations": [{"label": "text", "coordinates": {"x": 353.8076923076923, "y": 79.07692307692307, "width": 586.0, "height": 73.0}}, {"label": "text", "coordinates": {"x": 655.3076923076924, "y": 208.07692307692307, "width": 811.0, "height": 85.0}}, {"label": "text", "coordinates": {"x": 194.30769230769232, "y": 205.57692307692307, "width": 83.0, "height": 56.0}}, {"label": "text", "coordinates": {"x": 302.3076923076923, "y": 303.57692307692304, "width": 167.0, "height": 64.0}}, {"label": "text", "coordinates": {"x": 642.8076923076924, "y": 581.0769230769231, "width": 782.0, "height": 431.00000000000006}}, {"label": "text", "coordinates": {"x": 511.3076923076923, "y": 1087.576923076923, "width": 523.0, "height": 276.0}}, {"label": "text", "coordinates": {"x": 451.3076923076924, "y": 1421.576923076923, "width": 419.00000000000006, "height": 66.0}}, {"label": "text", "coordinates": {"x": 299.3076923076923, "y": 875.5769230769231, "width": 165.0, "height": 62.0}}, {"label": "text", "coordinates": {"x": 295.3076923076923, "y": 1309.076923076923, "width": 165.0, "height": 63.0}}, {"label": "img", "coordinates": {"x": 936.8076923076924, "y": 1070.576923076923, "width": 264.0, "height": 264.0}}, {"label": "img", "coordinates": {"x": 885.8076923076924, "y": 1468.076923076923, "width": 308.0, "height": 231.0}}, {"label": "img", "coordinates": {"x": 132.80769230769232, "y": 212.57692307692307, "width": 52.0, "height": 48.0}}, {"label": "text", "coordinates": {"x": 155.80769230769232, "y": 307.07692307692304, "width": 56.0, "height": 63.0}}, {"label": "text", "coordinates": {"x": 156.80769230769232, "y": 875.5769230769231, "width": 50.0, "height": 70.0}}, {"label": "text", "coordinates": {"x": 153.30769230769232, "y": 1305.076923076923, "width": 47.0, "height": 79.0}}]}]
```

![989c6557e78f627ad00a276ebf58e10](https://github.com/user-attachments/assets/192a0b00-df1f-4c82-b300-af24faa1b110)

We input the instruction manual document into the RPLM model to obtain both textual and visual representations of the document.  These representations are then used for image-text matching and structured text information extraction, which together help in constructing a knowledge graph for the manual.  Using the data mentioned above as an example, the visualization of the constructed manual knowledge graph is shown in the following figure:


![graph (2)](https://github.com/user-attachments/assets/a2481803-aafd-49f2-abc4-ca4955c16439)




Please note that the dataset will be made publicly available after the paper review results are released.  Thank you for your understanding and support!
