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
	1. Distance between Volkmann's canals (measured along the axis of the osteons) range (DVBC) value to set the position of equally-distanced points (interconnection points / IPs) for each vector line.
	2. These IPs are linked with other surrounding IPs with a straight line
	3. Those straight lines that do not comply with the maximum inclination angle are omitted from the model
	4. Interconnection line is transformed into a solid pipelike cylinder that represents the Volkmann's microchannels
9. All individual structures are merged using boolean and logic functons
10. Export the structures at different levels 
	1. Only osteons
	2. Only cement lines
	3. Only vascular porosities
	4. Whole bone model
	
### Modeling Algorithm in-Silico Validation with Porosity Check
- Volume check for each microstructure
- Volume fraction of the Haversian canals and the volkamnn's canals with respect to the total cortical bone volume:
*Healthy person*
Canals 14 +- 6%
Volkmann's 6 +- 3%
Haversian 8 +- 3%

## Experimental Validation towards Scaffold Usage Employing Additive Manufacturing and XCT-Scanning
Digital Light Processing --> better resolution (15 myumeter) to affordability ratio
*Difficulties*
Continuous clogging of the microchannels within the specimens:
	Not possible to have initial assessment for manufacturing models directly from CAD files

Therefore, the scale of 5x was used (6 Model 1, 6 Model 2)
Extracting scanned samples:
1. Sample was scanned using XCT-micro scanner
2. Files were processed with CT analyzer and rendered
3. Porosity check --> measuring the solid and empty areas in each layer of the scan
4. Exposed to X-rays to reconstruct a 3D model using Solidworks
5. Defined ROI and VOI

# Results and Discussion
## In-Silico Porosity Check
Visual Programming Language paired with reported values of the microsturcture can produce geometrical models without employment of images acquired from human tissue
Porosity check is a fair indicator that shows a good fidelity of biomimicking

## Experimental Porosity Check
To assess the feasibility of the proposed methodlogy towards manufacturing polymer-based bone substitute materials

The reconstruction of the Haversian and Volkmann canals is more defined in the osteoporotic structure
The definition of micro-tunnels and interconnections can be observed and measured more in the osteoporotic model
The degree of porosity before and after curing less than 1%
--> better addition, shrinkage or thermal expansion of the layers

*Difference between virtual and experimental models*
Reduced size of the microchannel and the limited resolution of the additive manufacturing process (100 myumeter) for this material

# Conclusions
1. Flexible parametric algorithm for mimicking bone microstructure in a 3D model was successfully developed and employed for the first time
2. Use of bone parameters and pseudo-random numbers allows the generation of bone microstructures dynamically
3. Merging of two or more osteons is a feature of the algorithm
4. 3D printing microstructural porous structures towards cortical bone implant fabrication remains a challenge given the limitations of additive manufacturing of microchannels for synthetic bone graft based on polymer
	1. Haven't made the biomimetic models with a 1:1 scale

# Correlation with my research
1. Give more knowledge about conducting algorithm
2. Need to take a look at SolidWorks API (Application Process Interface) for mimicking Grasshopper in Rhino, which were used in this paper
	1. Should understand basic of C++, the base of SolidWorks API
3. 

	
	


