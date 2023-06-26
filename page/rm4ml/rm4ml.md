---
layout: page
title: InputGen
permalink: /inputgen/
---

Download and use of InputGen can be found [here](https://rm2pt.com/advs/inputgen).

### Introduction
**InputGen** is a tool for automatic generation Prototype Inputs to Support Rapid Requirements Validation
. The **benefits** of InputGen are as follows:

1. **Automatic input data generation of system operations**. InputGen can automatically refactor the prototype generated by RM2PT to support generating the validated input data of the system operation.

2. **Initial data auto-loading**. InputGen contains an interface for loading initial data, which can save the time for the administrator. The initial data can be imported from external YAML file, which can be viewed and modified easily by the user.

3. **Supporting rapid requirements validation**. Compared with the original prototype generated from RM2PT, InputGen can automatically refactor the generatedthen prototype from the same *requirements model* without any templates. Then refactoried prototype can automatically generate the validated input data of the system operation, this will boost the validation process.

<img src="../../imgs/InputGen/OverviewofInputGen.png" alt="OverviewofInputGen" width="80%" height="80%" />

### Input of InputGen — Requirements Model

<img src="../../imgs/InputGen/rm.png" alt="rm" width="80%" height="80%" />

The input to InputGen is a UML requirements model with OCL constraints. The model includes: a conceptual class diagram, a use case diagram, system sequence diagrams, contracts of and system operations.

- **A conceptual class diagram:** A conceptual class diagram is a concept-relation model, which illustrates abstract and meaningful concepts and their relations in the problem domain, in which the concepts are specified as classes, the relations of the concepts are specified as the associations between the classes, and the properties of the concepts are specified as the attributes of the classes.

- **A use case diagram:** A use case diagram captures domain processes as use cases in terms of interactions between the system and its users. It contains a set of use cases for a system, actors represented a type of users of the system or external systems that the system interacts with, the relations between the actors and these use cases, and relations among use cases.

- **System sequence diagrams:** A system sequence diagram describes a particular domain process of a use case. It contains the actors that interact with the system, the system and the system events that the actors generate, their order, and inter-system events. Compared with the sequence diagram in design models, a system sequence diagram treats all systems as a black box and contains system events across the system boundary between actors and systems without object lifelines and internal interactions between objects.
- **Contracts of system operations:** The contract of a system operation specifies the conditions that the state of the system is assumed to satisfy before the execution of the system operation, called the pre-condition and the conditions that the system state is required to satisfy after the execution (if it terminated), called the post-condition of the system operation. Typically, the pre-condition specifies the properties of the system state that need to be checked when system operation is to be executed, and the postcondition defines the possible changes that the execution of the system operation is to realize.


### Main features
InputGen takes requirements models as input, which can automatically refactor and enhance the generated prototype from RM2PT. The enhanced prototype can automatically generate a validated input data of the system operations for requirement validation. In addition, the enhanced prototype provide an external interface to load the initial data from a external file, which can save the time of modeling the data functionality for the administrator. 

#### Importing the initial data
InputGen provides an external interface for loading initial data, which can save the time for the administrator. The operations of modeling the administrator and manually adding initial data in the generated prototype are eliminated. Initial data is imported from the YAML file, which can be viewed and modified easily by the user. 

#### Automatic input data generation of system operations
InputGen can automatically refactor and enhanced the generated prototype from RM2PT. The prototypr+ can automatically generate a validated input data of the system operations for requirement validation by clicking a button. If stakeholders are not satisfied with the input data, they can also click the input box to choose other candidates. 

#### Supporting rapid requirements validation
Compared with the original prototype generated from RM2PT, then refactoried prototype can automatically generate the validated input data of the system operation, this will boost the validation process.


### CoCoME Case Study

To illustrate the InputGen’s capabilities, CoCoME is used as an example to demonstrate the requirements model.

### Importing the initial data
Before using the prototype to validate the requirements, you can use the Load File button to automatically load the initial data through the external interface, without manually adding it after modeling the administrator. We provide an external CoCoME yaml file, you can click [here](https://github.com/RM2PT/InputGen-UpdateSite/releases/download/v1.0.0/test.yaml) to download.

<img src="../../imgs/InputGen/11loadfile.png" alt="11loadfile" width="70%" height="70%" />


### Automatic input data generation of system operations
 In the system operation enterItem, you can choose to click the LoadFromState button to generate input data, if you think that the input data does not meet your requirements, you can also click the input box to choose other candidates. Moreover, you can click the InputReset button to reset all inputs and manually input them by yourself.

The image below shows a part of CoCoME's automatic input data generation of the system operation enterItem. For more details, please see [CaseStudies](https://github.com/RM2PT/CaseStudies).

<img src="../../imgs/InputGen/7enterItem.png" alt="7enterItem" width="70%" height="70%" />


### Evaluation Results
In practice, the generated prototypes are manually entered input data by stakeholders for requirements validation. InputGen can refactor the prototype generated by RM2PT so that input data can be generated automatically. To measure the effectiveness, we compared two versions. (1)Prototype, which is generated by RM2PT. (2)The enhanced prototype, which is refactored by InputGen. The results of the time to complete the task are shown in Table.

<img src="../../imgs/InputGen/shiyan1.png" alt="8result" width="80%" height="80%" />

We count the time efficiency of using the prototype for requirements validation. For these system operations that can be entered multiple times, we count the time it takes to input three data. For example, we can enter multiple items into the system operation enterItem, and we count the time it takes to purchase three items. These four cases are shown in Table. 

On average, the enhanced prototype can improve 56.43% times efficiency of requirements validation than the original generated prototype from RM2PT. 

<img src="../../imgs/InputGen/shiyan2.png" alt="8result" width="80%" height="80%" />

In practice, developers need to spend time modeling the administrator and their operations and manually adding initial data to the generated prototype for requirements validation. We compared this time and the time cost of writing the YAML file. As Table II shows that on average, it takes 0.29 hours to write the YAML file with the same initial data, less than thirty minutes, while modeling the administrator and manually adding the same data takes 4.11 hours. 



In short, InputGen is an effective automated prototype approach than the manual inputting, which can assist in requirements validation and make it easier for customers and developers to find errors in their requirements.