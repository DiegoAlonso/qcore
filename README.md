# QCORE Metamodel for the Unitary Circuit Model of Quantum Computation

This repository stores the Qcore metamodel as well as some initial model transformations, OCL constraints and query functions that complement it. 
Our aim is to provide a core set of assets that the quantum software development community can use and around which they can contribute further tools 
and utilities. 



The metamodel provided as part of the core set is graph-based and is flexible enough so as to allow the same quantum circuit to be modelled in 
slightly different ways, according to the developer way of thinking or available tools. 
Up to now, we have identified five such ways to do so.
The unicity of the metamodel allows simplifying the development, deployment, and maintenance of modelling tools. 
This will allow the community to "speak and understand" the same language, while supporting at the same time some local variations. 


The provided assets are the following ones:

- *qcore.ecore*: the core metamodel that provides the basic functionality. 
It must be extended, by inheriting from the abstract base meta-class _QuantumGate_, in order to add all the gates available in the general quantum unitary circuit model.
Currently, we only provide the Hadamard, NOT and Z gates, and the option to create their controlled versions

- *ocl_assets.ocl*: 

- *m2m/mSL_2_SL.etl*: [Epsilon](https://www.eclipse.org/epsilon/) model transformation that converts a model that follows the strategy 'mixed swim-lane' to the strategy 'swim-lane'.

- *m2m/rL.etl*: Epsilon model transformation that generates a new version of a model that follows the strategy 'line' in which the number of modeling elements 
have been reduced.

