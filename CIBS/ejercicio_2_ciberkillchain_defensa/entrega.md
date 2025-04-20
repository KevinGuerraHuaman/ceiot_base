
## Ejercicio CiberKillChain - Defensa

### Alumno : Kevin Guerra Huamán

### Medidas para la defensa


1. 🔍 **Actions on Objectives**  
   - Detección: Monitorear el tráfico de red para detectar transferencias inusuales de datos, como archivos comprimidos con llaves de seguridad enviados a servidores externos, usando herramientas como Forcepoint DLP implementados en los servidores de la nube.  
   - Mitigación: Implementar políticas DLP para bloquear transferencias de datos sensibles. Además, cifrar credenciales y llaves de seguridad, a traves de herramientas como VeraCrypt, para que sean inútiles si se exfiltran los archivos.


2. 🛠️ **Command and Control**  
   - Detección: Configurar firewalls y sistemas de monitoreo de red para identificar tráfico en puertos no estándar que indique conexiones a servidores externos.  
   - Mitigación:Bloquear puertos no estándar y establecer reglas de firewall en el modem de internet Huawei para permitir solo tráfico esencial. Además, usar segmentación de red para limitar el alcance de conexiones sospechosas.


3. 📦 **Installation**  
   - Detección: Monitorear cambios en configuraciones de inicio y tareas programadas mediante herramientas de auditoría como Splunk para identificar mecanismos de persistencia de malware.  
   - Mitigación: Restringir permisos para modificar configuraciones de inicio o tareas programadas, se puede utilizar la herramietan Tripwire instalada en la placa reducida. También, implementar sistemas de integridad que reviertan cambios no autorizados.


4. 🚀 **Exploitation**
   - Detección: Usar herramientas de seguridad de endpoints (EDR) como SentinelOne para monitorear la ejecución automática de scripts mediante intérpretes como Bash o Python al conectar dispositivos USB.  
   - Mitigación: Configurar políticas de control de aplicaciones para impedir la ejecución de binarios no firmados o no autorizados.

5. 🖥️ **Delivery**  
   - Detección: Implementar software de gestión de endpoints como SentinelOne para registrar y alertar sobre la conexión de dispositivos USB no autorizados, como Flipper Zero o BadUSB.  
   - Mitigación: Deshabilitar puertos USB en dispositivos críticos o configurar políticas de "solo lectura" para evitar la ejecución de scripts desde dispositivos externos. Usar listas blancas de dispositivos permitidos.

6. 🎛️ **Weaponization**  
   - Detección: Monitorear actividades internas para detectar el uso no autorizado de herramientas o scripts que puedan ser configurados como maliciosos para ataques a través de puertos USB. En este caso se puede utilizar herramientas como SentinelOne o Okta para el monitoreo y ocntorl de acceso.  
   - Mitigación: Restringir el acceso a herramientas de desarrollo y scripting solo a personal autorizado. Implementar auditorías regulares para detectar configuraciones sospechosas.


7. 🎯 **Reconnaissance**  
   - Detección: Listar al personal con nivel de acceso y conocimiento en la implementación para identificar con mayor facilidad la filtración de información. Además, se puede implementar monitoreo de correo electronicos para identificar intentos de phishing dirigidos a otbener información del proyecto.  
   - Mitigación: Capacitar al personal en la identificación de intentos de phishing y establecer políticas de no divulgación de información técnica. También, cubrir los dispositivos para dificultar el reconocimiento a simple vista.
