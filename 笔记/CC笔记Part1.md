## <center>Common Criteria for Information Technology Security Evaluation
### 1.缩写
CC: Common Criteria 通用标准
### 2.CC涉及的基本概念总览
> 通过研究ST与PP的关系，得出信息服务的分类方案。
1. TOE: target of evaluation 评估目标
2. ST: security target 安全目标 (part1: Annex-A)
3. PP: protection profiles 保护框架 (part1: Annex-B)
4. 各概念之间的关系
- A PP is intended to be used as a “template” for an ST. That is: the PP describes a set of user needs, while an ST that conforms to that PP describes a TOE that satisfies those needs.(通过对比两者结构图看出)
- Whereas an ST always describes a specific TOE (e.g. the MinuteGap v18.5 Firewall), a PP is intended to describe a TOE type (e.g. firewalls). 
- The TOE has been evaluated to meet the ST.
### 3.基本概念具体
#### 1. TOE
#### 2. ST (p65)
- Before and during the evaluation, the ST specifies “what is to be evaluated”.  
- After the evaluation, the ST specifies “what was evaluated”.   

Two roles (among many) that an ST should not fulfil are: a detailed specification, and a complete specification.   
(*ST may be a part of a complete specification, but not a complete specification itself.*)  
#### 3. PP (part1 Annex-B)
- A PP describes the general requirements for a TOE type.  
- A PP is typically a statement of need where a user community, a regulatory entity, or a group of developers define a common set of security needs.
- PP的结构: 见图pp-contents.png
> 区别(9.6): Base-PP(s) B.14.3.2, PP-Module(s) B.14, PP-Configuration(s) B.15, Standard PP
### 4. evaluatin-results 评估结果
### 5. 疑问
























