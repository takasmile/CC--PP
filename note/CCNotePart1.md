## <center>Common Criteria for Information Technology Security Evaluation
### 1.缩写及基本概念解释
- CC: Common Criteria 通用标准
- TOE: target of evaluation 评估目标
- ST: security target 安全目标 (part1: Annex-A)
- PP: protection profiles 保护框架 (part1: Annex-B)

### 2. 基本概念的具体描述  
介绍CC中所涉及到的最基本的三个概念：ST/TOE 以及 PP，三者的关系，对应package的构建方式，为之后evaluation做铺垫。
#### 2.1. TOE (target of evaluation 具体的评估目标)
A TOE is defined as a set of software, firmware and/or hardware possibly
accompanied by guidance.(系统及其满足需求的各项配置)  
The TOE may be an IT product, a part of an IT product, a set of IT products, a unique technology that may never be made into a product, or a combination of these.    
> **representations:**  
> - a list of files in a configuration management system;
> - a single master copy, that has just been compiled;
> - a box containing a CD-ROM and a manual, ready to be shipped to a
customer;
> - an installed and operational version.
#### 2.2. ST (p65)
内容图见本文件夹中附件图：ST-contents.png
![ST contents](https://i.imgur.com/dihAXNU.png)
> - Before and during the evaluation, the ST specifies “what is to be evaluated”.  
> - After the evaluation, the ST specifies “what was evaluated”.   

##### 2.2.1. ST introduction 简介:
- the **ST referenc**e and the **TOE reference**, which provide identification
material for the ST and the TOE that the ST refers to;
- the **TOE overview**, which briefly describes the TOE;
- the **TOE description**, which describes the TOE in more detail.
##### 2.2.2. Conformance Claims(ASE_CCL)  一致性声明:   
The conformance claim indicates the source of the collection of requirements that is met by a PP or ST that passes its evaluation. 需求和已经通过的PP、ST认证相吻合  

- CC conformance claim:  
CC version, CC Part 2 function requirements, CC Part 3 assurance reauirements  
- PP claim:  
PP Conformant,  Conformant statement(Annex B) 
- Package claim  
name Conformant(predefiened), name Augmented增广
- Conformance rationale
##### 2.2.3 Security problem definition (ASE_SPD)安全问题定义:
- **Introduction**: The process of deriving the security problem definition
falls outside the scope of the CC.由CC以外的文件或标准确定
-  **Threats**:  A threat agent on an asset, describe them as types of entities, groups of entities etc.   
e.g. hackers, users, computer processes, and
accidents  
*(countered by the TOE, its operational environment, or a combination of the two.)*
- **Organisational security policies (OSPs)**  
Be enforced by the TOE, its operational environment, or a combination of the two.  

- **Assumptions**假定和猜想:  
Made on the operational environment in order to be able to provide
security functionality.  
e.g. Assumptions on physical / personnel人事部门 / connectivity连通性 aspects of the operational environment.

##### 2.2.4 Security objectives (ASE_OBJ)安全目标  
The security objectives are a concise and abstract statement of the intended
solution to the problem defined by the security problem definition.对之前定义的问题的解决方案  

- provide a high-level, natural language solution of the problem;
- divide this solution into two part wise solutions, that reflect that different entities each have to address a part of the problem;
- demonstrate that these part wise solutions form a complete solution to the problem.

##### 2.2.5 Extended Components Definition (ASE_ECD)  定义扩展组件
非基于CC Part 2 or CC Part 3组件之外的其他安全需求  
In this case, new components (extended components) must be defined, and this definition should be done in the Extended Components Definition. 对这些额外定义的组件有标准的定义要求
##### 2.2.6 Security requirements (ASE_REQ)安全需求
- the security functional requirements (**SFRs**) 安全功能性需求:   
a translation of the security objectives for the TOE into a standardised language;
- the security assurance requirements (**SARs**) 安全确保性需求:   
a description of how assurance is to be gained that the TOE meets the SFRs.
##### 2.2.7 TOE summary specification (ASE_TSS) TOE摘要说明书  
Provide potential consumers of the TOE with a description of how the TOE satisfies all the SFRs.针对TOE如何满足SFRs的说明

#### 2.3. PP (part1 Annex-B)
![PP contents](https://i.imgur.com/PQDax3k.png)
> 可将ST与PP的结构图进行对比，观察两者的相同和不同之处  

- A PP describes the general requirements for a TOE type.  
- A PP is typically a statement of need where a user community, a regulatory entity, or a group of developers define a common set of security needs.
- PP的结构: 见图pp-contents.png
> 区别(9.6): Base-PP(s) B.14.3.2, PP-Module(s) B.14, PP-Configuration(s) B.15, Standard PP
##### 2.3.1 PP introduction (APE_INT) PP简介:
The PP introduction describes the TOE in a narrative way on two levels of abstraction:  

- the **PP reference**, which provides identification material for the PP;  
- the **TOE overview**, which briefly describes the TOE.
##### 2.3.2 Conformance claims (APE_CCL)  
This section of a PP describes how the PP conforms with other PPs and with packages. It is identical to the conformance claims section for an ST 
##### 2.3.3 Security problem definition (APE_SPD)
This section is identical to the security problem definition section of an ST 
##### 2.3.4 Security objectives (APE_OBJ)
This section is identical to the security objectives section of an ST 
##### 2.3.5 Extended components definition (APE_ECD)
This section is identical to the extended components section of an ST
##### 2.3.6 Security requirements (APE_REQ)
This section is identical to the security requirements section of an ST 
##### 2.3.7 TOE summary specification
A PP has no TOE summary specification.

#### 2.4 Package (part 1 p52)
##### 2.4.1 package
A package is a named set of security requirements. A package is either
- a functional package, containing only SFRs (CC part 2), or
- an assurance package, containing only SARs (CC part 3).  

Packages can be used in the construction of larger packages, PPs and STs.     
At present there are no criteria for the evaluation of packages, therefore any set of SFRs or SARs can be a package.目前还没有针对构建package的具体标准
> Examples of assurance packages are the evaluation assurance levels (EALs) that are defined in CC Part 3.
##### 2.4.2 SFR(SFPs/TSF), SAR 与 EAL(level), CAP(level)简介
1. security functional requirements (**SFRs**) CC part2 p18 
The SFRs define the rules by which the TOE governs access to and use of its resources, and thus information and services controlled by the TOE.定义了TOE使用其资源的权限和方式
- The SFRs may define multiple Security Function Policies (**SFPs**) to represent the rules that the TOE must enforce.TOE必须遵守的规则  
- Those portions of a TOE that must be relied on for the correct enforcement of the SFRs are collectively referred to as the TOE Security Functionality (**TSF**). 为正确执行所依赖的部分
> The TSF consists of all hardware, software, and firmware of a TOE that is either directly or indirectly relied upon for security enforcement.TOE
2. Security assurance requirements (**SAR**s) CC part1 p79
The SARs are a description of how the TOE is to be evaluated.   
This standardised language is defined as a set of components defined in CC Part 3.  
3. Evaluation assurance level (**EAL**) 评估保证等级 CC part3 p31 p24
The Evaluation Assurance Levels (EALs) provide an increasing scale that balances the level of assurance obtained with the cost and feasibility of acquiring that degree of assurance. 针对评估的成本和可行性的递增的尺度
4. Composed assurance package (**CAP**) 
The Composed Assurance Packages (CAPs) provide an increasing scale that balances the level of assurance obtained with the cost and feasibility of acquiring that degree of assurance for composed TOEs.
### 3. ST/TOE 与 PP的关系，三者之间的联系和区别

### 4.CC涉及的其他方面
> 通过研究ST与PP的关系，得出信息服务的分类方案。
1. CC受众：

- **consumers**: decide whether a TOE fulfils their security needs;
- **developers**: preparing for and assisting in the evaluation of their TOEs and in identifying security requirements to be
satisfied by those TOEs; 
- **evaluators**: forming judgements about the conformance of TOEs to their security requirements. 

2. 各概念之间的关系
- A PP is intended to be used as a “template” for an ST. That is: the PP describes a set of user needs, while an ST that conforms to that PP describes a TOE that satisfies those needs.(通过对比两者结构图看出)
- Whereas an ST always describes a specific TOE (e.g. the MinuteGap v18.5 Firewall), a PP is intended to describe a TOE type (e.g. firewalls). 
- The TOE has been evaluated to meet the ST.

### 5. CC evaluation评估
#### 1. ST / TOE evaluation
1. 两步骤 (p45)：
- ST evaluation: where the sufficiency of the TOE and the operational environment are determined;确定具体的TOE和操作环境
- TOE evaluatino: where the correctness of the TOE is determined.确定TOE的正确性
2. ST evaluation:  
Security Target evaluation criteria(CC Part 3)
3. TOE evaluatinon (p45):  
input: TOE & ST, developement environment, SARs(form ST)  
result: SARs是否都已满足，若满足，通过ST中所陈述的,TOE针对SFRs的满足程度来确定其具体的担保等级(level of assurance).
#### 2. PP evaluation (后面会讲到)
### 6. Tailoring Security Requirements 裁剪安全需求  
> Operations:
- Iteration (迭代): allows a component to be used more than once with varying operations;
- Assignment (赋值): allows the specification of parameters;
- Selection (选择): allows the specification of one or more items from a list; 
- Refinemen (精致)t: allows the addition of details.
> Dependencies between components:
- Part 2 和 part 3 中的组件之间可能有依赖关系
- 使用时机：dependencies should be satisfied when requirements based on components with dependencies are incorporated into PPs and STs. Dependencies should also be considered when constructing packages.  
最后合并PPs和STs文档时，或者构建包时

### 7. evaluatin-results 评估结果(线性的评估流程)
> The expected results from PP and ST/TOE evaluations performed according to the CEM.
![evaluation-resultes](https://github.com/takasmile/CC-PP/blob/master/note/evaluation-results.PNG)
### 8. 疑问