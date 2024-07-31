
Book: ![[Software Architecture Fundamentals 1st Edition.pdf]]

___

# 1. Introduction

# 2. Software Architecture Fundamentals

**What is Software-intensive system:**
**System.** A collection of component organized to accomplish a specific function or set of functions. [IEEE 610.12-1990, p. 73]

**Software.** Computer programs, procedures, and possibly associated documentation and data pertaining to operation of a computer system. 
[IEEE 610.12-1990, p. 66]

A **Software-intensive system** is a collection of building blocks that are organized in such way that they together accomplish the purpose of the system. Building block of such a system that entirely of for the most part consist of software carry out essential task for achievement of the purpose of the system. The software element of the system consists of a collection of programs, procedures, data, and associated documentation.

## 2.3 Fundamental Software Architecture Concept
### 2.2.2 Type of Software-intensive system

![[Figure2_3-CategoriesOfSoftware-intensiveSystems.png]]

- The focus of **information systems** is on management and processing of information. Large amounts of data or complex data structures have to be managed, processed, evaluated and calculated, and several thousand users may have to be served both simultaneously and interactively. 
	- Examples of information systems are the core insurance management system of an insurance company, SAP systems, CAD systems, complex simulation systems for weather forecasting, or simulation calculations for engineers.

- **Embedded systems** contain software that is embedded into physical objects. With significant resource limitations in terms of the available hardware, they carry out tasks that are critical in terms of both data security and functional reliability, and which have to fulfill demanding functional and quality requirements. This functionality mostly involves regulation, control or communication functions.
	- Examples of embedded systems are washing machines, machine tools or production lines in the manufacturing industry, radio cells in mobile phone networks, airbag control systems, and vehicle parking assistants.

- **Mobile systems** are (semi-)autonomous, personal units with high interaction requirements. In addition to being mobile, they are characterized by the fact that they provide local and, where necessary, (semi-)autonomous functions. In addition they can, and to an extent also need to, interact with centralized, mainly stationary systems to synchronize themselves or to coordinate information and actions with others. Due to their mobility, however, the link to the central systems is not continuously available. 
	- Examples of embedded systems are smartphones, (semi-)autonomous transportation robots, and sensor/actuator nodes in ad-hoc networks.

**Note**: With increasing networking of system, software-intensive system exits that cannot be assigned to merely one category.

The importance of SWA for SW-intensive system ???

### 2.3.1 What is Software Architecture

There is no single, universally accepted definition of SWA.

[iSAQB]
The Software Architecture **defines** the fundamental **principle** and **rules** for the organization of a system and its **structure into building blocks and interfaces**, and their **relationships to each other and to the surrounding environment**. 
It thus defines **guidelines** for the entire **software lifecycle**, the **developer**, and the **software's operator**, from **analysis via design and implementation** to **operation** and **enhancement**. 

### 2.3.2 Building blocks, interfaces, and configuration

An interface represent a well-define access point to the system or its building blocks.
In this context, an interface describles the characteristics, (for example, attributes, data, functions) of this access point. The objective is to define these characteristics as percisely as possible with all the necessary aspects, such as syntax, data structures, functional behavior, error behavior, non-functional characteristics, the interface usage log, technologies, protocols, access modifier, file format, conditions/constraints, and semantics.


![[Figure2_4-ExampleOfBuildingBlock.png]]

Definition of a building block includes the three essential characteristics specified below

A building block provides interfaces that it gruantes in the sense of a contract. THis guarantee, however, only applies when the interfaces that it requires are made available within the scope of a corresponding configuration. **(Provided and required interfaces)** 

Via the provided and required interfaces, the building block encapsulates the implementation of these interfaces. Its can thus be replaced by other building blocks that provide and, where appropriate, also require the same interfaces. **(Encapsulation and interchangeability)**

Building block are also the unit of hierarchical (de)composition pf a software-intensive system. In other words, a building block can be implemented using an appropriate configuration of other (sub-) building blocks and their interrelationships. In this case, too, we say that this (super) building block encapsulates the (sub-) blocks. The building block can also delegate external interfaces to internal interfaces and vice versa. This is how relationships between building blocks are defined. **(Configuration and hierarchical (de)composition)**

![[Figure2_5-TheRelationshipsBetweenBuildingBlockAndInterfaces.png]]

![[Figure2_6-BlackboxGrayboxWhiteboxViews.png]]

![[Figure2_7-HierarchicalDecompositionWithBlackWhiteBoxView.png]]

![[Figure2_8-WhoDefinesTheInterfaceAndAgrement.png]]

