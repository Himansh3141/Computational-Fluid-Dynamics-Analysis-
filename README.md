**CFD Analysis of Laminar Forced Convection in a Staggered Tube Heat Exchanger**  

**Overview**

This repository presents a CFD-based investigation of laminar forced convection through a staggered tube heat exchanger using ANSYS Fluent. The objective of the study is to analyse the effect of varying inlet mass flow rates on flow behaviour, temperature distribution, and convective heat transfer performance using water as the working fluid.
The focus of this project is on physical interpretation, parametric analysis, and numerical reliability, rather than geometry optimisation or experimental validation.

**Problem Description**  
A two-dimensional staggered tube arrangement is used to model a simplified heat exchanger configuration. Water enters the domain at 298 K, while the tube walls are maintained at a constant temperature of 343 K. Simulations are carried out for multiple inlet mass flow rates to examine their influence on velocity fields, thermal boundary layers, and heat transfer characteristics.

**Fluid Properties (Water)**  
The thermophysical properties of water were assumed constant and are listed below:

Property	Value  
Density (ρ)	998.2 kg/m³   
Dynamic viscosity (μ)	0.001003 Pa·s  
Specific heat (Cp)	4182 J/kg·K  
Thermal conductivity (k)	0.6 W/m·K  
Prandtl number (Pr)	6.99  

**Geometric Parameter**  
Tube diameter (D): 0.01 m  

**Methodology**  
Solver: ANSYS Fluent (pressure-based, steady-state)  
Flow regime: Laminar, incompressible  
Energy equation: Enabled  
Working fluid: Water  
Inlet temperature: 298 K  
Tube wall temperature: 343 K  
Spatial discretisation: Second-order schemes  
Mesh: Quality-checked mesh with refinement near tube surfaces  
A parametric study was conducted by varying the inlet mass flow rate while keeping all other boundary conditions constant.

**Governing Dimensionless Numbers**  
The following dimensionless numbers were used to quantify flow and heat transfer behaviour:

*Reynolds Number*  
Reynolds number represents the ratio of inertial to viscous forces:

Re = (ρ · U · D) / μ

where  
ρ = density  
U = characteristic velocity  
D = tube diameter  
μ = dynamic viscosity  

*Prandtl Number*  
Prandtl number relates momentum diffusivity to thermal diffusivity:

Pr = (μ · Cp) / k  
For water with constant properties, Pr ≈ 6.99 for all cases.

*Nusselt Number*  
Nusselt number represents the ratio of convective to conductive heat transfer:

Nu = (h · D) / k

where  
h = convective heat transfer coefficient

**Key Parameters Analysed**

- Reynolds number (Re)  
- Nusselt number (Nu)  
- Prandtl number (Pr ≈ 6.99, constant)  
- Convective heat transfer coefficient (h)  
- Maximum velocity  
- Temperature distribution  

**Results Summary**  
The simulations demonstrate that increasing inlet mass flow rate results in higher velocities and Reynolds numbers, leading to thinner thermal boundary layers and enhanced convective heat transfer. Correspondingly, the Nusselt number and heat transfer coefficient increase with Reynolds number, in agreement with classical forced convection theory for liquid flow through tube bundles.
The Prandtl number remains constant across all cases, confirming that observed heat transfer variations are primarily driven by changes in flow conditions rather than fluid property variation.

**Validation and Numerical Reliability**  
Numerical reliability was ensured through:  
- Mesh quality assessment, with an average element quality of 0.907 and average skewness of 4.72 × 10⁻²  
- Residual convergence monitoring, using an absolute convergence criterion of 10⁻¹⁶  
- Stable convergence behaviour observed across all simulated mass flow rates  

Although no experimental data was used for validation, the agreement with established theoretical trends and strict numerical criteria indicates that the results are physically meaningful and numerically robust.

**Limitations**  
- Two-dimensional approximation  
- Isothermal tube walls  
- Constant thermophysical properties  
- No turbulence or radiation modelling  
- No experimental validation  

**Tools Used**  
ANSYS Workbench  
ANSYS Fluent
