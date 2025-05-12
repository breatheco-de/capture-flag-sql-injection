# GOSSIP - Alabama Suites Internal Panel

Bienvenido a **GOSSIP**, un laboratorio donde pondrás a prueba tus habilidades para detectar vulnerabilidades de inyección SQL, romper contraseñas y leer entre líneas para descubrir al verdadero saboteador.

Esta aplicación simula el sistema interno de un hotel corporativo llamado **Alabama Suites**, donde todo parece tranquilo... hasta que comienzas a escarbar los datos. Tu objetivo será acceder a la base de datos de la aplicación, obtener las contraseñas de todos los usuarios, entrar como cada uno y **descubrir quién está saboteando a Diego**.

<how-to-start>
   
## 🌱 Cómo iniciar este laboratorio

Sigue las siguientes instrucciones para comenzar:

1. **Descarga la máquina virtual** desde este [enlace]().
2. **Importa la máquina** en tu gestor de virtualización preferido (VirtualBox, VMware, etc.).
3. Una vez iniciada la máquina, ¡ya puedes comenzar con el laboratorio!
</how-to-start>


## 📄 Instrucciones

1. **Descubre la dirección IP de la máquina**: Utiliza herramientas como `nmap`, `netdiscover` o `arp-scan`.

2. **Escanea los puertos abiertos**  

3. **Visita la página web en tu navegador**: Ingresa a `http://<IP>/gossip/` y explora el portal.

4. **Prueba el login en `/gossip/login.php`**: No todo es lo que parece... ¡usá SQLMap! 😉

5. **Usa SQLMap para explotar la inyección SQL**: Extrae la tabla `users` y obten las contraseñas.

6. **Crackeá las contraseñas MD5**

7. **Descubre la verdad**: Lee cada panel de los usuarios y deduce **¿quién está saboteando a Diego?**

¡Feliz hackeo!

