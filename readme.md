## Demonstrations

https://user-images.githubusercontent.com/86758413/233221789-9ce959f5-4895-4921-9393-2e0eda7233c8.mp4

https://user-images.githubusercontent.com/86758413/233221813-2f6d39f4-ada8-479b-97b9-0966306220dc.mp4

https://user-images.githubusercontent.com/86758413/233753293-8710ea58-4ea1-46d8-b928-f61924262766.mp4

Immediately after the submission of the thesis, someone released [a same project](https://github.com/tomasvr/turtlebot3_drlnav) and the performance is far better than mine.

## Assessment Results

| | Supervisor | Assessor | Mark |
| :- | :-: | :-: | :-: |
| [Specification](feedback/specification-annotated.pdf) | [N/A](feedback/specification-supervisor.pdf) | [60](feedback/specification-assessor.pdf) | 60 (15%) |
| [Interim Presentation](slides/main.pdf) | [71](feedback/interim-presentation-supervisor.pdf) | [66](feedback/interim-presentation-assessor.pdf) (Dr Alex Phillips stood in for Prof Jason Ralph) | 69 (15%) |
| [Bench Inspection](poster/main.pdf) | [79](feedback/bench-inspection-supervisor.pdf) | [73](feedback/bench-inspection-assessor.pdf) | 76 (15%) |
| [Thesis](thesis/thesis.pdf) (with one day late penalty) | [85 - 5](feedback/thesis-supervisor.pdf) | [81 - 5](feedback/thesis-assessor.pdf) | 78 (55%) |
| **Overall** | N/A | N/A | **74** |

[![HoD Engineering Ethics Prize (Minghong Xu - 22.23)](feedback/hod-engineering-ethics-prize.png)](feedback/hod-engineering-ethics-prize.pdf)

## Activity Diary

```mermaid
gantt
    dateFormat  YYYY-MM-DD

    Literature review: literature_review, 2022-10-1, 90d
    Interim presentation: milestone, 2022-12-13,

    section Preparation
    Implement SOTA algos: 2022-10-24, 50d
    Sanity test the algos on popular environments: test_algo, 2022-11-15, 28d
    Algorithms were ready : milestone, 2022-12-13, 0d
    Spawn a robot into a simulator: load_robot, after test_algo, 3d
    Program the training env: program_env, after load_robot, 37d
    Match the interface between algo and env: match_interface,after program_env, 7d
    Training in an empty env: traning_in_empty_env, after match_interface, 9d
    Trained a workable policy in an empty env: milestone, 2023-2-7,

    section First Attempt
    Set up an indoor environment filled with obstacles for training: setup_indoor_env, after traning_in_empty_env, 7d
    Tinker the reward function: after setup_indoor_env, 10d
    Training in a cluttered environment: training_in_cluttered_env, after setup_indoor_env, 14d
    Observable intelligent mapless navigation behaviour: milestone, after training_in_cluttered_env

    section Training-Evaluation Loop
    Set up another environment for evaluating the performance of trained policy: setup_devel_env, after training_in_cluttered_env, 7d
    Repeat training and evaluating: train_eval, after setup_devel_env, 2023-03-23
    Bench inspection: milestone, after train_eval

    section Bachelor's Thesis
    Collect figures: 2023-03-23, 8d
    Compose: 2023-03-23, 2023-04-18
    Edit and proofread: 2023-04-18, 2023-04-20
    Submitted: milestone, 2023-04-20
```
