## Assessment Results

| | Supervisor | Assessor | Mark |
| :- | :-: | :-: | :-: |
| [Specification](feedbacks/specification-annotated.pdf) | [N/A](feedbacks/specification-supervisor.pdf) | [60](feedbacks/specification-assessor.pdf) | 60 (15%) |
| [Interim Presentation](slides/main.pdf) | [71](feedbacks/interim-presentation-supervisor.pdf) | [66](feedbacks/interim-presentation-assessor.pdf) (Dr Alex Phillips stood in for Prof Jason Ralph) | 69 (15%) |
| [Bench Inspection](poster/main.pdf) | [79](feedbacks/bench-inspection-supervisor.pdf) | [73](feedbacks/bench-inspection-assessor.pdf) | 76 (15%) |
| [Thesis](thesis/main.pdf) (with one day late penalty) | [85 - 5](feedbacks/thesis-supervisor.pdf) | [81 - 5](feedbacks/thesis-assessor.pdf) | 78 (55%) |
| **Overall** | N/A | N/A | **74** |

[![HoD Engineering Ethics Prize (Minghong Xu - 22.23)](feedbacks/hod-engineering-ethics-prize.png)](feedbacks/hod-engineering-ethics-prize.pdf)

## Demonstrations

https://user-images.githubusercontent.com/86758413/233221789-9ce959f5-4895-4921-9393-2e0eda7233c8.mp4

https://user-images.githubusercontent.com/86758413/233221813-2f6d39f4-ada8-479b-97b9-0966306220dc.mp4

https://user-images.githubusercontent.com/86758413/233753293-8710ea58-4ea1-46d8-b928-f61924262766.mp4

Immediately after the submission of the thesis, someone released [a same project](https://github.com/tomasvr/turtlebot3_drlnav) and the performance is far better than mine.

## Activity Diary

```mermaid
gantt
    dateFormat  YYYY-MM-DD

    Literature review: literature_review, 2022-10-1, 90d
    Interim presentation: milestone, 2022-12-13,

    section Preparation
    Implement SOTA algos: 2022-10-24, 50d
    Sanity test the algos on popular environments: test_algo, 2022-11-15, 28d
    Algorithms are ready : milestone, 2022-12-13, 0d
    Spawn a robot into a simulator: load_robot, after test_algo, 3d
    Program the training env: program_env, after load_robot, 37d
    Match the interface between algo and env: match_interface,after program_env, 7d
    Training in an empty env: traning_in_empty_env, after match_interface, 9d
    Trained a workable policy in an empty env: milestone, 2023-2-7,

    section First Attempt
    Set up an indoor environment filled with obstacles for training: setup_indoor_env, after traning_in_empty_env, 7d
    Tinker the reward function: after setup_indoor_env, 7d
    Training in cluttered environment: training_in_cluttered_env, after setup_indoor_env, 14d
    Trained a policy for mapless navi: milestone, after training_in_cluttered_env

    section Training-Evaluation Loop
    Set up another environment for evaluating the performance of trained policy: setup_devel_env, after training_in_cluttered_env, 7d
    Repeat training and evaluating: train_eval, after setup_devel_env, 2023-03-23
    Bench inspection: milestone, after train_eval
```
