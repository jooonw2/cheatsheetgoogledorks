# Google Dorks

Los Google Dorks son combinaciones específicas de palabras o frases que se usan para realizar búsquedas avanzadas en Google y obtener resultados que no se pueden obtener mediante una búsqueda normal.

## **Cheatsheet**

| Operador | Descripción del operador | Ejemplo | Descripción de ejemplo |
| --- | --- | --- | --- |
| `site:` | Limita los resultados a un sitio web o dominio específico. | `site:example.com` | Encuentra todas las páginas de acceso público en example.com. |
| `inurl:` | Encuentra páginas con un término específico en la URL. | `inurl:login` | Busca páginas de inicio de sesión en cualquier sitio web. |
| `filetype:` | Busca archivos de un tipo particular. | `filetype:pdf` | Encuentra documentos PDF descargables. |
| `intitle:` | Busca páginas con un término específico en el título. | `intitle:"confidential report"` | Busca documentos titulados "informe confidencial" o variaciones similares. |
| `intext:`o `inbody:` | Busca un término dentro del cuerpo del texto de las páginas. | `intext:"password reset"` | Identifica páginas web que contengan el término "restablecimiento de contraseña". |
| `cache:` | Muestra la versión en caché de una página web (si está disponible). | `cache:example.com` | Ve la versión en caché de example.com para ver su contenido anterior. |
| `link:` | Encuentra páginas que enlazan a una página web específica. | `link:example.com` | Identifica los sitios web que enlazan con example.com. |
| `related:` | Encuentra sitios web relacionados con una página web específica. | `related:example.com` | Descubre sitios web similares a example.com. |
| `info:` | Proporciona un resumen de información sobre una página web. | `info:example.com` | Obtiene detalles básicos sobre example.com, como su título y descripción. |
| `define:` | Proporciona definiciones de una palabra o frase. | `define:phishing` | Obtiene una definición de "phishing" de varias fuentes. |
| `numrange:` | Busca números dentro de un rango específico. | `site:example.com numrange:1000-2000` | Busca páginas en example.com que contengan números entre 1000 y 2000. |
| `allintext:` | Busca páginas que contengan todas las palabras especificadas en el cuerpo del texto. | `allintext:admin password reset` | Busca páginas que contienen "admin" y "restablecer contraseña" en el texto del cuerpo. |
| `allinurl:` | Busca páginas que contengan todas las palabras especificadas en la URL. | `allinurl:admin panel` | Busca páginas con "admin" y "panel" en la URL. |
| `allintitle:` | Busca páginas que contengan todas las palabras especificadas en el título. | `allintitle:confidential report 2023` | Busca páginas que tengan "confidencial", "informe" y "2023" en el título. |
| `AND` | Limita los resultados al exigir que todos los términos estén presentes. | `site:example.com AND (inurl:admin OR inurl:login)` | Encuentra páginas de administración o inicio de sesión específicamente en example.com. |
| `OR` | Amplia los resultados incluyendo páginas con cualquiera de los términos. | `"linux" OR "ubuntu" OR "debian"` | Busca páginas web que mencionen Linux, Ubuntu o Debian. |
| `NOT` | Excluye los resultados que contienen el término especificado. | `site:bank.com NOT inurl:login` | Busca páginas en bank.com, excluidas las páginas de inicio de sesión. |
| `*`(comodín) | Representa cualquier carácter o palabra. | `site:socialnetwork.com filetype:pdf user* manual` | Busca manuales de usuario (guía de usuario, manual de usuario) en formato PDF en socialnetwork.com. |
| `..`(búsqueda de rango) | Encuentra resultados dentro de un rango numérico específico. | `site:ecommerce.com "price" 100..500` | Busca productos con precios entre 100 y 500 en un sitio web de comercio electrónico. |
| `" "`(comillas) | Busca frases exactas. | `"information security policy"` | Busca documentos que mencionen la frase exacta "política de seguridad de la información". |
| `-`(signo menos) | Excluye términos de los resultados de búsqueda. | `site:news.com -inurl:sports` | Busca artículos de noticias en news.com, excluyendo contenido relacionado con deportes |

