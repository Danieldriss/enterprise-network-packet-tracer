# NexaCorp - Diseño Inicial de la Red

## 1. Descripción General del Proyecto

NexaCorp es una empresa tecnológica ficticia utilizada para diseñar e implementar una infraestructura de red empresarial completa en Cisco Packet Tracer.

El objetivo principal de este proyecto es aprender conceptos de redes de forma progresiva, comenzando por los fundamentos básicos y avanzando hacia tecnologías empresariales más complejas, mientras se documenta todo el proceso de diseño, implementación, verificación y resolución de problemas.

La red será diseñada teniendo en cuenta la escalabilidad, segmentación, seguridad, disponibilidad y administración centralizada.

---

## 2. Sedes de la Empresa

NexaCorp cuenta con aproximadamente 320 empleados distribuidos entre tres sedes:

| Ubicación | Tipo | Empleados |
|---|---|---:|
| Málaga | Sede principal (HQ) | 200 |
| Madrid | Sucursal 01 | 80 |
| Sevilla | Sucursal 02 | 40 |
| **Total** | | **320** |

---

## 3. Sede Principal de Málaga

Málaga es la sede principal de NexaCorp y concentra el mayor número de usuarios y la mayor parte de la infraestructura central de la empresa.

### Departamentos

| Departamento | Empleados |
|---|---:|
| Dirección | 10 |
| Administración | 20 |
| Finanzas | 20 |
| Recursos Humanos | 15 |
| Ventas | 50 |
| Desarrollo | 60 |
| IT / Sistemas | 25 |
| **Total** | **200** |

Además de los dispositivos de los empleados, la sede principal contará con infraestructura y servicios de red como:

- Servidores
- Impresoras de red
- Teléfonos IP
- Puntos de acceso inalámbricos
- Switches
- Routers
- Firewall
- Dispositivos de administración de red
- WiFi corporativo
- WiFi para invitados
- Red interna de servidores
- DMZ

---

## 4. Sucursal de Madrid

Madrid es la sucursal más grande de NexaCorp, con aproximadamente 80 empleados. Cuenta con su propia infraestructura de red local y mantiene conectividad con la sede principal de Málaga.

### Departamentos

| Departamento | Empleados |
|---|---:|
| Administración | 10 |
| Ventas | 35 |
| IT / Soporte | 10 |
| Operaciones | 25 |
| **Total** | **80** |

La sucursal de Madrid contará con:

- Ordenadores y portátiles de empleados
- Impresoras de red
- Teléfonos IP
- Puntos de acceso inalámbricos
- WiFi corporativo
- WiFi para invitados
- Switches
- Router
- Dispositivos de administración de red

---

## 5. Sucursal de Sevilla

Sevilla es la sucursal más pequeña de NexaCorp, con aproximadamente 40 empleados. Su infraestructura de red será más sencilla que la de Málaga y Madrid, pero seguirá proporcionando los servicios corporativos y la conectividad necesarios.

### Departamentos

| Departamento | Empleados |
|---|---:|
| Administración | 5 |
| Ventas | 20 |
| Operaciones | 10 |
| IT / Soporte | 5 |
| **Total** | **40** |

La sucursal de Sevilla contará con:

- Ordenadores y portátiles de empleados
- Impresoras de red
- Teléfonos IP
- Puntos de acceso inalámbricos
- WiFi corporativo
- Switches
- Router

---

## 6. Requisitos de Red

La red de NexaCorp debe proporcionar conectividad fiable y controlada entre usuarios, departamentos, servicios, sucursales e Internet.

Los principales requisitos de red son:

- Todos los usuarios corporativos deben disponer de acceso a Internet.
- Los dispositivos deben recibir automáticamente la configuración de red correspondiente siempre que sea posible.
- Los diferentes departamentos deben estar separados lógicamente entre sí.
- La comunicación entre los diferentes segmentos de red debe estar controlada.
- Málaga, Madrid y Sevilla deben poder comunicarse a través de la red corporativa.
- Los usuarios de las sucursales deben poder acceder a los servicios autorizados ubicados en la sede principal de Málaga.
- Los servidores internos deben estar separados de las redes de usuarios.
- Los servicios accesibles públicamente deben estar separados de la red corporativa interna.
- El WiFi corporativo y el WiFi para invitados deben funcionar como redes independientes.
- Los usuarios invitados deben disponer de acceso a Internet, pero no deben poder acceder a la red corporativa interna.
- Los teléfonos IP deben estar separados lógicamente de los dispositivos de usuario convencionales.
- Los dispositivos de red deben disponer de una red dedicada para su administración.
- Los administradores de IT deben poder administrar remotamente la infraestructura de red de forma segura.
- La red debe soportar servicios centralizados como DNS, DHCP, NTP, AAA y Syslog.
- La red debe estar diseñada para permitir la incorporación futura de nuevos usuarios, departamentos, dispositivos y sucursales.

