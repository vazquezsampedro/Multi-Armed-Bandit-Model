* El problema del "***Bandido Multi-Brazo***" es un problema clásico del aprendizaje por refuerzo basado en el ***juego de las máquinas "tragaperras"*** donde se "tira del brazo" (palanca) de la "tragaperras" y se obtiene una recompensa por el juego, positiva si se gana dinero o negativa si perdemos el dinero.


* A este problema se le conoce como el problema del "Bandido Multi-Brazo" al denominarse una máquina "tragaperras" como "Bandido de un solo brazo". Cuando se juega a varias máquinas "tragaperras" se denomina "Bandido de Multiples Brazos", de ahí el nombre de "Multi Armed Bandit" (MAB):



* El objetivo de este problema es el de ***jugar un 'P' partidas a las 'K' "tragaperras" y obtener el mayor beneficio posible*** (la mayor recompensa posible).


* Para ello tendremos que ir jugando partidas en las 'K' "tragaperras" y descubrir cual es la distribución de probabilidad de obtener premio en cada una de las "tragaperras". Con esto conseguiremos saber a ***que máquinas jugar y en que orden para máximizar nuestros beneficios (o recompensas)***.



* Para resolver este problema definimos el $Q(a)$ como la ***recompensa media (beneficios medios) recibida por partida en la "tragaperras"*** $a$ y se calcula como:


$$Q(a) = \frac{R_a}{N_a}$$


* Siendo:
    + $R_a$: Suma de las recompensas (beneficiós) obtenidos en la "tragaperras" $a$.
    + $N_a$: Número total de partidas jugadas en la "tragaperras" $a$.
    
    
* El ***objetivo es encontrar la máquina "tragaperras" que mayor beneficio (recompensa) dé***:

$$Q(a^{*}) = max Q(a)$$


* Siendo:
    + $a^{*}$: El conjunto de las 'K' "tragaperras" a las que se juega.
    
    
* En este problema es muy importante aplicar correctamente los conceptos de **"Explotación" y "Exploración"** ya que si solo nos dedicamos a "*Explorar*" obtendremos el valor medio de recompensas que dén las 'K' "tragaperras" y si solo nos dedicamos a "*Explotar*" obtendremos la recompensa que nos dé la primera "tragaperras" a la que jugemos.


* Para ello debemos de seguir una política conocida como "***epsilon-greedy policy***" la cual seleccionará una "tragaperras" al azar con probabilidad $\epsilon$ para jugar y *explorar* o seleccionará la mejor "tragaperras" con probabilidad $1-\epsilon$.
