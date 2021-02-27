# Práctica 2 - Instalación y configuración de Visual Studio Code
* Elaborado por Eduardo Da Silva Yanes
## 1. Introduccion
En esta segunda práctica vamos a centrarnos más en el entorno de trabajo. Vamos a configurar el entorno de Visual Studio Code para poder trabajar cómodamente, instalando extensiones y configurando la conexión SSH.
Una vez hecho esto vamos a tener una primera toma de contacto con Typescript creando un "Hola mundo".
### Objetivos
## 2. Desarrollo de la práctica
### 2.1 Instalando VS Code
Visual Studio Code es uno de los entornos más populares entre desarrolladores. Lo primero que vamos a hacer es instalarlo en nuestra máquina local.
Si estamos en Windows podemos instalarlo como cualquier otra aplicación, descargando un ejecutable y ejecutandolo.
Si nos encontramos en un entorno Linux, como es nuestro caso, podemos realizar la instalación con los siguientes comandos:
```bash
...$  sudo apt install code
```
o haciendo uso de snap (otro gestor de paquetes)
```bash
...$  sudo apt install code
```
En mi caso particular ya tenía instalado VSCode y lo he usado previamente pero si es la primera vez que tienes contacto con este editor/"ide" es recomendable que mires algún tutorial o guía para saber cómo son las funcionalidades del programa. En la documentación de VSCode tenemos la sección de **[Manejo básico](https://code.visualstudio.com/docs/editor/codebasics)** donde podemos aprender un poco, a lo largo de varias guías, cómo usar este editor.

### 2.1 Conectándose remotamente usando VS Code
Lo primero que vamos a hacer es descargarnos la extensión [Remote-SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh). Gracias a esta extensión podremos conectarnos por SSH a la máquina del IaaS.
Una vez instalada podemos usar directamente la conexión SSH. Vemos que abajo a la izquierda hay un cuadradito verde. Podemos dar click ahí o presionar **F1** para abrir la paleta de comandos y luego buscamos **ssh**. Pulsamos sobre **Connect to host...**. Si hemos realizado todos los pasos de la [Práctica 1]() vemos que nos va a salir nuestra máquina iaas-dsi44. Si por algún motivo no hicimos esos pasos podemos hacer lo siguiente:Vamos a ir a **Configure SSH Hosts...** y elejimos la opción **~/.ssh/config**.
Ahora debemos introducir lo siguiente:
```
Host iaas-dsi44
  HostName iaas-dsi44 //o en lugar de iaas-dsi44 ponemos la ip
  User usuario
```
Recordemos que iaas-dsi44 es mi máquina del IaaS. Cada uno debe poner la que le corresponda.
Una vez hecho esto ya podemos hacer la conexión SSH. Como hemos dicho antes, presionamos en el icono verde de la esquina inferior izquierda o abrimos la paleta de comandos con **F1**, buscamos **ssh** y, en ambos casos, seleccionamos **Connect to host...**, seleccionando el host que acabamos de poner. Vemos que se nos abre una nueva ventana y en la esquina inferior izquierda vemos como pone que es una conexión ssh con iaas-dsi44. Abrimos una terminal en esta nueva ventana y lo primero que vemos es el característico prompt que configuramos en la práctica anterior pero de todos modos vamos a asegurarnos que estamos en el sitio correcto. Usemos el siguiente comando para verificarlo:
```bash
...$ hostname
iaas-dsi44
```


