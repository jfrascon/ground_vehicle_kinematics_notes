# Ground Vehicle Kinematics Notes

These notes contain the formal mathematical derivation of the direct and inverse
kinematics of different ground vehicle architectures.

They are personal notes that I decided to keep in TeX and PDF so I can consult
them later when I create software packages for controlling different terrestrial
mobile platforms.

The text is intentionally not brief. Some parts could be shortened, but the goal
is that readers with more or less experience in mathematical algebra can still
follow the document.

The source files and the PDF are provided in English and Spanish:

| Language | PDF | LaTeX source |
|----------|-----|--------------|
| English  | [kinematics_en.pdf](kinematics_en.pdf) | [kinematics_en.tex](kinematics_en.tex) |
| Spanish  | [kinematics_es.pdf](kinematics_es.pdf) | [kinematics_es.tex](kinematics_es.tex) |

Some of the ROS 2 implementations of the architectures described here are in:

https://github.com/jfrascon/ground_vehicle_kinematics

## Contents

- Physical constraints of a wheel.
- The role of Singular Value Decomposition in the computation of direct and
  inverse kinematics.
- One worked model:
  - three active wheel platform (`three swerve drive`).
- TODO:
  - differential platform.
  - Ackermann platform.
  - four active wheel platform.
  - mecanum wheel platform.

