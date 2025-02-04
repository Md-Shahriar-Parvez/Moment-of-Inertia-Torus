# Moment of Inertia of a Solid Torus: Analytical Derivations

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Field](https://img.shields.io/badge/Field-Classical%20Mechanics-green.svg)
![Institution](https://img.shields.io/badge/BUET-Mechanical%20Engineering-red.svg)

This repository contains three independent analytical derivations for calculating the **Moment of Inertia ($I$) of a uniform solid torus** about its central rotational axis of symmetry. 

Traditionally, calculating the rotational inertia of a torus involves complex 3D coordinate transformations (toroidal or spherical-polar) and multidimensional triple integration requiring Jacobian determinants. The papers presented in this repository demonstrate elegant alternative geometric decomposition methods that reduce the problem to single-variable integration without sacrificing physical rigor.

---

## 📐 Final Result

For a uniform solid torus of total mass $M$, major radius $R$ (distance from center of torus to center of tube), and minor radius $r$ (radius of circular cross-section, where $R > r$), the moment of inertia about its central axis is:

$$I = M \left( R^2 + \frac{3}{4} r^2 \right)$$

---

## 📚 Summary of Derivation Methods

| File | Primary Method | Geometric Element | Integration Variable & Range | Key Mathematical Tools |
| :--- | :--- | :--- | :--- | :--- |
| **`Torus_MOI_1.pdf`** | Concentric Cylindrical Shells | Thin cylindrical shells | Angle $\theta \in [0, \pi]$ | Double-angle trigonometric identities |
| **`Torus_MOI_2.pdf`** | Annular Disk / Horizontal Slices | Annular cylindrical disks | Height/position $x \in [-r, r]$ | Beta/Gamma functions ($\int \sin^m\theta \cos^n\theta \, d\theta$) |
| **`Torus_MOI_3.pdf`** | Concentric Hollow Torus Layering | 2D surface shell $\rightarrow$ 3D solid | Minor radius $x \in [0, r]$ | Surface integral + Radial layer integration |

---

## 🔍 Detailed Overview of Included Papers

### 1. Cylindrical Shell Method (`Torus_MOI_1.pdf`)
* **Title:** *Derivation of the Moment of Inertia of a Solid Torus via the Cylindrical Shell Method*
* **Core Concept:** Decomposes the 3D solid torus into a continuum of concentric cylindrical shells parametrized by the cross-sectional angle $\theta$.
* **Highlights:** 
  * Avoids toroidal coordinate system transformations.
  * Direct evaluation through single-variable integration over $\theta$.
  * Verifies total volume $V = 2\pi^2 R r^2$ via Pappus's Centroid Theorem.

---

### 2. Annular Disk / Horizontal Slicing Method (`Torus_MOI_2.pdf`)
* **Title:** *Rotational Inertia of an Annular Cylinder and a Donut-Shaped Solid Body (Torus) using Annular Disk*
* **Core Concept:** 
  1. First derives the rotational inertia of a thin annular cylinder: $I = \frac{1}{2}M(R^2 + r^2)$.
  2. Uses this base result to integrate horizontal annular slices of the torus along its vertical symmetry axis.
* **Highlights:**
  * Uses trigonometric substitution and Gamma Function identities ($\Gamma(3/2) = \frac{\sqrt{\pi}}{2}$) to evaluate $I_0 = \int_0^r x^2 \sqrt{r^2-x^2} \, dx$.
  * Provides a clear link between basic cylindrical geometry and toroidal geometry.

---

### 3. Hollow Torus Layering Method (`Torus_MOI_3.pdf`)
* **Title:** *Derivation of the Moment of Inertia of a Solid Torus via Hollow Torus Layering*
* **Core Concept:** A two-step geometric layering approach:
  1. **Part 1:** Calculates $I$ for an infinitely thin hollow toroidal shell of surface mass density: 
     $$I_{\text{hollow}} = M \left( R^2 + \frac{3}{2}r^2 \right)$$
  2. **Part 2:** Treats the solid torus as a continuous stack of concentric hollow toroidal shells of varying minor radius $x \in [0, r]$.
* **Highlights:**
  * Bridges 2D surface geometry with 3D volume distribution.
  * Simplifies the 3D volume integral into a straightforward single-variable radial integration over $x$.

---

## 📂 Repository Structure

```text
.
├── Torus_MOI_1.pdf    # Cylindrical Shell Method Derivation
├── Torus_MOI_2.pdf    # Annular Disk & Gamma Function Method Derivation
├── Torus_MOI_3.pdf    # Hollow Torus Layering Method Derivation
└── README.md          # Project documentation
```

---

## 👤 Author

**Md. Shahriar Parvez**  
Department of Mechanical Engineering  
Bangladesh University of Engineering and Technology (BUET)  
Dhaka, Bangladesh  
📧 Email: [sbijoy524@gmail.com](mailto:sbijoy524@gmail.com)  
🐙 GitHub: [@Md-Shahriar-Parvez](httpsprotocol://github.com/Md-Shahriar-Parvez)

---

## 📜 Citation & License

If you find these analytical notes helpful in your study or research, feel free to cite or reference this repository.

This project is open source and available under the [MIT License](LICENSE).