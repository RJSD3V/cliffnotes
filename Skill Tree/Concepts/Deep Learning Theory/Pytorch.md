Open source machine learning framework that accelerates the path from research prototyping to production deployment. 


- NN Layer types, activation and loss functions, optimizers. 
- Autograd - Autmatic Differentiation Engine
- TorchScript, TorchServe, Quantization


### Tensors - Currency of Pytorch. 

```
import torch
z = torch.zeros(5, 3)
r1 = torch.ones((2,2), dtype=torch.int16)
print(r1)
torch.manual_seed(1729)
r1 = torch.rand(2,2)
print(f"A Random Tensor: {r1}")
# Miscellaneous mathematical functions 

torch.abs(r)
torch.asin(r)
torch.det(r)
torch.svd(r)
torch.std_mean(r)
torch.max(r)
torch.min(r)
```


Element-wise multiplication and addition of tensors with the same shape. 


### Automated Differentiation Engine - Autograd

Computation as a graph built at Runtime

Each tensor generated from the computation graphs knows how it came to be. It has metadata about its past history and what computation it was a product of. This allows Backpropogation to become a simple task.
Gradient w.r.t the input Tensors is computed step-by-step from loss to top in reverse. 
Computation history will track the path a  input variable took backwards to calculate the gradients properly. 


```
import pytorch
import torch.nn as nn
impor torch.nn.functional as F

class LeNet(nn.Module):
	def __init__(self):
		super(LeNet, self).__init__()
	    self.conv1 = nn.Conv2d(1,6,3)
		self.conv2 = nn.Conv2d(6,16,3)
		self.fc1 = nn.Linear(16*6*6,120)
		self.fc2 = nn.Linear(120, 84)
		self.fc3 = nn.Linear(84, 10)
    def forward(self, x):
	    x = F.max_pool2d(F.relu(self.conv1(x)), (2,2))
	    x = F.max_pool2d(F.relu(self.conv2(x)),2)
	    
		
```


[[ResNet - Deep Residual Learning for Image recognition]]
[[Reinforcement Learning]]
