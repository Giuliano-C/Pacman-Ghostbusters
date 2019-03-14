# Pacman-Ghostbusters


In this project, I designed Pacman agents that use sensors to locate and eat invisible ghosts. The main goal was to advance from locating single, stationary ghosts to hunting packs of multiple moving ghosts with ruthless efficiency.

## Part 1 - Exact Inference Observation

This correctly updates the agent's belief distribution over ghost positions given an observation from Pacman's sensors. The implementation also handle one special case: 

- when a ghost is eaten, you should place that ghost in its prison cell.

```bash
$ python autograder.py -q q1
```

## Part 2 - Exact Inference with Time Elapse

The reading indicating the ghost is very far is likely to be the result of a buggy sensor. Pacman's prior knowledge of how the ghost may move will decrease the impact of this reading since Pacman knows the ghost could not move so far in only one move.

```bash
$ python autograder.py -q q2
```

As an example of the GoSouthGhostAgent

```bash
$ python autograder.py -t test_cases/q2/2-ExactElapse
```

## Part 3 - Exact Inference Full Test

The agent should first find the most likely position of each remaining (uncaptured) ghost, then choose an action that minimizes the distance to the closest ghost. 

```bash
$ python autograder.py -q q3
```

## Part 4 - Approximate Inference Observation

The implementation handles two special cases:

1. When all your particles receive zero weight based on the evidence, you should resample all particles from the prior to recover.

2. When a ghost is eaten, you should update all particles to place that ghost in its prison cell, as described in the comments of observe. 

When complete, Pacman should be able to track ghosts nearly as effectively as with exact inference.

```bash
$ python autograder.py -q q4
```

## Part 5 - Approximate Inference with Time Elapse

Pacman should be able to track ghosts nearly as effectively as with exact inference.

```bash
$ python autograder.py -q q5
```

To see which ghost is used for each test case you can look in the .test files. As an example, you can run

```bash
$ python autograder.py -t test_cases/q5/2-ParticleElapse
```


## Part 6 - Joint Particle Filter Observation

The implementation handles two special cases. 

1. When all your particles receive zero weight based on the evidence, you should resample all particles from the prior to recover.

2. When a ghost is eaten, you should update all particles to place that ghost in its prison cell, as described in the comments of observeState.

```bash
$ python autograder.py -q q6
```

## Part 7 - Joint Particle Filter with Elapse Time

```bash
$ python autograder.py -q q7
```





