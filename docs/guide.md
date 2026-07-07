# From Research to Product

*Notes on Computational Epistemology*

## Preface

This is a pipeline for building successful projects, rather than a framework for academic research. We borrow concepts from research to construct projects, but we do not pursue academic rigor or originality.

The mission of a project is to solve a specific problem. As long as this goal is achieved, the project fulfills its value. The focus of this pipeline is practicality, not theoretical perfection.

## Process

Explore the target domain through the following pipeline:

1. Problem Space  
2. Abstraction  
3. Model  
4. Prototype  
5. Product  

Not every problem space will necessarily become a product. In practice, many problem spaces stop at the model or prototype stage. This is part of exploration, not failure. Therefore, the success criterion of this pipeline is not the product itself, but whether it deepens the understanding of the problem space.

## Meta-Framework

* This pipeline is not traditional software engineering development, but rather a methodology for knowledge exploration.  
* If, during exploration, the problem space is judged to lack practical implementation value, it is entirely reasonable to terminate the process early. This is precisely the core spirit of three-stage implementation design.  
* Developers do not even need to write code; as long as the problem space can be mapped into abstractions and the understanding documented, part of the research outcome has already been achieved.  
* Nevertheless, we still encourage building at least one model as a tool for initial understanding of the problem space. If needed later, the project can be restarted and extended into the prototype and product stages.  

This meta-framework is not limited to DSLs or software development. Any problem that can be formalized and made programmable can be applied. Its core principle is **“knowledge first, product second.”** Therefore, any problem that can be abstracted and expressed as a model can gain research value through this framework.

## The Role of Code

In this pipeline, code is not merely a product but serves multiple epistemological roles:

* **Formalization**: Mapping abstractions into executable forms.  
* **Verification**: Checking whether the model is reasonable.  
* **Exploration**: Testing hypotheses through prototypes.  
* **Communication**: Code as an artifact for knowledge sharing.  

Therefore, within this pipeline, code is not only a technical tool but also a carrier of knowledge, fulfilling the complete epistemological function from abstraction to shared understanding.

## Principles

* Code is a tool for validating abstractions.  
* Research outcomes may conclude at any level of the pipeline.  
* Products are by-products, not inevitabilities.  
* Knowledge exploration takes precedence over delivery.

## Reflections on Proof of Concept

Although products are by-products of the problem space, valuable abstractions should evolve toward products, ultimately becoming software infrastructure rather than remaining indefinitely at the model or prototype stage.

The ultimate goal of this pipeline is to ensure that knowledge does not remain at the level of abstraction or prototype, but is transformed into sustainable, usable software infrastructure—serving as a bridge between research and engineering.

## Problem Space

* Select a concrete problem within the target domain and scale it to an appropriate scope, forming the problem space.  
* The problem space is not the product itself, but the proposition to be solved; the product is merely a tool to address that proposition.  
* When defining the problem space, existing solutions must be evaluated. This process filters out problems not worth pursuing, saving valuable time.  
* Do not start building a product without first defining the problem space. A vague problem space only leads to products without clear direction.  

The problem is not *“I want to create a programming language”* but rather *“I want to use a programming language to solve a specific problem”* — and then examine whether existing languages can address it. Programming languages are already abundant; unless a new language introduces unique features that resolve real pain points, it will likely remain a niche project.

## Abstraction

* Abstraction maps the problem space into operable vocabulary and structures.  
* When building abstractions, it is possible to map only part of the problem space and refine it gradually as needed.  
* Abstraction is not an algorithm or concrete logic, but rather the linguistic foundation of the model.  
* Some abstractions may later be discarded if they prove unhelpful for implementation or unsuitable for practical use.  
* The value of abstraction lies in its ability to formalize complex phenomena, serving as the starting point for models and prototypes.  

For example, a medical record may include patient data, chief complaints, symptoms, physical examinations, biochemical tests, imaging studies, diagnoses, and treatments. These data are not all embedded in a single record but are distributed across different structures: patient data may be managed independently, while test results may exist as time series. Such abstractions are also common in medical information standards, though this guide does not delve into specific regulations—it focuses only on the role of abstraction.

## Model

* Begin by recording ideas in free text. At this stage, don’t worry too much about accuracy — capturing the ideas is more important.
* Once the model is preliminarily confirmed, choose appropriate tools for modeling based on the context.
* When modeling, you can hardcode literal values and create only minimal examples; there’s no need to write usable programs.
* It is not recommended to skip modeling and jump straight to prototyping. Modeling takes less time and helps eliminate unsuitable projects early.

## Prototype

* The main purpose of a prototype is to validate the feasibility of a concept, so choose a technology stack with low development friction and fast writing speed.
* When developing a prototype, it is not necessary to implement full functionality — focus only on the core features.
* After evaluation, a prototype project can be directly converted into a production system without rewriting in another language, though the trade-off is lower system stability.
* During the prototype stage, focus solely on core logic and command-line tools. Avoid introducing complex architectures such as microservices too early.

> **Example**: If the prototype goal is to develop a domain-specific language (DSL), it is sufficient to ensure that the DSL syntax is stable and that there is a core path (happy path) to convert it into JSON. At this stage, it is not recommended to spend effort on error reporting or syntax checking, as these are non-core features.

If a production language is used directly for prototype development, the journey from concept to implementation may require three to five times more development time. However, such high-cost semi-finished products may face the risk of being abandoned and no longer maintained.

## Writing the Production System

* Never write a production system directly without a prototype. Without a prototype as a reference, development iterations will be excessively slow.
* Since a prototype already serves as an implementation baseline, this stage can even leverage vibe coding to quickly generate code, followed by manual fine-tuning and optimization.
* Create a new branch in Git for the production project. Do not overwrite or delete the existing prototype project.
* Once the production project matures, move the prototype project to a separate branch for archival, and merge the production branch back into the `main` or `master` branch.

## Community

- Compared to community, **dogfooding is more important**. Many personal or internal projects may not have a community, yet they continue to evolve through consistent dogfooding.
- Even for internal projects, it is essential to maintain reasonable generality. Avoid hardcoding literals, file paths, or environment-specific settings.
- For a project, the value of community lies in external users challenging its validity. Responding appropriately to community feedback can help improve the project.
- When community direction diverges from internal needs, revisit the problem space and abstractions. This may reveal opportunities for refinement.

## Conclusion

The same abstraction mapped from a problem space will be re-implemented at different scales across the stages of model, prototype, and product. On the surface, this may seem like wasted effort, but it is in fact the core of the pipeline: **code is merely the artifact of exploration, while abstract models are the true accumulation of knowledge (Code as Epistemic Artifact).**

Through repeated validation, we confirm that the problem space indeed holds value, ensuring that the final product is not an accidental outcome but a grounded implementation built upon a solid model.

## Vision

To make code not just a by-product of research, but a continuous carrier of knowledge—ultimately becoming shared infrastructure across disciplines.
