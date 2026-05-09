# Notas de cinemática de vehículos terrestres

Estas notas contienen la derivación formal y matemática de la cinemática
directa e inversa de diferentes arquitecturas móviles terrestres.

Son notas personales que he decidido guardar en formato TeX y PDF para poder
consultarlas después cuando construyo paquetes de software para controlar
distintas plataformas móviles terrestres.

El texto no pretende ser breve. Algunas partes podrían condensarse, pero el
objetivo es que el documento pueda seguirse con más o menos experiencia en
álgebra matemática.

Los ficheros fuente y el PDF se proporcionan en inglés y en español:

| Idioma  | PDF | Fuente LaTeX |
|---------|-----|--------------|
| Inglés  | [kinematics_en.pdf](kinematics_en.pdf) | [kinematics_en.tex](kinematics_en.tex) |
| Español | [kinematics_es.pdf](kinematics_es.pdf) | [kinematics_es.tex](kinematics_es.tex) |

Parte de la implementación en ROS 2 de algunas de las arquitecturas descritas
aquí se encuentra en:

https://github.com/jfrascon/ground_vehicle_kinematics

## Contenido

- Restricciones físicas de una rueda.
- El papel de la descomposición en valores singulares, SVD, para calcular la
  cinemática directa e inversa.
- Un modelo ya desarrollado:
  - plataforma con 3 ruedas activas (`three swerve drive`).
- TODO:
  - plataforma diferencial.
  - plataforma Ackermann.
  - plataforma con 4 ruedas activas.
  - plataforma con ruedas mecanum.

