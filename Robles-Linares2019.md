# Introduction
Objectives:
Present a novel algorithm for generating [[in-silico]] [[biomimetic]] models of a cortical bone microstructure towards manufacturing biomimetic bone via additive manufacturing

Modeling based on:
- Density
- Inclination
- Size range of:
	- Osteon
	- Haversian and Volkmann's canals

Porosity = 13.37 - 21.49% ~ same with models of of healthy and osteoporotic bone --> *are this also in-silico?*



Bone consists of 2 main tissues:
1. The cortical (compact) layer in the outermost region
	- Can be regarded as composite material made of unidirectional fibers called [[osteons]] immersed in matrix made of old surmineralized osteons
2. The cancellous or spongy layer filling the inner section of the bone

**Objectives**
1. Provide brief outline of the current state-of-the-art of cortical bone modeling. --> *what about cancellous?*
2. In-depth analysis of the porposed parametric modeling based on:
	- set of macro and microstructural parameters
3. Build algorithm that dynamically constructs a 3-d bone sample model composed based on number 2
4. By creating healthy and osteoporotic cortical bone conditions, it can show the feasibility of this algorithm for detailed and tunable cortical bone tissue modeling


# Materials and Methods
## Algorithm for Generating the Cortical Bone Models
Made by:
- Free-form surface modeler CAD software (Rhino 6)
- Built-in visual programming language Grasshopper
- 
A set of parameters are specified by the user including:
#### Input
- Osteon diamter range
- Osteon density
- Osteon inclination angle range
- Cement line thickness range
- Haversian canals diameter range
- Volkmann's canals diameter range
- Distance between Volkann's canals
- Maximum inclination angle of the Volkmann's canals

To create randomness in the model:
- Add pseudo-numbers using seed values

The results can be seen in terms of:
#### Output
- Haversian porosity
- Volkmann's porosity
- Overall porosity

### Modeling Algorithm
Two types of algorithm with each corresponds to:
1. Geometrical (macrostructural) features of the bone
2. Nature of the microstructure of the bone

### Modeling Algorithm Process and Steps
1. Generate solid 3D volume
2. Lower base of volume is filled with circles (osteons) with a random size and position accordingly to the microstructural parameters
3. Vector is constructed from each circle center towards the top surface of the bone volume (osteon inclination angle range)
4. A solid pipe-like cylinder is created along each vector with the same diameter as the base circle
5. The cement line is generated as a tangent concentric cylinder to the solid pipe
6. The thickness is determined with the seed values and the cement line thickness range (CLT)
7. Haversian canals are constructed along the same vectors using the diameter range (HCDR)
8. Volkmann's canals generation:
	1. Distance between Volkmann's canals (measured along the axis of the osteons) range (DVBC) value to set the position of t

### Modeling Algorithm in-Silico Validation with Porosity Check

## Experimental Validation towards Scaffold Usage Employing Additive Manufacturing and XCT-Scanning

	
	