## **Ejemplos**

| Google Dork | Descripción |
| --- | --- |
| `intitle:"Index of" password.txt` | Muestra directorios que contienen archivos de texto con nombres como "password.txt". |
| `intitle:"Index of" /admin` | Muestra directorios de administración en sitios web. |
| `filetype:xls inurl:"email.xls"` | Muestra listado de emails expuestos |
| `inurl:"login" site:example.com` | Encuentra páginas de inicio de sesión en un sitio web específico |
| `filetype:log inurl:"password.log"` | Encuentra archivos de registro (logs) que contienen "password" en su nombre. |
| `intitle:index.of id_rsa -id_rsa.pub` | Encuentra claves privadas SSH |
| `site:.gov intitle:"secret" filetype:pdf` | Encuentra acrchivos gubernamentales expuestos en internet |
| `intext:"Welcome to phpMyAdmin"` | Busca páginas que contienen la cadena "Welcome to phpMyAdmin" en su contenido. |
| `inurl:/wp-content/uploads/ filetype:pdf` | Encuentra archivos PDF en la carpeta de "uploads" de sitios web basados en WordPress. |
| `intitle:"Index of" /backup` | Muestra directorios que contienen archivos de backup. |
| `site:example.com ext:sql` | Encuentra archivos SQL en el sitio web especificado. |
| `intitle:"index of" "database.sql"` | Encuentra archivos de bases de datos SQL |
| `intitle:"SQL Injection" site:example.com` | Encuentra páginas web que contienen la frase "SQL Injection" en un sitio web específico |
| `site:example.com ext:doc` | Encuentra documentos de Microsoft Word en el sitio web especificado. |
| `site:example.com ext:xml` | Encuentra documentos Excel en el sitio web especificado. |
| `site:example.com ext:conf` | Busca archivos de configuración en el sitio web especificado. |
| `inurl:"/cgi-bin/pass.txt"` | Busca archivos de texto con nombres como "pass.txt" en carpetas de "cgi-bin". |
| `intitle:"WebcamXP 5"` | Encuentra cámaras web accesibles a través de WebcamXP 5. |
| `site:example.com inurl:config` | Busca archivos de configuración en el sitio web especificado. |
| `intitle:"index of" intext:config.php` | Muestra directorios que contienen archivos de configuración PHP. |
| `intitle:"index of" intext:.htpasswd` | Encuentra directorios que contienen archivos .htpasswd. |
| `intitle:"index of" intext:.env` | Busca directorios que contengan archivos .env. |
| `intitle:"index of" "wp-content/uploads" site:example.com` | Encuentra archivos cargados en WordPress en un sitio web específico |
| `filetype:xls inurl:"email.xls"` | Encuentra archivos de hojas de cálculo Excel que contienen "email" en su nombre. |
| `intext:"Powered by phpBB"` | Muestra sitios web que utilizan el sistema de gestión de contenido phpBB. |
| `intext:"Powered by Wordpress"` | Muestra sitios web que utilizan Wordpress. |
| `intext:"@outlook.com" site:example.com` | Encuentra webs que contienen direcciones de correo de Outlook en un sitio específico |
| `inurl:/dana-na/ filetype:cgi` | Encuentra páginas CGI en la carpeta "/dana-na/". |
| `inurl:server-info "Apache Server Information"` | Muestra información del servidor Apache. |
| `intext:"sql syntax near"` | Muestra webs con posibles errores de SQL |
| `intext:"confidential" site:example.com` | Encuentra páginas web que contienen la palabra "confidencial" en un sitio web específico |
| `inurl:/proc/self/cwd` | Muestra el directorio de trabajo actual de un servidor. |
| `intitle:"index of" intext:web.config` | Encuentra archivos de configuración web en directorios indexados. |
| `filetype:reg reg HKEY_CURRENT_USER username` | Busca archivos de registro (registries) que contengan la cadena "username" en la clave HKEY_CURRENT_USER. |
| `inurl:"ViewerFrame?Mode="` | Encuentra cámaras web accesibles a través de scripts de visualización. |
| `intext:"powered by vBulletin"` | Muestra sitios web que utilizan el sistema de gestión de contenido vBulletin. |
| `intitle:"index of" inurl:ftp` | Encuentra servidores FTP que tienen directorios indexados. |
| `intitle:"index of" "WhatsAppDB.csv"` | Muestra directorios que contienen archivos CSV de bases de datos de WhatsApp. |
| `filetype:env intext:APP_ENV` | Busca archivos de configuración con información sobre el entorno de la aplicación. |
| `inurl:"/phpinfo.php"` | Muestra información sobre el servidor PHP. |
| `intitle:"index of" intext:sftp-config.json` | Encuentra archivos de configuración SFTP en directorios indexados. |