### 2.3.3 Concepts for descripbing software architectures

An architecture is only of limit use if it is not documented. only an appropriately document architecture can be sustainably communicated, discussed, and further developed.

All aspects of the software architecture are presented to representatives of different interests (stakeholder), discussed with them, and jointly further developed. 
Customer and users can also become involved in architecture decisions that affect them. Developer should also become involved in the discussion, in particular for communication and discussion of aspects of the architecture that are relevant to the final implementation.

![[Figure2_9-CoreElementOfConceptuallModel.png]]

![[Figure2_11-ConceptualModelForDescriptionsOfSWA.png]]


#### Note: Need to revisit this section for more deep down (Architecture viewpoint, architecture view) ???

### 2.3.4 Architectural description and architectural levels

![[Figure2_12-TheDifferentLevelInAnArchitecturalDescription.png]]


### 2.3.5 Interactions between software architecture and environment

- **Project environment and project management**
	Project environment and project management provide a variety of constrains and project objectives that must be taken into account where they are relevant to the architecture. Budget and the development approach, for example, can influence the software architecture, and vice versa. 
	In the surrounding environment of a system there are usually a number of applications and projects. This existing (and continuously changing) project and application landscape often has significant impacts on the software architecture being developed. If additional project or applications are initiated or suddenly terminated, this can have enormous impact on interfaces to the system for which a software architecture is to be developed. 
- **Product Management and Requirements Engineering**
	Product Management and Requirements Engineering place functional and, in particular, non-functional requirements, quality objectives, and constraints on the system, all of which can change during the course of the project and thus affect the architecture. On the other hand, the architecture can also identify which requirements generate conflicts of interest with other requirements or project constraints. The architecture can thus also generate impulses for changes to requirements.
- **Execution platform and operation**
	Generally, the execution platform and operations organization already exits within the organization. New system should use existing systems where possible, and this should be taken into account during the architecture design. On the other hand, new platform and operations requirements can also result from the architecture.
- **Tool and development environment**
	The architecture must ultimately be implemented. This requires appropriate tools and a development organization. Appropriate development environments also have to be provided for the selected programming languages, frameworks, and technologies. Equally, the architecture itself can also place new requirements on tools and the development organization. Expansion of test infrastructure may, for example, be necessary, depending on the selected technology.
	
![[Figure2_13-SWAIsInfluencedByItsEnvironmentAndViceVersa.png]]

### 2.3.6 Quality and value of a software architecture

Follow ISO Standard 25010 [ISO/IEC 25010], in which high-level quality characteristics are already defined;
- Functional Suitability
- Reliability
- Usability
- Performance efficiency
- Security
- Maintainability
- Compatibility
- Portability

## 2.4 Bird's-eye view of Software Architecture

Requirements Engineering and architecture design are two key factors for successful software development.
It is not sufficient to address these two areas in isolation. On the contrary, it is essential to ensure consistent integration of requirements engineering and architecture design if they are to influence each other positively.

![[Figure2_14-TheTwinPeakModel.png]]

### 2.4.1 Objectives and functions of software architecture design

The central task of software architecture design is to find a design approach with which the function and non-functional requirements defined by requirements engineering are implemented in a fully designed solution. 
This approach, however, is not a one-way street, as indicated by the Twin Peaks Model. Instead, the process involves continual compromise between the "request list" from requirements engineering and the software architect's inventory of existing solutions, building blocks, and other architecture artifacts.

![[Figure2_15-TheSWALongMarch.png]]

Sine a new system or system enhancements should not be addressed in isolation:
- the interfaces, requirements, and constraints from the four adjacent areas (fig. 2-13)
- interfaces to other systems, affected organizations, execution platform, and the implementation infrastructure, 
- also entire lifecycle of the system
these adjacent areas must be considered and co-designed by the architect.

### 2.4.2 Overview of software architecture design

The architect not only has to consider interfaces with requirements engineering, but also with other disciplines and roles involved in SW development. A SW architect design an architecture starting from the conditions, constraints, and requirements of these surrounding areas, thus defining the essential aspects of the solutions, such as the building block structure and interaction patterns.

![[Figure2_16-IterativeAndIncrementalStepsInvolvedInSWADesign.png]]

