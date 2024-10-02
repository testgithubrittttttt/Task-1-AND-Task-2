# Generative AI Product Photography and Video Creation

## Table of Contents
- Project Overview
- Requirements
- Task 1: Product Image Generation
  - Approach
  - Execution
- Task 2: Video Creation
  - Approach
  - Execution
- How to Run
- Conclusion

## Project Overview
This project explores using Generative AI techniques for creating realistic product photographs and video outputs. The primary goal is to simulate professional product photography using AI by generating natural scenes with a given product (like a coffee cup) and then animating the product within the scene to create video content.

This project is divided into two tasks:

Task 1: Generating a realistic image of a product (coffee cup) placed in a naturally coherent background scene based on a text prompt.
Task 2: Create a video by generating multiple consistent frames with transitions (such as zooming out) and combining these frames into a video.

## Requirements
To successfully run this project, you need the following:

- Python 3.7 or higher
- Google Colab or a local Python environment
- The following Python libraries:
  - torch (for running the AI models)
  - diffusers (for the Stable Diffusion pipeline)
  - Pillow (for image manipulation)
  - opencv-python (for video generation)
 
!pip install torch torchvision torchaudio
!pip install diffusers[torch]
!pip install opencv-python-headless
!pip install Pillow

## Task 1: Product Image Generation
- Goal
The objective of Task 1 is to generate a realistic product image. Given an object image (such as a coffee cup) and a text prompt describing the scene, the goal is to place the object naturally within the generated background based on the text prompt.

- Approach
  - Object Placement: The given object (coffee cup) should remain unaltered but be resized and placed in the scene based on the background generated from the text prompt.
  - Scene Coherence: The generated scene must look natural, ensuring that lighting, spatial placement, and object aspect ratio match the background.
  - Text Prompting: The background scene is created based on the user's input text prompt, which describes the desired environment (e.g., "A cozy kitchen with natural light").
 
- Execution
  - The project uses Stable Diffusion via the diffusers library to generate the background image based on the text prompt.
  - The PIL library opens, resizes, and places the object image (coffee cup) onto the generated background.
  - The final image is saved after compositing the object into the background.
 
## Task 2: Video Creation
- Goal
Task 2 aims to create a video output by generating multiple frames with consistent transitions, such as a zoom-out effect or object movement. These frames are then combined into a video.

- Approach
  - Frame Generation: For each frame, either the object is resized (to simulate zooming out) or moved slightly to create a natural transition.
  - Combining Frames into Video: Once all the frames are generated, they are combined into a video using the opencv-python library.
  - Consistency: The object (coffee cup) should remain consistently integrated into the scene across all frames.

- Execution
  - Multiple Frames: The project generates a sequence of images where the object gradually zooms out or moves within the background.
  - Video Creation: The frames are combined into a video at a specified frame rate using OpenCV.
 
## How to Run
Running in Google Colab
- Install Dependencies: Use the !pip install commands listed under the Requirements section to install necessary libraries in Colab.

- Upload Object and Background Images: Use the following to upload your object and background images (if needed):
   code = from google.colab import files
          uploaded = files.upload()
  
- Running Task 1: After uploading the images, run the code for Task 1 to generate a realistic product image based on your object and prompt.

- Running Task 2: Run the frame generation and video creation code to create a video showing the object in motion (e.g., zooming out).

## Conclusion
This project demonstrates how Generative AI can be leveraged for creative workflows like product photography and video content creation. Using Stable Diffusion for text-conditioned scene generation and tools like OpenCV for video creation, we successfully:

- Generated realistic product images (Task 1).
- Created videos showing dynamic transitions, such as zooming out (Task 2).
This assignment showcases the power of AI in automating complex tasks like scene generation, object placement, and video creation, which would traditionally require manual effort and expensive equipment.

## Outputs
- this is the screenshot of the output for task 1 = ![image](https://github.com/user-attachments/assets/6ae25408-1b1c-495c-9b8b-12dcef2cd4c9)

- output of the second video is in video which is also in the repository.