## **Ejemplos comunes**

### **Encontrar páginas de inicio de sesión:**

- `site:example.com inurl:login`
- `site:example.com (inurl:login OR inurl:admin)`

### **Identificar de archivos expuestos:**

- `site:example.com filetype:pdf`
- `site:example.com (filetype:xls OR filetype:docx)`

### **Descubrir archivos de configuración:**

- `site:example.com inurl:config.php`
- `site:example.com (ext:conf OR ext:cnf)`(busca extensiones comúnmente utilizadas para archivos de configuración)

### **Localizar copias de seguridad de bases de datos:**

- `site:example.com inurl:backup`
- `site:example.com filetype:sql`
## Operadores adicionales

| Operador         | Descripción del operador                                                                 | Ejemplo                                  | Descripción del ejemplo                                                                 |
|-------------------|-----------------------------------------------------------------------------------------|------------------------------------------|-----------------------------------------------------------------------------------------|
| `cache:`          | Muestra la versión en caché de una página almacenada por Google.                        | `cache:example.com`                      | Accede a la última versión en caché de example.com.                                     |
| `related:`        | Encuentra sitios relacionados al dominio especificado.                                  | `related:example.com`                    | Muestra sitios similares o relacionados con example.com.                                |
| `allintext:`      | Busca páginas que contengan todas las palabras especificadas en el texto.               | `allintext:seguridad cibernética`        | Encuentra páginas que mencionen "seguridad" y "cibernética" en su contenido.            |
| `allintitle:`     | Busca páginas que contengan todas las palabras especificadas en el título.              | `allintitle:curso hacking ético`         | Encuentra páginas con títulos que incluyan "curso" y "hacking ético".                   |
| `allinurl:`       | Busca páginas que contengan todas las palabras especificadas en la URL.                 | `allinurl:admin login`                   | Encuentra URLs que incluyan las palabras "admin" y "login".                             |
| `numrange:`       | Busca páginas que contengan números dentro de un rango específico.                      | `numrange:2010-2020`                     | Encuentra páginas con números entre 2010 y 2020.                                        |
| `OR`              | Busca resultados que incluyan cualquiera de las palabras especificadas.                 | `seguridad OR hacking`                   | Encuentra páginas relacionadas con seguridad o hacking.                                 |
| `AND`             | Fuerza a que los resultados incluyan todas las palabras especificadas (implícito).      | `seguridad AND hacking`                  | Encuentra páginas que contengan tanto "seguridad" como "hacking".                       |
| Combinaciones     | Usa múltiples operadores para afinar aún más tus búsquedas.                             | `site:example.com filetype:pdf "manual"` | Encuentra manuales en formato PDF dentro de example.com.                                |

## Ejemplo de búsqueda avanzada

Si quieres encontrar documentos PDF sobre hacking ético publicados en dominios educativos:

```
site:edu filetype:pdf "hacking ético"
```

Esto limitará los resultados a archivos PDF en sitios web con el dominio `.edu` que mencionen "hacking ético".

---

Estos operadores expanden significativamente las posibilidades de búsqueda avanzada en Google.