- **Analysis of requirements and constraints**
	The central task of architecture analysis is to analyze the objectives, constrain, and the functional (and in particular, non-functional requirements) that come from requirements engineering in the context of the other surrounding areas (figure 2-13).  This must include an analysis of quality, flexibility (the stakeholder is open to changes), and susceptibility to change (change of result of external influence over time) of the requirements.
	Gaps in the requirements must be identified (se [HNS99]). Particularly with regard to non-functional requirements, there is normally room for the improvement since those responsible for specifying the requirements often regard them as being self-evident.
	All parties involve in the project--especially designer and developers--have to develop an initial understanding of the architecture style and the technical infrastructure. This is the central architectural metaphor of the system.

- **Development of architecture views and technical concepts**
	Here, the architecture is developed in more detail. In particular the view-based description of the different architectural levels (functional and technical levels -- see figure 2-13) also takes place here. The objective is to break down the functional requirements to the corresponding functional architecture level, and for the relevant aspects of the non-functional requirements to design and document appropriate cross-cutting solution building blocks as the technical architecture level (see also Chapter 4). All the while, the fundamental solution framework given by the architecture style and the technical infrastructure must be taken into account.

- **Evaluation of architecture and design decision**
	The developed architecture must udergo quality assurance. Various methods can be used here, from diverse review techniques through technical prototypes and test to analysis and evaluation. The critical aspect here is derivation of specifics scenarios from the requirements to ensure the quality of the resulting architecture (see also Chapter 5).

- **Implementation support and review**
	The importance of communication of software architecture to all parties involved in the project is often underestimated. Only when all those involved--from the developers through the customer-- have understood and accepted the software architecture, can it be successfully implement and achieve the desired effects. The software architecture must of course be communicated in such way that it can be understood by the recipient. This mean that the architecture is explained to the customer with a different level of detail than to the developer. This process is not a one-way street, but rather a process of learning form one another and understanding.
	During its implementation, the architecture continues to be discussed with the parties involve in the project and any open issue, potential for improvement, fault and error,  any approaches for further development continue to be identified.

Effective tool support should also be established on the basic of these concepts. Autonomous tool solutions already exit for these individual task areas (see Chapter 6). These stand-alone tools must be integrated as seamlessly as posible to ensure that the architect can use them effectively.

### 2.4.3 Interplay between activities and abstraction level within the design
The individual activities involved in SWA design process can not be arranged linearly. They are areas of equal important to which SWA has to devote sufficient attention depending on the current project situation. The architecture design is a continuous interplay between the activities show in figure 2-16:
- Analysis of requirements and constrains
- Development of architecture views and technical concepts
- Evaluate of architecture and design decisions
- Support and review of the implementation

During the architecture design process, the SWA carries out these four activities in a sequence that suited the needs and context of the project. This iterative and incremental interplay of activities is associated with a top-down and bottom-up change of the abstraction levels and perspectives show in figure 2-13:
- Requirements and constraints of the surrounding areas
- Software architecture with abstraction levels, for example:
	- Architecture style and technical infrastructure
	- Functional and technical architecture levels
- Program design and implementation

This way, we can switch from the **topmost abstraction level** of the conditions, constraints, and requirements of the surrounding areas via the **abstraction level in the SWA** (architecture style and technical infrastructure, plus the functional and technical architecture levels) through to the **bottommost abstraction level**, which consist of the SW program itself, the program's design and its implementation. This is illustrated in figure 2-17. 

![[Figure2_17-OverviewSWADesignProcess.png.png]]

Within this process, the **project setting and constraints** **define the constraints of the architecture**. In return, the **architecture design** provides data on **technical project risks** and planning information. 
**Requirements engineering** describes the **functional and non-functional requirements** for the architecture design coming from those accountable for the system. **This is not a one-way street**,  the **architecture design** also **provides feedback** on the **feasibility of implementing the requirements**, and their **consequences for requirements engineering**.

The **partially or fully available technical infrastructure**—for example, server infrastructure, operating systems, requirements for programming languages, and the operating organization— must also be taken into **consideration during the architecture design process**. Especially the **interface with operations** is far too often **neglected**, which can result in **major problems during system deployment**. 
And once again, this is not a one-way street. The **architecture design** can **produce new technical infrastructure requirements**—for example, further expansion of the server landscape or the integration of additional middleware.

Finally, the architecture design provides the specifications for detailed design and programming. However, return flows of information are also necessary here. **Unforeseen problems** can **arise during** the **implementation of the software architecture** and, if these are **not communicated to the SWA** and a supposedly simple solution is **implemented** instead, this can **undermine the entire architecture**. It is therefore **important to discuss such problems with the SWA**, and to **jointly develop a solution** that may result in changes to the architecture.
### 2.4.4 Software architect's task and relationship with other roles

