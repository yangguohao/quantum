# AI-Studio-量子电路合成

## 项目描述
本赛题由 “2020百度之星·程序设计大赛” 的决赛赛题改编而来，以期为更多开发者提供量子计算领域的学习交流机会。百度自 2017 年起发起了面向全球 AI 技术爱好者的深度学习算法竞赛——百度之星·开发者大赛，大赛的宗旨是为有创新力、专业性强、富有极客精神和团队合作精神的顶级开发者团队提供交流切磋、施展才能的舞台，并为参赛选手提供真实的数据集、深度学习平台飞桨（PaddlePaddle）、完整技术解决方案和一站式 AI 开发平台 AI Studio，降低广大开发者的 AI 学习门槛。2021 年的百度之星·开发者大赛，期待你的加入！

高度发达的 A 星在一次异变中文明即将消失，A 星人将重要信息加密后发送到下一个面临同样异变的欠发达的 C 星，希望能帮助 C 星上的文明躲过这次浩劫。A 星文明高度发达，已经实现了量子计算，故而采用了量子电路来加密信息。C 星接收后深感无力，因为他们的文明只能实现小型的基础量子门，不足以解密该重要信息。此时他们想起了友好星球 B 星上的我们，或许能为他们带来一线生机。而在座的我们能否帮助 C 星文明解决这次危机？

科学家分析，神秘信息是经由量子电路加密过的一张图片，我们使用给定的 2 量子比特电路和 3 量子比特电路便可能进行解密。 为了不让 C 星坐以待毙，我们要将量子电路分解成 C 星可以实现的基础量子门，从而能帮助 C 星完成解密，完成史诗级的救援任务。
详细赛题信息可点击[查看](https://aistudio.baidu.com/aistudio/competition/detail/70)


## 量子比特符号

通常使用 狄拉克标记 (也称作bra-ket标记)表示量子比特。bra代表行向量，用<|表示，ket代表列向量，用|>表示。如下图所示

![image](https://ai-studio-static-online.cdn.bcebos.com/a830b98690f84223b6c63c60af93d927be8096778086439798c65e2424834cdc)



量子力学中的量子比特，需要用到量子态去表达，它需要用到两个连续的变量才能表达出全部信息。这两个量之间存在约束关系:

$|φ> = a|0>+b|1>$其中a和b都是复数，满足关系$|a|^2+|b|^2=1$ 

上式也可以写成$|φ> = cos\frac{θ}2|0>+e^{iθ}sin\frac{φ}2|1>$(与密度矩阵及其分解相关，具体内容我也没太弄得明白),其中$θ∈[0,Π]$，$φ∈[0,2Π]$，因此我们得到了可以用三维空间的一个点去表达一个态。如下图中的布洛赫球所示，传统的比特只有两端的0和1，而量子比特可以有整个球面上所有的点。

![image](https://ai-studio-static-online.cdn.bcebos.com/4611ba06cff94e9ea44330d2a30e5588769a07cd3f2547e2bb5ebb183176b351)

## 量子门

量子门必须是一个幺正矩阵。量子门需要由物理设备实现，因此必须遵守量子物理定律。物理学的定律表明:信息在过去和未来的点转换时，不会丢失，这被称为幺正性。量子门定义了状态的转变，因此必须遵守幺正性。

题目中$Ry(θ)$门就是其中一个量子门，通过绕y轴旋转θ值来更改量子比特状态。

而CNOT门也是如此，作用于两个量子比特，一个控制量子比特和一个目标量子比特，改变量子比特状态，如下图所示

![image](https://ai-studio-static-online.cdn.bcebos.com/333f5b6592a84e46be5efea1513d2b5f4af510aefcf44b8dbef36617105abdb5)

![image](https://ai-studio-static-online.cdn.bcebos.com/ffa265ebc1984834b9542c2722cc694ed398465463bb47e2988fbd5774a11231)

|00>和|01>中前一个为目标态，后一个为控制态
可以看到CNOT不会修改"00"的值，因为控制态为0。而控制态等于1的时候会反转目标态，由|01>变为|11>，所以也被称作控制非门，如同计算机中的"非"的操作。

接下来的题目就是通过这两个门来改变量子比特的状态达到我们需要的状态。

参考资料:
https://zhuanlan.zhihu.com/p/94015026

https://zhuanlan.zhihu.com/p/80455104

## 项目结构
```
-|data
-|work
-README.MD
-xxx.ipynb
```
## 使用方式
A：在AI Studio上[运行本项目](https://aistudio.baidu.com/aistudio/projectdetail/1637105)
B：此处由项目作者进行撰写使用方式。
