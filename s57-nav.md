S57 Navigation
====

Introducción
----
Mejoras a realizar para que GisViewer sirva como ECDIS para uso en navegación marítima.
Información extraída de: https://www.iho.int/iho_pubs/standard/S-52/S-52_e6.0_EN.pdf
En este apartado de navegación el "usuario final" es denominado "marinero"


Símbolos especiales para identificar zonas inseguras debido a su profundad
---------

Existen "features" que son importante para la seguridad en la navegación (pag 32):
* Contorno de seguridad.
* Sombreado por zonas de profundidad
* Profundidad de seguridad.
* Peligros aislados.

### Contorno de seguridad.

Es seleccionable por el marinero. Es posible que la profundidad selecconada por el marinero no esté disponible en todas las celdas. 
El programa debería notificarlo de alguna manera y marcar la siguiente profundidad conocida. 

Valor por defecto es 30 metros.  DEPCNTnn

### Sombreado por zonas de profundidad (depth shades). 

Se deben mostrar en distinto color zomas más profundas de las zonas menos profundas. El límite de cambio de color quedará establecido por los valores de seguridad elegidos por el marinero.

Zonas mínimas de produndidad diferenciables mediante tonos de color.

* deep water: deeper than the safety contour (colour token DEPDW)
* shallow water: shallower than the safety contour (colour token DEPVS)
* intertidal area: area exposed at low water (colour token DEPIT)
 
Por la noche (en modo nocturno) debe ser claramente distinguible los tres tonos de profundidad.

Es recomendable que el ECDIS permita al marinero elegir entre estas 5 zonas:

* deep water: deeper than the deep contour (colour token DEPDW),
* medium-deep water: depths between the deep contour and the safety contour (DEPMD),
* medium-shallow: depths between the safety contour and the shallow contour (DEPMS),
* very shallow water: depths between the shallow contour and zero metre contour (DEPVS)
* drying foreshore: intertidal area (DEPIT)

Por defecto se pueden usar los siguientes valores para las anteriores profundidades

* deep water: a partir de 30 m.
* medium-deep water: nivel de seguridad del propio barco (DEPMD),
* medium-shallow: 2 m hasta el nivel de seguridad del propio barco (DEPMS),
* very shallow water: 0 a 2 m (DEPVS)
* drying foreshore: expuesto en marea baja (DEPIT)
 
### Peligros aislados.

Hay objetos S57 que pueden servir de aviso de peligro durante la navegación:

* SOUNDG : Hay puntos marcados como especiales por estar muy por encima o por debajo de los puntos de alrededor.
* WRECK
* ...

[[ This is yellow alert. ]]

<div class="alert alert-error">Another red alert.</div>

