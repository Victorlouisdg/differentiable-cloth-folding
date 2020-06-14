# Differentiable Cloth Folding

![fold_optimized](/images/linear_15x15_opt.png)

This repository contains several notebooks which explain how to create a differentiable cloth simulation and how we can use it to fold cloth.
These notebooks where made as part of my master thesis. 

If you want to dive right in and see the cloth folding in action, check out [folding.ipynb](https://github.com/Victorlouisdg/differentiable-cloth-folding/blob/master/folding.ipynb).
For a gentle introduction to how the springs are simulated, see [springs.ipynb](https://github.com/Victorlouisdg/differentiable-cloth-folding/blob/master/springs.ipynb).
The [cloth.ipynb](https://github.com/Victorlouisdg/differentiable-cloth-folding/blob/master/cloth.ipynb) notebook shows how the springs model is used to simulate cloth.


Note that Github does not render the animations in the output of the notebook and sometimes fails to render the notebooks entirely.
For the best experience, you can open the notebooks online in [Colab](https://colab.research.google.com/) or [NBViewver](https://nbviewer.jupyter.org/).


Feel free to open issues for questions or suggestions. You can contact me by email at victorlouisdg@gmail.com.

## Differentiable Simulation for Learning Control
In this section we briefly describe how differentiable simulation can be used for learning control.

![backprop](/images/forward_backward.png)
