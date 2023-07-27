# Snapchat_EitherOrQuizz
Create the popular either-or quizz very easily with this demo project!

How to use this template:
1. Read the Instruction card and/or the QuizzTree.js script
2. Exchange the images and texts in the Choices Tree Hierarchy
3. If you want to add more questions / choices to the tree, simply add 2 children under the scene object that represents the last answer leading to the choice.
4. Make sure your new children have a ScreenImage component with the texture you want to see in the background
5. Make sure your new children also have a text component with a descriptive name of the choice
6. If you want to delete a choice, simply delete the two scene objects in question
7. Left choice will add a 0 to the final trigger, right choice will add a 1. I called this the "choicesPath" in the script.
8. Make sure you set up behaviour scripts for each outcome trigger (e.G. 001, 010,...) or use the alternative results script to trigger certain events for each outcome

How it works:
The ChoicesTree that you edit is only there to hold image & text references for the quizz and is not visible at any time.
These references will be used to set the new textures/texts in the "Final Backgrounds" Scene Objects.
The Quizztree.js script checks each round, if the scene object of the chocie you made has (exactly) two children.
If yes, we set the new textures/texts from these children into the final background images and continue with the quizz loop.
If not, the quizz is finished and we send out the choices path as a trigger.
