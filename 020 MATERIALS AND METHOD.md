# Material Properties
## Bone

| Author           | Elastic Modulus (MPa)                               | Poisson's Ratio                                      | Assumptions                                       |
| ---------------- | --------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------- |
| [[tarapoom2015]] | 14870 (cortical) 400 (cancellous) 300 (bone marrow) | 0.296 (cortical) 0.3 (cancellous) 0.45 (bone marrow) |                                                   |
| [[ren2018]]      | 14000                                               | 0.4                                                  | Continuous, homogeneous, isotropic linear elastic |
| [[Jang2017]]     | 17000 (cortical) 300 (cancellous)                   | 0.36 (cortical) 0.3 (cancellous)                                                     |                                                   |

## Implants
| Author           | Elastic Modulus (MPa)  | Poisson's Ratio                                      | Assumptions                                       |
| ---------------- | ---------------------- | ---------------------------------------------------- | ------------------------------------------------- |
| [[tarapoom2015]] | *none*                 | 0.296 (cortical) 0.3 (cancellous) 0.45 (bone marrow) |                                                   |
| [[ren2018]]      | 200000                 | 0.3                                                  | Continuous, homogeneous, isotropic linear elastic |
| [[Jang2017]]     | 113000  (ASTM F136-08) | 0.33                                                 |                                                   |
# Boundary Conditions
## Contact behavior
1. bone to bone
>- bonded [[Jang2017]]
3. screw to bone
>- Coulomb friction 0.4 [[Jang2017]]
5. implant to bone
>- Coulomb friction 0.4 [[Jang2017]]
7. screw to implant
>- Coulomb friction 0.4 [[Jang2017]]

## Loading conditions
[[Jang2017]]
![[Pasted image 20210601135345.png]]
[[golovakh2014]]
800 N (0.3 MPa)


Malreduction gap:
> Malreduction gap 
> >2 mm [[ren2018]]

> Ignored the factors influencing knee strees:
>>ligaments
>>muscles
>>other soft tissue

# Results
## Vertical displacement
## Maximum stress of each implant
## Von Mises stress (distribution stress)
## Professor's Guidance
1. Finish the bone model
2. Get to know poroelastodynamics
3. Get to know poroelastic

# Method
## 1. Image Acquisition
Images were obtained from Visible Human Project. The 

# General Knowledge
Convergence test is used as indication whether the FE model used in the current study is not sensitive to the grid refinement of the mesh (the closer to 0, the better)

Explain more about the dimension of the implant and the screw (length, radius)


