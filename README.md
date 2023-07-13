## Assessment Results

| | Supervisor | Assessor | Mark |
| :- | :-: | :-: | :-: |
| [Specification](feedbacks/specification-annotated.pdf) | [N/A](feedbacks/specification-supervisor.pdf) | [60](feedbacks/specification-assessor.pdf) | 60 (15%) |
| [Interim Presentation](slides/main.pdf) | [71](feedbacks/interim-presentation-supervisor.pdf) | [66](feedbacks/interim-presentation-assessor.pdf) (Dr Alex Phillips stood in for Prof Jason Ralph) | 69 (15%) |
| [Bench Inspection](poster/main.pdf) | [79](feedbacks/bench-inspection-supervisor.pdf) | [73](feedbacks/bench-inspection-assessor.pdf) | 76 (15%) |
| [Thesis](thesis/main.pdf) (with one day late penalty) | [85 - 5](feedbacks/thesis-supervisor.pdf) | [81 - 5](feedbacks/thesis-assessor.pdf) | 78 (55%) |
| **Overall** | N/A | N/A | **74** |

## Demonstrations

https://user-images.githubusercontent.com/86758413/233221789-9ce959f5-4895-4921-9393-2e0eda7233c8.mp4

https://user-images.githubusercontent.com/86758413/233221813-2f6d39f4-ada8-479b-97b9-0966306220dc.mp4

https://user-images.githubusercontent.com/86758413/233753293-8710ea58-4ea1-46d8-b928-f61924262766.mp4

## Activity Diary

```mermaid
gantt
    dateFormat  YYYY-MM-DD

    Literature Review: literature_review, 2022-10-17, 2022-10-31

    section Preparation
    Implement a SOTA algo: 2022-10-24, 7d
    Test the algo on popular environments: test_algo, 2022-10-30, 2d
    Algorithm is ready : milestone, 2022-11-01, 0d

    section Sanity Test
    Load the robot into the simulator: load_robot, after test_algo, 3d
    Set a randomly generated target: generate_target, after load_robot, 5d
    Define the reward function: after generate_target, 7d
    Match the interface between algo and simulation: 2022-11-12, 2022-11-20
    Training: traning_in_empty_world, 2022-11-16, 2022-11-20
    Trained a policy in an empty world: milestone, 2022-11-20, 
    
    section Training
    Set up an indoor environment filled with obstacles for training: setup_indoor_env, after traning_in_empty_world, 7d
    Training in the indoor environment: training_in_indoor_env, after setup_indoor_env, 2022-12-16
    Trained a policy for mapless navi: milestone, after training_in_indoor_env

    section Training-Evaluation Loop
    Set up another environment for evaluating the performance of trained policy: setup_devel_env, after training_in_indoor_env, 7d
    Repeat Training & Evaluating loop: training_evaluating_loop, after setup_devel_env, 28d
    Select a policy which has the best performance on evaluating env: milestone, after training_evaluating_loop
```
