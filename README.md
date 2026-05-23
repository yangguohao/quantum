# AI-Studio-Quantum Circuit Synthesis

## Project Description
This challenge is adapted from the final-round problem of the "2020 Baidu Star Programming Contest" to provide more developers with opportunities to learn and exchange ideas in quantum computing. Since 2017, Baidu has hosted the Baidu Star Developer Contest, a global deep-learning competition for AI enthusiasts. The contest aims to provide top developer teams—creative, highly professional, geek-minded, and collaborative—with a stage to communicate, compete, and showcase their skills. It also provides contestants with real datasets, the PaddlePaddle deep-learning platform, complete technical solutions, and the one-stop AI development platform AI Studio, lowering the barrier to AI learning for developers. Join the 2021 Baidu Star Developer Contest!

A highly advanced Planet A is about to lose its civilization due to a sudden anomaly. The people of Planet A encrypted critical information and sent it to the less developed Planet C, which faces the same anomaly, hoping to help Planet C survive. Planet A has already achieved quantum computing and therefore used a quantum circuit to encrypt the information. After receiving it, Planet C felt powerless because their civilization can only implement small basic quantum gates, which are insufficient to decrypt this critical information. They then remembered us on the friendly Planet B, who might offer a chance of survival. Can we help Planet C overcome this crisis?

Scientists have determined that the mysterious information is an image encrypted by a quantum circuit. We may decrypt it using the given 2-qubit and 3-qubit circuits. To avoid leaving Planet C defenseless, we must decompose the quantum circuits into basic quantum gates that Planet C can implement, thereby helping Planet C decrypt the message and complete this epic rescue mission.
Detailed challenge information is available [here](https://aistudio.baidu.com/aistudio/competition/detail/70).

## Qubit Notation

Qubits are usually represented using Dirac notation (also called bra-ket notation). A bra is a row vector, denoted by `<|`, and a ket is a column vector, denoted by `|>`, as shown below.

![image](https://ai-studio-static-online.cdn.bcebos.com/a830b98690f84223b6c63c60af93d927be8096778086439798c65e2424834cdc)

In quantum mechanics, qubits are expressed through quantum states, which require two continuous variables to encode all information. These two quantities satisfy a constraint:

$|φ> = a|0>+b|1>$, where $a$ and $b$ are complex numbers and satisfy $|a|^2+|b|^2=1$.

The above expression can also be written as $|φ> = cos\frac{θ}2|0>+e^{iθ}sin\frac{φ}2|1>$ (related to density matrices and their decomposition). Here, $θ∈[0,Π]$ and $φ∈[0,2Π]$, so a state can be represented as a point in three-dimensional space. This is the Bloch sphere shown below: unlike classical bits, which only take values 0 and 1 at two endpoints, a qubit can take any point on the sphere surface.

![image](https://ai-studio-static-online.cdn.bcebos.com/4611ba06cff94e9ea44330d2a30e5588769a07cd3f2547e2bb5ebb183176b351)

## Quantum Gates

A quantum gate must be a unitary matrix. Quantum gates must be physically realizable, so they must obey the laws of quantum physics. These laws imply that information is not lost when transforming between points in time, which is called unitarity. Since quantum gates define state transformations, they must satisfy unitarity.

The $Ry(θ)$ gate in this problem is one such quantum gate. It changes the qubit state by rotating by angle $θ$ around the y-axis.

The CNOT gate works similarly. It acts on two qubits, with one control qubit and one target qubit, changing the qubit state as shown below.

![image](https://ai-studio-static-online.cdn.bcebos.com/333f5b6592a84e46be5efea1513d2b5f4af510aefcf44b8dbef36617105abdb5)

![image](https://ai-studio-static-online.cdn.bcebos.com/ffa265ebc1984834b9542c2722cc694ed398465463bb47e2988fbd5774a11231)

In `|00>` and `|01>`, the former qubit is the target state and the latter is the control state.
As shown, CNOT does not modify the value of `"00"` because the control state is 0. When the control state equals 1, it flips the target state from `|01>` to `|11>`, so it is also called a controlled-NOT gate, analogous to the computer "NOT" operation.

The following tasks use these two gates to transform qubit states into the required states.

References:
https://zhuanlan.zhihu.com/p/94015026

https://zhuanlan.zhihu.com/p/80455104

## Project Structure
```
-|data
-|work
-README.MD
-xxx.ipynb
```
## Usage
A: [Run this project on AI Studio](https://aistudio.baidu.com/aistudio/projectdetail/1637105)
B: The project author can add additional usage instructions here.
