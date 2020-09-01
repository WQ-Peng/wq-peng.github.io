# Ways to accelerate MATLAB computation

> There's a machine learning task on MATLAB recently. At first, it tooks 80 days to train the model which is not practical at all. So I tried several ways to accelerate the training process.

---

## 1. Vectorization
MATLAB has made optimazition for "loop" computation, so using vector is usually more efficient than using  `for` loop.

However, in my machine learning tasks, the computation of the following matrix takes the longest time, which means that vectorization cannot be implemented here.

![matrix Q](https://raw.githubusercontent.com/WQ-Peng/repo_image/master/MATLAB_parallel/1.png)

Each element `Q(i,j)` in the matrix depends on the neighbouring elements, so the computation must be done with `for` loop.

## 2. parallel computing with GPU 
The workstation in the lab is equited with two 2080ti GPUs, so I was wondering it might be faster to compute on GPUs. However, due to I/O-intensive nature of the task, it did not work with GPUs.

![MATLAB parallel solution](https://raw.githubusercontent.com/WQ-Peng/repo_image/master/MATLAB_parallel/2.png)

## 3. `parfor` 
Another parallel tool provided by MATLAB is `parfor` , which allows you to implements parallel computing on CPU.

![`parfor`](https://raw.githubusercontent.com/WQ-Peng/repo_image/master/MATLAB_parallel/3.png)

By exchange `for` loop into `parfor` loop, one can devide the computation task into several MATLAB works which run simultaneously.
Thanks to the multi-cores CPU on the workstation, the computation task was done with in 5 days.

![](https://raw.githubusercontent.com/WQ-Peng/repo_image/master/MATLAB_parallel/4.png)
![](https://raw.githubusercontent.com/WQ-Peng/repo_image/master/MATLAB_parallel/5.png)
