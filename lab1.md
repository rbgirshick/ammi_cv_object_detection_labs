# Lab 1: Detectron2 Warmup

In this practical session, we will familiarize ourselves with [Detectron2][d2], an object detection library written in PyTorch. Detectron2 implements state-of-the-art object detection models, like the ones you learned about in lecture. It also provides a "model zoo" -- a library of models trained on a variety of datasets. This allows users to download models and apply them to their own images. 

We will be going through the Detectron2 [tutorials][d2tut] which offer a step-by-step exploration of Detectron2.

Throughout this lab we will use colab notebooks to run detectron2 models. This is essential as the models will run much faster on the colab GPU compared to your personal laptops (which may only have CPUs). 

## Lab report submission
Please upload your short report in the form of `lab1_firstname_lastname.pdf` by Sunday, April 3, at midnight (in your local time). A dropbox upload link will be shared via Campuswire.

## Part A: Install Detectron2 

The first step is to install Detectron2 inside a colab notebook. It is recommended that you make a copy of the colab notebook to your personal google drive so that you can save any changes you make. (Alternatively, you can work in "playground mode," but you will be unable to save your changes.) The [install tutorial][d2inst] offers a step-by-step installation guidance. This should be relatively painless but if issues emerge the TAs are here to help!

## Part B: Run a pre-trained model for instance segmentation

Next, you will run a pre-trained model and use it on a set of images of your choice. The [example tutorial][d2run] in Detectron2 shows you how it's done; it loads a Mask R-CNN model with a ResNet-50-FPN backbone pre-trained on the [COCO][coco] dataset for the tasks of object detection and instance segmentation (to be covered in the next lecture) and runs it on an image. COCO is a dataset of ~120k images annotated with bounding boxes and object segmentation masks for 80 object categories. 

Pick a set of images from your personal collection (you can take a few of pictures of your apartment, or images that are on your phone or anywhere on the internet) and run the pre-trained model on them. Visualize the predictions.

## Part C: Run a pre-trained model for pose estimation 

In Part B, you loaded a model for instance segmentation, ran it through a few images from your collection, and visualized the predictions. In Part C, you are asked to repeat this process but now for the task of [human pose estimation][pose].

For this part, the [Detectron2 Model Zoo][d2zoo] will prove to be very helpful. You will need to find a suitable model and fill in the `CONFIG_FILE` variable in the notebook. When it's working correctly, you should see a "stick figure"-like skeleton drawn over each detected person. Again, take some images from your personal collection, run the model and visualize the predictions. 

## Part D: Report

We want you to summarize your findings and exploration with Detectron2 on a short report. 

__For each task__, namely instance segmentation (Part B) and human pose estimation (Part C), provide the following
* Model architecture: This should include the method, the backbone architecture and the dataset it was pretrained on.
* Examples: Visualizations of two examples of __correct__ predictions, and two examples of __incorrect__ predictions. In the caption of the figures, say why the examples are correct or incorrect.
* Observations: From running the models on your images, you must have observed some interesting model behavior (remember these models do not achieve 100% AP!). Provide some interesting example cases and describe why the behavior of the model is interesting or unexpected. 
* Error modes: In a short paragraph, describe the error modes that you have discovered when running the models. Have you seen a pattern of mistakes that keep occuring even on different images? Do you have any insight on what is causing the errors/confusions? 

The length of the report should not exceed 2 pages.

*Credits: This lab is adapted from the lab created by Georgia Gkioxari for the 2020 AMMI CV course.*

[d2]: https://github.com/facebookresearch/detectron2
[d2tut]: https://colab.research.google.com/drive/1wgg7IT8NrlxDeAmhYRjyHasg3jvwCnUd#scrollTo=QHnVupBBn9eR
[d2inst]: https://colab.research.google.com/drive/1wgg7IT8NrlxDeAmhYRjyHasg3jvwCnUd#scrollTo=9_FzH13EjseR
[d2run]: https://colab.research.google.com/drive/1wgg7IT8NrlxDeAmhYRjyHasg3jvwCnUd#scrollTo=dq9GY37ml1kr
[coco]: http://cocodataset.org/#home
[d2zoo]: https://github.com/facebookresearch/detectron2/blob/master/MODEL_ZOO.md
[pose]: https://colab.research.google.com/drive/1wgg7IT8NrlxDeAmhYRjyHasg3jvwCnUd#scrollTo=GYJrlXZC5M-J
