Markdown
# Incident Response Report: Ransomware LockBit Black Analysis & Remediation

Este repositorio contiene el informe técnico de **Respuesta a Incidentes y Análisis de Ciberataque** frente a una infección por **Ransomware LockBit Black** en un entorno empresarial simulado.

El informe documenta la cronología de los hechos, las acciones de contención inmediatas, el proceso de notificación regulatoria y la formulación de un plan preventivo alineado con controles **ISO 27001**[cite: 2].

---

## Resumen del Ciberataque

* **Fecha/Hora de Detección:** 28/05/2025 – 01:27 AM[cite: 2].
* **Vector de Infección Inicial:** Ingeniería Social / Phishing. Un usuario interno ejecutó un archivo malicioso descargado de una fuente externa[cite: 2].
* **Mecanismo de Propagación:** Movimiento lateral acelerado a través de recursos compartidos en red local (`SMB/Carpeta Finanzas`), infectando estaciones de trabajo (Ingeniería, RRHH) y el Servidor Central[cite: 2].
* **Malware Confirmado:** *LockBit Black* (Validado mediante firmas de análisis de hash en VirusTotal / YARA Rules)[cite: 2].
* **Impacto Operativo:** Cifrado de archivos clave, despliegue de notas de rescate (`UvCSWEXBq.README.txt`), modificación de fondos de pantalla de los equipos e intervención de directivas del sistema mediante la consola Server Win32[cite: 2].

---

## Cronología de la Respuesta al Incidente

1. **01:27 AM:** Infección inicial por ejecución del binario y reporte inmediato del personal de turno al área de TI[cite: 2].
2. **01:28 AM - 01:30 AM:** Cifrado masivo de recursos en red e interrupción de la consola de comandos en el servidor[cite: 2].
3. **01:31 AM:** Aislamiento del segmento de red y **notificación oficial del ciberataque ante la Agencia Nacional de Ciberseguridad (ANCI)** vía portal `anci.gob.cl`[cite: 2].
4. **01:32 AM:** Evidenciación de la persistencia y nota de secuestro en los endpoints afectados[cite: 2].

---

## Plan Preventivo y Mejoras (Controles ISO 27001)

Como parte del proceso de aprendizaje continuo y mitigación de riesgos futuros, se estructuró un plan de acción basado en el Anexo A de la norma ISO 27001[cite: 2]:

| Control ISO 27001 | Medida de Remediación Implementada |
| :--- | :--- |
| **A.7.3 Concientización** | Capacitaciones periódicas sobre ingeniería social y campañas de Phishing Ético[cite: 1, 2]. |
| **A.8 Gestión de Activos** | Inventariado actualizado de activos críticos y asignación clara de propietarios[cite: 2]. |
| **A.9 Control de Acceso** | Reestructuración de privilegios bajo el principio de mínimos accesos y renovación masiva de credenciales[cite: 1, 2]. |
| **A.12.3 Copias de Seguridad** | Rediseño de la política de respaldo con copias en la nube y medios aislados cada 3 días[cite: 2]. |
| **A.12.6 Vulnerabilidades** | Bloqueo de ejecución de ejecutables externos, restricción de puertos USB y actualización de motores antivirus[cite: 1, 2]. |
| **A.16.1 Respuesta a Incidentes** | Formalización e integración del protocolo de escalamiento y notificación ante ciberataques[cite: 1, 2]. |

---

## Archivos del Repositorio

* `Informe_Incidente_Ransomware.pdf`: Documento completo con evidencia fotográfica del ciberataque, capturas de pantalla de análisis en VirusTotal, formulario de notificación a la ANCI y matriz de controles ISO 27001[cite: 2].

---

## Herramientas e Infraestructura Utilizadas

* **Triaje y Threat Intelligence:** VirusTotal, YARA Signatures, OSINT[cite: 2].
* **Plataforma Regulatoria:** Portal de Notificación ANCI (Chile)[cite: 2].
* **Framework Normativo:** ISO/IEC 27001 (A.8, A.11, A.12, A.13, A.16, A.17)[cite: 2].

---

## 👨‍💻 Autor

**Sebastián Paz**  
*Ciberseguridad y Gestión de Riesgos Informáticos*
