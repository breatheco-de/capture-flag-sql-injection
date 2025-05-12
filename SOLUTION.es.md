# Guía para el Instructor — Laboratorio GOSSIP

Este laboratorio pone a prueba la capacidad del alumno para detectar vulnerabilidades en el login de una aplicación web, explotar una inyección SQL, crackear contraseñas y descubrir mediante deducción narrativa quién saboteó a un compañero de trabajo.

A través de este laboratorio los alumnos lograrán comprender:

- Identificación y explotación de una inyección SQL con SQLMap.
- Extracción y descifrado de contraseñas MD5.
- Análisis narrativo de paneles de usuarios simulados.
- Deducción lógica a partir de mensajes cruzados.
- Acceso a una flag final mediante uso realista del login.



## Especificaciones de la máquina 🖥️

- **Sistema:** Ubuntu Server (sin GUI)
- **Servidor web:** Apache
- **Ruta del sitio:** `/var/www/html/gossip/`
- **Contenido vulnerable:** Formulario de login vulnerable a SQL Injection (`login.php`)
- **Base de datos:** `gossip_db` con usuarios y contraseñas MD5
- **Usuarios del sistema:** ninguno, todo es vía web

- **Usuarios en la base de datos:**
  - Diego → coffee123 → `md5('coffee123')`
  - Sarah → password! → `md5('password!')`
  - Karen → trustno1 → `md5('trustno1')`
  - William → securepass → `md5('securepass')`

- **Flag accesible desde el panel web de:** `William`
- **Contenido de la flag:** `4GEEKS{D13G0_Y0u_4re_f1red!!!}`

> **Nota:** no se requiere escalada de privilegios ni conexión SSH

### Credenciales de la máquina

```bash
servername: gossip-lab
username: student
password: 4geeks-lab
```

## Pasos esperados por el alumno

1. **Realiza reconocimiento de red para identificar la máquina.**
   - Utiliza herramientas como `nmap`, `netdiscover` o `arp-scan`.
   - Debe detectar una IP con el puerto **80 (HTTP)** abierto.

2. **Accede al sitio web desde el navegador.**
   - Introduce la IP descubierta en el navegador para cargar la landing page de Alabama Suites.

3. **Identifica el formulario vulnerable en `/gossip/login.php`.**
   - Puede ingresar valores manuales para comprobar su funcionamiento.

4. **Utiliza SQLMap para explotar la vulnerabilidad.**
   - Extrae la base de datos `gossip_db` y la tabla `users`.
   - Obtiene las contraseñas en MD5.

5. **Crackea las contraseñas con John, Hashcat o CrackStation.**
   - Obtiene los accesos de los usuarios: Diego, Sarah, Karen y William.

6. **Se loguea como cada usuario y analiza el contenido del panel.**
   - Debe leer los mensajes cruzados y contenidos falsos o distractores.

7. **Deducir que Karen es quien saboteó a Diego.**
   - La justificación aparece en su panel en un mensaje dirigido a Freddy.

8. **Obtener la flag desde el panel de William.**
   - La flag está claramente visible en su escritorio.