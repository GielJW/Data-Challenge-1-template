# Data-Challenge-1-template-code
This repository contains the template code for the TU/e course JBG040 Data Challenge 1.
Please read this document carefully as it has been filled out with important information.

## Code structure
The template code is structured into multiple files, based on their functionality. 
There are six `.py` files in total, each containing a different part of the code. 

- To download the data: run the `ImageDataset.py` file. The script will create a directory `/data/` and download the training and test data with corresponding labels to this directory. 
    - You will only have to run this script once usually, at the beginning of your project.

- To run the whole training/evaluation pipeline: run `main.py`. This script is prepared to:
    - Load your train and test data (Make sure its downloaded beforehand!)
    - Initializes the neural network as defined in the `Net.py` file.
    - Initialize loss functions and optimizers. If you want to change the loss function/optimizer, do it here.
    - Define number of training epochs and batch size
    - Check and enable GPU acceleration for training (if you have CUDA or Apple Silicon enabled device)
    - Train the neural network and perform evaluation on test set at the end of each epoch.
    - Provide plots about the training losses both during training in the command line and as a png (saved in the `/artifcats/` subdirectory)
    - Finally, save your trained model's weights in the `/model_weights/` subdirectory so that you can reload them later.

In your project, you are free to modify any parts of this code based on your needs. 
Note that the Neural Network structure is defined in the `Net.py` file, so if you want to modify the network itself, you can do so in that script.
The loss functions and optimizers are all defined in `main.py`.
Also feel free to create new files to explore the data or experiment with other ideas.

## GitHub setup instructions
1. Click the green *<> Code* button at the upper right corner of the repositiory.
2. Make sure that the tab *Local* is selected and click *Download ZIP*.
3. Go to the GitHub homepage and create a new repository.
4. Make sure that the repository is set to **private** and give it the name **JBG040-GroupXX**, where XX is your group number.
5. Press *uploading an exisiting file* and upload the extracted files from Data-Challenge-1-template-main.zip to your repository. Note that for the initial commit you should commit directly to the main branch
6. Invite your **group members, tutor and teachers** by going to *Settings > Collaborators > Add people*.
7. Open PyCharm and make sure that your GitHub account is linked.*
8. In the welcome screen of PyCharm, click *Get from VCs > GitHub* and select your repository and click on clone.
9. After the repository is cloned, you can now create a virtual environment using the requirements.txt.

*For information on how to install PyCharm and link Github to your PyCharm, we refer to the additional resources page on Canvas.


## Environment setup instructions
We recommend to set up a virtual Python environment to install all necessary packages. 
These packages are included in the `requirements.txt` file.
If you are using PyCharm, it should offer you the option to create this virtual environment from the requirements file.

## Submission instructions
After each sprint, you are expected to submit your code. This will **not** be done in Canvas, instead you will be creating a release of your current repository. 
A release is essentially a snapshot of your repository taken at a specific time. 
Your future modifications are not going to affect this release.
**Note that you are not allowed to update your old releases after the deadline.**
For more information on releases, see the [GitHub releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) page.

1. Make sure that your code is running without issues and that **everything is pushed to the main branch**.
2. Head over to your repository and click on *Releases* (located at the right-hand side).
3. Click on the green button *Create a new release*.*
4. Click on *Choose a tag*.
5. Fill in the textbox with **SprintX** where X is the current sprint number and press *Create new tag: SprintX*. 
6. Make sure that *Target: main* or *Target: master* (depending on your main/master branch) is selected, so that the code release will be based on your main branch. 
7. Fill in the title of the release with **Group XX Sprint X** where XX is your group number and X is the current sprint number.
8. Click the *Publish release* button to create a release for your sprint.
9. **Verify** that your release has been succesfully created by heading over to your repository and press the *Releases* button once again. There you should be able to see your newly created release.

*After the first release, you should click *Draft a new release* instead of *Create a new release*
