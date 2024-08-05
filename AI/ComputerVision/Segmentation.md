Segmentation is the process of identifying the areas in an image or video to identify set of characteristics

There are 4 types of segmentation
- Image
  - Divide image into groups of pixels (called contours or mask) based on some criteria
  - Process of taking an image or video and segment components or objects for better tracking and analysis
- Semantic
  - Identify a group of objects (by class) and assign a color
  - Identify objects say a cars, boys, dogs etc., in an image
- Instance
  - Extending the semantics segmentation, identify each instance of the class (mostly outline only)
  - Say, clearly segregate each car or each person. First step in object detection
  - Unlike object detection, here output is a contour containing the object
- Panoptic
  - Combination of semantic and instance