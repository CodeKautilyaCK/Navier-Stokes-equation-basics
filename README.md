# Navier–Stokes Equations — Plain Text Version

## 1. Introduction
The Navier–Stokes (NS) equations govern fluid motion.  
They describe how fluid velocity and pressure evolve in space and time, based on:

1. Conservation of Mass (Continuity)
2. Conservation of Momentum (Newton’s Second Law)

These are nonlinear partial differential equations (PDEs) used in computational fluid dynamics (CFD).

---

## 2. Continuity Equation (Mass Conservation)

General form:  
ρ ( ∂u/∂x + ∂v/∂y + ∂w/∂z ) + ∂ρ/∂t = 0

For incompressible flow (constant ρ):  
div(u) = ∂u/∂x + ∂v/∂y + ∂w/∂z = 0

Where:  
- ρ = density  
- u = velocity vector (u, v, w)

---

## 3. Momentum Conservation (Navier–Stokes)

Vector form:  
ρ * ( ∂u/∂t + u · ∇u ) = - ∇p + μ ∇²u + ρ * f

Terms:  
- Left: Inertia (unsteady + convective acceleration)  
- Right: Forces (pressure, viscous, body)

---

## 4. 1D Navier–Stokes (x-direction)

ρ * ( ∂u/∂t + u * ∂u/∂x ) = - ∂p/∂x + μ * ∂²u/∂x² + ρ * fx

- Single velocity component u(x, t)  
- Applications: pipe flow, channel flow, shock tubes

---

## 5. 2D Navier–Stokes (x-y plane)

x-momentum:  
ρ * ( ∂u/∂t + u * ∂u/∂x + v * ∂u/∂y ) 
= - ∂p/∂x + μ * ( ∂²u/∂x² + ∂²u/∂y² ) + ρ * fx

y-momentum:  
ρ * ( ∂v/∂t + u * ∂v/∂x + v * ∂v/∂y ) 
= - ∂p/∂y + μ * ( ∂²v/∂x² + ∂²v/∂y² ) + ρ * fy

- Applications: lid-driven cavity, flow over a cylinder, natural convection

---

## 6. 3D Navier–Stokes (x-y-z)

x-momentum:  
ρ * ( ∂u/∂t + u * ∂u/∂x + v * ∂u/∂y + w * ∂u/∂z ) 
= - ∂p/∂x + μ * ( ∂²u/∂x² + ∂²u/∂y² + ∂²u/∂z² ) + ρ * fx

y-momentum:  
ρ * ( ∂v/∂t + u * ∂v/∂x + v * ∂v/∂y + w * ∂v/∂z ) 
= - ∂p/∂y + μ * ( ∂²v/∂x² + ∂²v/∂y² + ∂²v/∂z² ) + ρ * fy

z-momentum:  
ρ * ( ∂w/∂t + u * ∂w/∂x + v * ∂w/∂y + w * ∂w/∂z ) 
= - ∂p/∂z + μ * ( ∂²w/∂x² + ∂²w/∂y² + ∂²w/∂z² ) + ρ * fz

- Applications: 3D CFD flows, aircraft aerodynamics, turbulent channels

---

## 7. Key Notes

- 1D: Simplest, often educational  
- 2D: Captures main physics, moderate computational cost  
- 3D: Realistic, high computational cost  
- Turbulence: High-Re flows require RANS, LES, or DNS models  
- Boundary Conditions: Inlet, outlet, wall, and symmetry conditions are critical

---

## 8. Applications

- Aerospace: Lift, drag, and airflow over wings  
- Automotive: Vehicle aerodynamics, cooling systems  
- Civil: Wind load on buildings, hydrodynamics  
- Energy: Turbines, combustion chambers, battery cooling  
- Medicine: Blood flow simulation, biofluid dynamics

---

## 9. References

- Panton, R. L. “Incompressible Flow”  
- Ferziger, J. H., & Perić, M. “Computational Methods for Fluid Dynamics”  
- Karniadakis, G. E. “Physics-Informed Machine Learning”

---

## 10. Next Steps

- Implement 1D finite difference solution  
- Extend to 2D lid-driven cavity flow  
- Implement basic 3D channel flow simulation  
- Optional: Solve simplified NS using PINNs for proof-of-concept
