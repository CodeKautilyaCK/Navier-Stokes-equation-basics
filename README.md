# 📘 Navier–Stokes Equations: 1D, 2D, 3D Fluid Motion & Momentum

This repository provides a structured overview of the **Navier–Stokes equations** — the fundamental governing equations of fluid motion. The focus is on understanding **momentum conservation** in **1D, 2D, and 3D** contexts, with extensions to incompressible flows.

---

## 🔹 1. Introduction
The Navier–Stokes (NS) equations describe how the velocity field of a fluid evolves under the influence of pressure, viscous, and external forces.  
They are derived from **Newton’s Second Law** applied to a fluid element:

\[
\text{Rate of change of momentum} = \text{Forces acting on fluid}
\]

The forces include:
- **Pressure gradient force**
- **Viscous (diffusion) force**
- **Body forces** (e.g., gravity, electromagnetic)

---

## 🔹 2. Governing Equations

### **Continuity (Mass Conservation)**
\[
\nabla \cdot \mathbf{u} = 0 \quad \text{(Incompressible flow)}
\]

### **Momentum Conservation (Navier–Stokes)**
\[
\rho \left( \frac{\partial \mathbf{u}}{\partial t} + \mathbf{u}\cdot \nabla \mathbf{u} \right) 
= -\nabla p + \mu \nabla^2 \mathbf{u} + \rho \mathbf{f}
\]

Where:
- \(\mathbf{u} = (u,v,w)\) → velocity components  
- \(p\) → pressure  
- \(\rho\) → density  
- \(\mu\) → dynamic viscosity  
- \(\mathbf{f}\) → body forces  

---

## 🔹 3. 1D Navier–Stokes
For flow along the **x-axis** (e.g., 1D pipe or channel flow):

\[
\rho \left( \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} \right) 
= - \frac{\partial p}{\partial x} + \mu \frac{\partial^2 u}{\partial x^2} + \rho f_x
\]

- Single velocity component \(u(x,t)\)  
- Useful for **1D heat conduction–convection models**, simplified flows, shock-tube problems  

---

## 🔹 4. 2D Navier–Stokes
For flow in the **x–y plane** with velocity field \(\mathbf{u} = (u,v)\):

\[
\rho \left( \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x} + v\frac{\partial u}{\partial y} \right) 
= -\frac{\partial p}{\partial x} + \mu \left( \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} \right) + \rho f_x
\]

\[
\rho \left( \frac{\partial v}{\partial t} + u\frac{\partial v}{\partial x} + v\frac{\partial v}{\partial y} \right) 
= -\frac{\partial p}{\partial y} + \mu \left( \frac{\partial^2 v}{\partial x^2} + \frac{\partial^2 v}{\partial y^2} \right) + \rho f_y
\]

Applications:
- Lid-driven cavity  
- Flow over a cylinder  
- Natural convection in a cavity  

---

## 🔹 5. 3D Navier–Stokes
For full **3D motion** with velocity \(\mathbf{u} = (u,v,w)\):  

\[
\rho \left( \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x} + v\frac{\partial u}{\partial y} + w\frac{\partial u}{\partial z} \right) 
= -\frac{\partial p}{\partial x} + \mu \nabla^2 u + \rho f_x
\]

\[
\rho \left( \frac{\partial v}{\partial t} + u\frac{\partial v}{\partial x} + v\frac{\partial v}{\partial y} + w\frac{\partial v}{\partial z} \right) 
= -\frac{\partial p}{\partial y} + \mu \nabla^2 v + \rho f_y
\]

\[
\rho \left( \frac{\partial w}{\partial t} + u\frac{\partial w}{\partial x} + v\frac{\partial w}{\partial y} + w\frac{\partial w}{\partial z} \right) 
= -\frac{\partial p}{\partial z} + \mu \nabla^2 w + \rho f_z
\]

Applications:
- Aircraft aerodynamics  
- Turbulent pipe/channel flows  
- Multiphase & reacting flows  

---

## 🔹 6. Key Notes
- **1D → Simplification**, often pedagogical.  
- **2D → Still computationally cheaper, captures main flow physics**.  
- **3D → Real-world, but extremely computationally intensive**.  
- **Turbulence modeling (RANS, LES, DNS)** modifies how these equations are solved at scale.  

---

## 🔹 7. Next Steps in This Repo
- ✅ Numerical solution in Python (FDM/FVM) for 1D diffusion/convection  
- ✅ Extension to 2D lid-driven cavity  
- ✅ Baseline 3D case setup (simple channel flow)  
- 🔄 PINN implementation to solve simplified Navier–Stokes  

---

## 📚 References
- Panton, R. L. *Incompressible Flow*  
- Ferziger, J. H., & Perić, M. *Computational Methods for Fluid Dynamics*  
- Karniadakis, G. E. *Physics-Informed Machine Learning*  

---
