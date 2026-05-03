# Ground Robotics Kinematics

### A Generalized Framework for Forward and Inverse Kinematics of Wheeled Terrestrial Robots

> *Rigorous analytical development of wheel kinematics — from first principles to SVD-based numerical solvers.*

---

## What is this?

A self-contained technical document that builds — from scratch — a **unified kinematic framework** for wheeled ground robots. Whether you are working with a humble differential drive, an Ackermann car, a Mecanum-wheeled platform, or a full swerve drive, the same matrix formulation applies.

The document is available in two languages:

| Language | PDF | LaTeX source |
|----------|-----|--------------|
| English  | [kinematics_en.pdf](kinematics_en.pdf) | [kinematics_en.tex](kinematics_en.tex) |
| Spanish  | [kinematics_es.pdf](kinematics_es.pdf) | [kinematics_es.tex](kinematics_es.tex) |

---

## What you will find inside

### 1 · Motion constraints imposed by the wheels

A coordinate-frame approach to modeling how each wheel constrains the chassis motion. Covers:

- The **no-lateral-slip constraint** for conventional (steerable and non-steerable) wheels.
- Why **Mecanum / omnidirectional** wheels break that constraint and what it implies.
- The **wheel base frame** $\mathcal{B}_i$: a stable, time-invariant reference attached to each wheel mounting point that makes the matrix derivation clean and general.

<p align="center">
  <img src="images/wheel_placement.png" width="49%" alt="Wheel placement">
  <img src="images/rolling_direction.png" width="49%" alt="Rolling direction">
</p>

### 2 · A single matrix equation for any wheeled platform

For a robot with $N$ wheels the kinematics collapses to:

$$A\mathbf{x} = \mathbf{b}, \qquad A \in \mathbb{R}^{2N \times 3}$$

where $\mathbf{x} = [V_{r,x},\; V_{r,y},\; \omega_{r,z}]^\top$ is the chassis velocity and $\mathbf{b}$ stacks the individual wheel velocity measurements. Because $2N > 3$ for any practical robot, the system is **overdetermined** — and that is a feature, not a bug.

### 3 · Least squares, pseudoinverse, and SVD

Real robots carry encoder noise, wheel slip, and calibration errors. The document walks through:

- Why the **Normal Equations** $(A^\top A)^{-1} A^\top \mathbf{b}$ can be numerically catastrophic.
- How **Singular Value Decomposition** $A = U \Sigma V^\top$ gives the Moore-Penrose pseudoinverse $A^+ = V \Sigma^+ U^\top$ reliably and safely — with a complete, step-by-step algebraic proof.
- The **condition number** $\kappa = \sigma_{\max} / \sigma_{\min}$ as a diagnostic tool: how to interpret it, why a high $\kappa$ reveals a *mechanical design flaw*, and why SVD should never be used as an excuse to ignore bad geometry.

### 4 · Concrete robot topologies worked out in full

| Platform | Inverse kinematics | Forward kinematics |
|----------|-------------------|-------------------|
| Three-wheel swerve drive (Y / inverted-Y) | ✓ | ✓ |
| Four-wheel swerve drive | ✓ | ✓ |
| *(same framework applies to diff-drive, Ackermann, Mecanum)* | | |

<p align="center">
  <img src="images/three_swerve_drive_configuration.png" width="60%" alt="Three swerve drive configurations">
</p>

---

## Who is this for?

- Robotics engineers implementing **wheel odometry** or **chassis velocity estimators**.
- Students learning how to derive kinematics systematically instead of case-by-case.
- Anyone who has wondered *why* you should use SVD instead of just inverting a matrix.

---

## Prerequisites

The document assumes familiarity with basic linear algebra (matrix products, transpose, eigenvalues) and rigid-body kinematics (reference frames, cross products). Everything else — SVD, pseudoinverse, condition number — is derived from first principles.

---

## Author

**Juan Francisco Rascón Crespo**

---

*Feedback, corrections and pull requests are welcome.*
