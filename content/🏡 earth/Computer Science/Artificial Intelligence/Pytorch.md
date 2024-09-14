#concept-pamphlet 
#todo: pytorch terminology is important


x.shape

x.dtype

.sum

torch.Generator().manual_seed(234235235)

torch.multinomial(p, num_samples=1, replacement=True, generator=g).item()

torch.tensor(x)

import torch.nn.functional as F
xenc = F.one_hot(xs, num_classes=27).float()


torch.randn((27, 1))

torch.zeros(5)


W.grad

loss= -probs[torch.arange(5), ys].log().mean()
loss.backward()

