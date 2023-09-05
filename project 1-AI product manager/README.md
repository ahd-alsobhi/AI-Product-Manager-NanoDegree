### **Project Overview**

Your goal, as a product owner is to build a product that helps doctors quickly identify cases of pneumonia in children. You'll want to build a classification system that


- Can help flag serious cases
- Quickly identify healthy cases
- And, generally, act as a diagnostic aid for doctors

As such, this project is designed to test your ability to build a labeled dataset that distinguishes between healthy and pneumonia x-ray images; this can be used by ML engineers later on down the line to build a classification product. Your main task will be to create a data labeling job using [Appen's platform](https://client.appen.com/jobs). If you have not yet, you'll need to create an Appen account and log in to complete this project.

If you intend to purchase any services through Appen, you'll want to use a valid business email so you can receive notifications. But for the project, if you do not have a business email, you can use the above workaround in the meantime. You will not be required to actually launch the data labeling job, you'll be evaluated on submitted documents and design only.

**The Data**
The dataset you'll be given is a modified version of this [Kaggle chest x-ray dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia), with most labels removed. Every piece of data is a chest x-ray image. You may see images taken that are slightly different in size and taken under slightly different exposure times. A typical, labeled image is shown below.
![annotated-chest-xray](https://github.com/ahd-alsobhi/AI-Product-Manager-NanoDegree/assets/109044858/4ce4a7c2-80c8-4e44-92c5-217e3d8a8ed5)
A labeled, healthy, chest x-ray image. Pay close attention to the two lungs and diaphragm (below the lungs).

**What Does Pneumonia Look Like?**
This is a challenging task because it is not always clear when pneumonia symptoms are present or not in an image. As such, your system is not meant to be a replacement for a doctor, only to aid in quickly identifying healthy patients and surfacing potential cases of pneumonia.

You should design a data annotation job, such that a non-expert can identify more noticeable cases of pneumonia. Since you are designing for a non-expert annotator, you should design for failure; this means including some way to capture uncertainty in your data labels and test questions.

So, what indicates pneumonia and what kind of advice and examples can we give potential annotators?
There are a few different visual symptoms that indicate pneumonia. The most important areas to have annotators pay attention to are the lungs and the diaphragm.

- A normal, healthy image will depict clear lungs without any areas of abnormal cloudiness/opacity; there may be structured, web-like vasculature in the lungs but otherwise, that area should be clear. In healthy images, you are also more likely to see a diaphragm shadow.

- A pneumonia image may include a few things: areas of cloudiness/opacity in several concentrated areas or one large area. You may also see a general pattern of opacity that obscures the structure of the lungs, heart and diaphragm.
![healthy-example](https://github.com/ahd-alsobhi/AI-Product-Manager-NanoDegree/assets/109044858/44253267-1ecb-42c4-8791-7c94775b8ac7)
Some characteristics of a healthy image: is a clear lung area.

**Designing a Data Labeling Job**
One of your biggest tasks will be to design an appropriate data labeling job using [Appen's platform](https://client.appen.com/jobs). You will need to submit an HTML file of a complete job Preview, which includes: 1. Instructions for annotation and 2. Example test questions. You will also need to submit a Proposal document that discusses the design of the job and steps you'll take for quality assurance.

You will not need to launch the annotation job; you are only creating one to demonstrate your ability to create a dataset.

**Good Annotator Instructions (Handling Uncertainty)**
This is a very challenging classification task and so you should provide clear examples and instructions to potential annotators.

- You may choose to have annotators try to label an image as pneumonia or not (binary classification); if this is the case, you should include an Unknown or Other option to account for uncertainty in an annotation.

- You may also choose to have annotators describe how likely they think a case of pneumonia is in a given image, and you could measure this on a numerical scale; 0-n for their confidence that an image contains pneumonia symptoms or not. A scale like this automatically includes room for low-confidence and uncertainty.

- In your Proposal document, you will discuss your design choices and methods for quality assurance.

It is suggested that you start with an Appen job-template, and customize it to this particular task. And you can read more about the platform, next.

**The Data**
You are given a data file xray_image_data.csv (filename may have dashes instead of underscores), which contains a column of image url's and a label column. You can copy-paste any image url into your browser to see an image in its entirety. Of over 100 images in this dataset, only 16 of them are labeled, and so you'll still need to create a job to create a completely labeled dataset. The provided labels are so that you can take a look at known pneumonia/healthy cases, note any visual patterns, and create accurate test questions.

It is recommended that you use an [appropriate Appen template](https://make.figure-eight.com/welcome) as a starting point for this image classification project.
