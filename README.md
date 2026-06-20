# Práctica SISO: Simulador de Planificación de Procesos en Bash

Este repositorio alberga el proyecto práctico desarrollado para la asignatura de Sistemas Operativos (SISO). Fundamentalmente, se trata de un simulador escrito íntegramente en Bash que modela las políticas de gestión de CPU a nivel del núcleo del sistema. 

A veces, prescindir de lenguajes de alto nivel y volver a las bases de la terminal es la estrategia más efectiva para asimilar la teoría subyacente. En este script, he implementado los siguientes algoritmos clásicos de planificación:

* **FCFS** (First Come, First Served) - Política estricta de orden de llegada.
* **SJF** (Shortest Job First) - Priorización basada en la ráfaga de CPU más corta.
* **MFU** (Most Frequently Used).
* Se incluyen también variaciones algorítmicas adicionales (NC y R) para evaluar diferentes escenarios de rendimiento.

Ciertamente, gestionar estructuras de datos complejas y colas de espera utilizando exclusivamente herramientas nativas de shell script presenta desafíos técnicos particulares. No obstante, el resultado ofrece una aproximación bastante fiel a cómo un sistema operativo real administra sus recursos y toma decisiones de asignación.

## Ejecución directa en la nube

Para facilitar la revisión técnica del código y evitar a los evaluadores o reclutadores la tediosa tarea de configurar un entorno local, he desplegado la herramienta en una plataforma online. 

Es posible interactuar con la consola de manera inmediata y gratuita a través del siguiente enlace:
👉 **[Ejecutar simulador en Replit](https://replit.com/@arkadigo/FCFS-SJF-MFU-NC-R)**

El procedimiento es sumamente sencillo: una vez acceda a la URL, pulse el botón **Run** ubicado en la parte superior. La terminal interactiva se inicializará en el panel derecho, presentándole el menú principal para comenzar la simulación.

## Arquitectura del repositorio

Sobre la organización interna de los directorios, he optado por mantener una estructura lo más limpia y semántica posible:

* `Script/`: Directorio principal que aloja el código fuente (`script.sh`).
* `FDatos/`: Contiene los conjuntos de datos de prueba preconfigurados. Decidí incluir estos ficheros para agilizar las pruebas de escritorio; de este modo, es posible cargar lotes enteros de procesos (con sus respectivos tiempos de llegada y ráfagas de ejecución) sin necesidad de introducirlos manualmente en cada iteración.

## Despliegue en entorno local

Si dispone de un entorno Linux nativo —o en su defecto, WSL configurado en sistemas Windows— y prefiere la ejecución tradicional desde su propia terminal, los comandos estándar son suficientes:

```bash
# Clonar el repositorio (sustituye por el nombre real de tu repositorio si cambia)
git clone [https://github.com/arkadigo04/practica-siso.git](https://github.com/arkadigo04/practica-siso.git)

# Acceder al directorio del código
cd practica-siso/Script

# Otorgar permisos de ejecución al archivo principal
chmod +x script.sh

# Iniciar el simulador
./script.sh