The task of the architect is to develop a blueprint for the system base on functional and non-functional requirements, while talking requirements and constraints of the surrounding areas into account. The subsequent implementation, maintenance, support and enhancements are based on this blueprint.

![[Figure2_18-SWAInRelationWithOtherRoles.png]]

- **Communication and discussion platform**
	Based on the architecture, the **architect presents** the **feasibility of the requirements** to the **requirements engineer**, the **customer**, and possibly the **user** too. During this process, the architect **provides support** by **correlating, prioritizing, and reflecting on functional and nonfunctional requirements**. He can **identify contradictions and discrepancies**, and ultimately **ensures** that the **requirements can be implemented**. The architect **identifies** ways of **integrating existing solutions and systems**, and **aligns the requirements** to the **existing system architecture and hardware**. He develops, evaluates, and assesses alternative solution approaches. Finally, based on the SWA, the architect **advises** the **project manager on project** and **iteration planning**, and **supports risk analysis and mitigation**, thus **providing support** for the **definition of work structure and assignment**.

- **Design and implementation plan**
	The **architect** is a **central point of contact** for the **system’s developers**. He **defines** the **system’s building blocks** as well as their **interfaces and interaction patterns**. He has to encourage the integration of new technologies and innovative solution approaches, and discuss them with the developers. He is in charge of the development, introduction, training, and reviewing of programming guidelines. He **assists** the **developers** in the **development of prototypes** and **sample solutions**, and **accelerates reuse of existing (partial) implementations**. He **explains the architecture**, **provides development specifications**, passes on his experience, and **carries out code reviews**. He also supports the testers. In an ideal situation, he even **defines testing conditions** and **specific test cases** for **testing specific architecture objectives**. He assists in the definition of **test sequences** and **dependencies**. Finally, he is the point of contact for **fault and error reports** that are **relevant to the architecture**. He is also the **central point of contact** for organizational roles such as **operations staff, security experts, and the like**.

# 3. Designing Software Architectures

## 3.2 Overview of The Architecture Design Process

## 3.3 Deign Principles and Heuristics

### 3.3.1 Top-down and bottom-up

### 3.3.2 Hierarchical (de)composition

Divide and conquer

Decomposition principles

The "as-simple-as-possible" principle

Separation of concern

### 3.3.3 Lean interfaces and information hiding

Information hiding

Use of interfaces

### 3.3.4 Regular refactoring and redesign


## 3.4 Architecture-Centric Development Approaches

### 3.4.1 Domain-driven design

Functional models as the basic for a design
![[Figure3_5-ComponenetElementsIOfDomainModel.png]]

Systematic management of domain objects

Structuring of functional domain

Types of domains

Integration of domains

### 3.4.2 Model-driven Architecture (MDA)

MDA is a concept that enables the generation of (part of) applications from model, such as UML. MDA was developed by the Object Management Group (OMG).

### 3.4.3 Reference architectures

Generative creation of system building blocks

Aspect orientation

Object orientation

Procedural approaches

## 3.5 Techniques For A Good Design

### 3.5.1 Degenerated design

### 3.5.2 Loose coupling

### 3.5.3 High cohesion

### 3.5.4 The open/closed principle

### 3.5.5 Dependency inversion

### ...


## 3.6 Architectural Patterns


## 3.7 Design Patterns





# 4. Description and Communication of Software Architectures








____

# **Training**
https://www.isaqb.org/certifications/cpsa-certifications/cpsa-foundation-level/

![[iSAQB_Pic.png]]

## Clarify requirements
tbd

## Influencing factor
tbd

## Identify risks
tbd

## Design structure and technical concepts

### Technical concepts

#### [[SW Design Principle]]

#### [[SW patterns]]

#### Reduce Complexity

##### Aspect-oriented programming - AOP

##### Cross-Cutting Concern
**Persistence**
- Persist data from volatile memory to permanent storage
- Decouple business domain and (database) infrastructure

**Error Handling**

**Security**
- Authentication
- Authorization
- Integrity
- Confidentiality
- Non-repudiation
- Availability

**I18N - Internationalization**
**Communication and Messaging**
**User Interface and Ergonomics**
**Business Rules and Processes**

##### Designing Interfaces
Style:
Call behavior:
Data interfaces:

##### Degenerated Design
- Fragility/Brittleness
- Rigid
- Poor reuse

##### Achieving Quality Goals
- Tactics
	- Performance 
	- Modifiability
	- Reduce Coupling

- Strategy
	- High Performance
	- Adaptability and Flexibility
	- High Availability

### Architecture Development Approaches

#### Iterative and Incremental Design

#### View-Based Architecture Development






