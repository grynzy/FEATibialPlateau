# Objectives
Determine the biomechanical stability of these external fixators in type III pilon fractures using finite element modelling.

# Materials and Methods
The slice thickness of the CT images was 1.5 mm in a 512 c 512 matrix.
The DICOM data sets, which consist of 225 CT images, were then imported into Mimics 15.1 software to reconstruct the surfcace geometry of the tibia, fibula ...

## Finite element modelling
The bones in the STL files were imported into Marc.Mentat (MSC.Software, Santa Ana, CA). 
Convert the completed three-dimensional model to linear first order tetrahedral elements. 

Bones were assigned using linear isotropic material properties with elastic modulus of 7300 MPa for cortical bone, and 1100 MPa for cancellous bone

![[Pasted image 20210426151234.png]]

Poisson's ratio = 0.3 (cortical) 0.26 (cancellous).
The implants were designed using SolidWorks (SolidWorks 2012, Dassault Systemes Solidworks Corp., USA).

All the fixators were meshed using 3-Matic (same with Mimics)
Young's modulus = 110,000 MPa
Poisson's ratio = 0.3

Mesh convergence analyses were performed and resulted in a variation in mesh size throughout the model. 
All contact between articulating surfaces was assigned a friction coefficient of 0.3
Bones were converted to a surface triangular mesh and saved in a stereolithographic file format

Imported into Marc.Mentat to 
### Boundary conditions
Stance phase:
- 70 kg of body weight
- 50% of the body weight (350 N) was applied on to the foot
- The relative micromovement of all simulated models were measured between the proximal and distal fragments at the lateral side
- 


# Results
![[Pasted image 20210426153424.png]]