# Thinking about Multi-Task Learning

Thinking about how multi-task learning(MTL) works in NLP. Inspired by [the work from Ruder](https://arxiv.org/pdf/1706.05098.pdf).

The repository aims for thinking about the advantages of MTL in NLP. Why it works and how to choose the helpful auxiliary tasks for the main task. It may be a hard work. However, BERT, a hit model, also give us a reason to explore the rules of language or inference, which defines a neat task for the language model. 

## What is Multi-task learning

"Multitask Learning is an approach to inductive transfer that improves generalization by using the domain information contained in the training signals of related tasks as an inductive bias. It does this by learning tasks in parallel while using a shared representation; what is learned for each task can help other tasks be learned better." said by Rich Caruana, 1997.

## Motivation

1. Inspired by human learning, for learning new tasks, we often apply the knowledge we have acquired by learning related tasks. 
2. We can view multi-task learning as a form of inductive transfer. Inductive transfer can help improve a model by introducing an inductive bias, which generally leads to solutions that generalize better.

## Two MTL methods for Deep Learning
1. Hard Parameter Sharing
    1. get shared representation for different tasks
    2. reduces the risk of overfitting
    3. schematic diagram
    
    <div align=center>
    <img src="./imgs/hard.png" height="30%" width="30%" />
   </div>
2. Soft Parameter Sharing
    1. each task has its own model with its own parameters
    2. encourage the parameters to be similar using regulations
    3. schematic diagram
    
    <div align=center>
    <img src="./imgs/soft.png" height="60%" width="60%" />
   </div>
   
## Recent work on MTL for NLP
Keep updating...
1. **Sluice networks: Learning what to share between loosely related tasks.** *Ruder, S., Bingel, J., Augenstein, I., and Søgaard, A. .* AAAI 2019, [code](https://github.com/sebastianruder/sluice-networks)
    <div align=center>
    <img src="./imgs/sluice.png" height="60%" width="60%" />
   </div>

2. **Multi-Task Learning for Machine Reading Comprehension.** *Xu Y, Liu X, Shen Y, et al.* arXiv preprint arXiv:1809.06963, 2018.
    <div align=center>
    <img src="./imgs/mrc.png" height="60%" width="60%" />
   </div>
3. MS MARCO leaderboard: S-Net, V-Net... see [Analysis](https://github.com/IndexFziQ/MSMARCO-MRC-Analysis).


## Discussion
1. How to design suitable auxiliary tasks for the main task?
2. Shared representation and task-specific representation are of equal importance？
3. Noise from related tasks is helpful?

## References
1. Ruder S. An overview of multi-task learning in deep neural networks[J]. arXiv preprint arXiv:1706.05098, 2017.
2. Xu Y, Liu X, Shen Y, et al. Multi-Task Learning for Machine Reading Comprehension[J]. arXiv preprint arXiv:1809.06963, 2018.
3. Ruder, S., Bingel, J., Augenstein, I., and Søgaard, A. (2017). Sluice networks: Learning what to share between loosely related tasks. 
4. Caruana R. Multitask learning[J]. Machine learning, 1997, 28(1): 41-75.
5. Wikipedia: https://en.wikipedia.org/wiki/Multi-task_learning