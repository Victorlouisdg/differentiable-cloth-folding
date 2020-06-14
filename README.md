# Differentiable Cloth Folding

![fold_optimized](/images/linear_15x15_opt.png)

This repository contains several notebooks which explain how to create a differentiable cloth simulation and how we can use it to fold cloth.
The image above shows such a fold after optimization.
These notebooks where made as part of my master's thesis. 

If you want to dive right in and see the cloth folding in action, check out [folding.ipynb](https://github.com/Victorlouisdg/differentiable-cloth-folding/blob/master/folding.ipynb).
For a gentle introduction to how the springs are simulated, see [springs.ipynb](https://github.com/Victorlouisdg/differentiable-cloth-folding/blob/master/springs.ipynb).
The [cloth.ipynb](https://github.com/Victorlouisdg/differentiable-cloth-folding/blob/master/cloth.ipynb) notebook shows how the spring model is used to simulate cloth.


Note that Github does not render the animations in the output of the notebooks and sometimes fails to render the notebooks entirely.
For the best experience, you can open the notebooks online in [Colab](https://colab.research.google.com/) or [NBViewer](https://nbviewer.jupyter.org/).


Feel free to open issues for questions or suggestions. You can contact me by email at victorlouisdg@gmail.com.

## Differentiable Simulation for Learning Control
In this section we briefly describe how differentiable simulation can be used to learn control.
The image below shows on the left a run of the the simulation S with a controller C.
The goal is to find parameters for the controller C that minimizie the loss.
We will do this by using the gradient of the loss function w.r.t. controller's parameters.
The gradient tells us, locally in which direction to change the controller's parameter to increase to loss the most.
We search for good parameters by iteratively taking small steps in the opposite direction of the gradient, this is called gradient descent.
The gradient is calculated by backpropagating through the simulation, as shown in the image below on the right.

![backprop](/images/forward_backward.png)

The usage of the backpropagated gradient is where learning control through differentiable simulation differs from other search techniques.
Other techniques, such as random search, evolutionary algorithms, reinforcement learning etc, use either approximations of the gradient or avoid using the gradient entirely.
However, because the gradient connects actions and consequences, we believe it can greatly speed up learning.
Our experiments show that learning to fold cloth through differentiable simulation is indeed very fast.
The fold in the image on top of this page was trained only for 100 training iterations, but already converged after 20 iterations (which equals only 20 seconds of simulated time).


We hope that these notebooks can show that writing such a differentiable simulation does not have to intimidating, and that learning control through differentiable simulation is possible.
Hopefully these notebook have spraked some interest in differentiable simulation and thanks for reading!

