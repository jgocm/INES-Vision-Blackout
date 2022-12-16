# INES-Vision-Blackout
Modeling Finite State Machines for solving autonomous robotics navigation challenges

## Steps to open project
1. Run eclipse
2. Set your workspace directory to INES-Vision-Blackout/workspace and Launch
![image](https://user-images.githubusercontent.com/85940536/202816339-48849ccb-68a8-4b24-84b7-ff695e17de76.png)
3. Import project into workspace folder:

![image](https://user-images.githubusercontent.com/85940536/208133009-bf68d74d-4997-40c6-8ca3-3ff4e066a477.png)
![image](https://user-images.githubusercontent.com/85940536/208133244-4da26746-7bfd-4934-a262-aba90616d7d1.png)
![image](https://user-images.githubusercontent.com/85940536/208133888-b0c36932-49da-494b-9280-778543f18c84.png)

## Vision Blackout base structure
Finite State Machine inputs:
- frameHasBall: boolean
- frameHasRobot: boolean
- frameHasGoal: boolean
- Ball: x, y, theta
- Robot: x, y, theta
- Goal: x, y, theta

Finite State Machine outputs:
- Target: x, y, theta
- NavigationType: enum(driveToPoint, rotateOnSelf, rotateInPoint)
- Kick: boolean

![blackout2023](https://user-images.githubusercontent.com/85940536/204012984-0692724d-237b-412b-bdeb-6284ca50c50a.png)

## Source Code
Currently, the project is under minor refactors, due to ongoing researches on robot self-localization. So, ball grabbing is the only working skill on the current master branch.

SSL Vision Blackout source code: https://github.com/jgocm/ssl-detector

Current main code is located at: https://github.com/jgocm/ssl-detector/blob/master/src/stage1_refactor.py

![image](https://user-images.githubusercontent.com/85940536/204016679-12970195-c3dc-4922-8ded-efeae14eabab.png)

[fsm.py](https://github.com/jgocm/ssl-detector/blob/master/src/fsm.py) implements finite state machines for solving the [SSL Vision Blackout Challenge](https://robocup-ssl.github.io/technical-challenge-rules/2022-ssl-vision-blackout-rules.pdf) stages:
- Stage 1: Grab a stationary ball on the field
- Stage 2: Score on an empty goal
- Stage 3: Move to specific coordinates on the field
- Stage 4: Pass the ball to an ally robot and score