---

## 7. Requisitos de Seguridad

La red de NexaCorp debe proteger los recursos internos y restringir el acceso en función del tipo de usuario, dispositivo y segmento de red.

Los principales requisitos de seguridad son:

- Los usuarios invitados no deben poder acceder a ninguna red corporativa interna.
- Solo los usuarios y departamentos autorizados deben poder acceder a servicios internos sensibles.
- El departamento de IT debe disponer de acceso administrativo seguro a los dispositivos de red.
- El acceso de administración a routers y switches no debe estar disponible desde las redes de usuarios convencionales.
- Los dispositivos de red deben utilizar métodos seguros de administración remota.
- Las redes de usuarios, servidores, administración, telefonía e invitados deben permanecer separadas lógicamente.
- El acceso entre los diferentes segmentos de red debe seguir el principio de mínimo privilegio.
- Siempre que sea posible, se debe restringir la conexión de dispositivos no autorizados a los puertos de acceso.
- La red debe incluir protección frente a ataques comunes de Capa 2 y errores de configuración.
- Los servicios accesibles públicamente deben estar aislados de la red corporativa interna.
- Los eventos de red y la información relevante de seguridad deben registrarse de forma centralizada siempre que sea posible.

---

## 8. Requisitos de Escalabilidad y Disponibilidad

La red de NexaCorp debe estar diseñada para soportar el crecimiento futuro de la empresa y minimizar las interrupciones del servicio provocadas por fallos de red.

Los principales requisitos de escalabilidad y disponibilidad son:

- La red debe permitir añadir nuevos usuarios y dispositivos sin necesidad de realizar un rediseño completo.
- Debe ser sencillo integrar nuevos departamentos y segmentos de red.
- El esquema de direccionamiento IP debe reservar suficiente capacidad para el crecimiento futuro.
- En el futuro debe ser posible conectar nuevas sucursales a la red corporativa.
- La sede principal de Málaga debe evitar puntos únicos de fallo críticos siempre que sea posible.
- Las conexiones de red críticas deben disponer de redundancia.
- La red debe permanecer operativa cuando exista una ruta alternativa disponible tras el fallo de un enlace.
- Los dispositivos de red críticos deben utilizar diseños redundantes cuando sea necesario.
- La infraestructura de routing debe ser capaz de adaptarse a cambios en la topología de red.
- El diseño debe continuar siendo administrable a medida que la red crezca.

---

## 9. Objetivos Iniciales de la Red

A partir del escenario de la empresa y los requisitos definidos anteriormente, la red de NexaCorp será diseñada e implementada progresivamente.

Los principales objetivos del proyecto son:

- Diseñar una red empresarial estructurada y escalable.
- Crear un plan de direccionamiento IP eficiente para todas las sedes y segmentos de red.
- Segmentar la red según departamentos, servicios y tipos de dispositivos.
- Proporcionar comunicación controlada entre los diferentes segmentos de red.
- Establecer conectividad entre Málaga, Madrid y Sevilla.
- Proporcionar servicios de red centralizados para los usuarios corporativos.
- Proporcionar conectividad segura a Internet.
- Separar las redes internas, públicas, de invitados, telefonía, servidores y administración.
- Implementar una administración segura de la infraestructura de red.
- Introducir redundancia y alta disponibilidad para la infraestructura crítica.
- Implementar monitorización de red y registro centralizado de eventos.
- Aplicar mecanismos de seguridad en diferentes capas de la red.
- Probar y verificar cada tecnología implementada.
- Crear escenarios de resolución de problemas para comprender fallos comunes de red.
- Documentar todo el proceso de diseño, configuración, verificación y resolución de problemas.

La infraestructura será construida progresivamente en Cisco Packet Tracer. Cada etapa introducirá nuevos conceptos de redes únicamente después de haber estudiado y documentado las bases teóricas necesarias.