# Herramientas propias del sistema

## Monitorización de procesos

### ps

Muestra los procesosen ejecución.

![1](img/1.png)

### ps aux

Muestra información más detallada.

![4](img/4.png)

### ps -C nano

Busca un proceso, en este caso sería "nano". Para más información añadimos u.

![6](img/6.png)

Para ver los 5 procesos que más CPU consumen usamos el comando **ps -eo pid,user,%cpu,%mem,etime,command --sort=-%cpu**

![7](img/7.png)

### top

Muestra una lista de procesos ordenados por consumo de recursos.

![8](img/8.png)

Con el comando **top -b -n 3 -o %CPU > top.txt** se ejecuta top, actualiza la lista de procesos 3 veces, ordena los procesos por el uso de CPU y guarda el resultado en el archivo top.txt.

![10](img/10.png)

### atop

Muestra información detallada sobre el uso de recursos como CPU, memoria, disco, red y procesos individuales.

![13](img/13.png)

## Monitorización de la red

### tcpdump

Captura y analiza paquetes de red.

![22](img/22.png)

Usamos el comando **tcpdump -i eno1** para capturar los paquetes de nuestra red.

![23](img/23.png)

Para ver la salida de tcpdump lo redirigimos a un archivo con **tcpdump -i eno1 -w capturas**.

No podremos leer el contenido del archivo porque está encriptado.
Para que sea legible usamos **tcpdump -r capturas**.

![26](img/26.png)

### tcptrack

Se utiliza para monitorear conexiones TCP en tiempo real. 

![27](img/27.png)

### iptraf

Se utiliza para la monitorización de red pero se centra en proporcionar una visión general de la actividad de red.

![28](img/28.png)

![29](img/29.png)

### bmon

Se utiliza para monitorear el uso de ancho de banda en tiempo real. 

![30](img/30.png)

## Monitorización de almacenamiento

### free

Muestra la cantidad de memoria libre y utilizada que tiene el sistema.

Con **free -h**, la salida es mas legible y con **free -s** se puede ver en intervalos de 3 segundos.

![15](img/15.png)

### df -h

Se utiliza para ver el espacio en disco tanto disponible como usado.

![16](img/16.png)

### du -sh 

Se utiliza para mostrar el espacio utilizado y disponible en el sistema de archivos, de una manera resumida y fácil de leer.

![18](img/18.png)

En este caso se especifica la ruta.

### iostat

Proporciona estadísticas de entrada/salida del sistema, relacionadas con el uso de dispositivos de almacenamiento y la carga del CPU.

![19](img/19.png)

Con el comando **iostat -x nvm0n1** se mostra estadísticas detalladas de rendimiento del dispositivo de almacenamiento nvme0n1.

![20](img/20.png)

Con el comando **iostat -x nvm0n1 -s 5** se muestra lo mismo de antes pero en intervalos de 5 segundos.

![21](img/21.png)
