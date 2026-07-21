<h1 align="center">Blue Team · SOC & SIEM</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Elastic%20SIEM-005571?style=flat-square&logo=elasticsearch&logoColor=white" />
  <img src="https://img.shields.io/badge/Suricata%20IDS-EF7B20?style=flat-square" />
  <img src="https://img.shields.io/badge/pfSense-212121?style=flat-square" />
  <img src="https://img.shields.io/badge/Threat%20Hunting-3FB950?style=flat-square" />
  <img src="https://img.shields.io/badge/MITRE%20ATT%26CK-FF7B72?style=flat-square" />
</p>

---

## Sobre este módulo

Defensa activa desde la perspectiva de un **SOC (Security Operations Center)**: monitorización, detección, correlación de eventos y respuesta ante incidentes. El foco está en **ver** lo que pasa en la red y los endpoints, y **actuar** antes de que un incidente se convierta en una brecha.

**Temas cubiertos:** SOC/CSIRT/CERT · SIEM (ELK Stack, Splunk) · IOCs e IoAs · Cyber Kill Chain · Pirámide del Dolor · threat hunting · IDS/IPS (Suricata) · honeypots · hardening · Zero Trust · marcos NIST/ISO.

---

## Concepto clave — Pirámide del Dolor

La estrategia de detección no es toda igual. La **Pirámide del Dolor** (David Bianco) ordena los indicadores según cuánto le cuesta al atacante cambiarlos: detectar un hash es trivial de evadir, pero detectar **comportamiento (TTPs)** obliga al adversario a reinventar su forma de operar.

![Pirámide del Dolor](piramide-del-dolor.png)

> La conclusión operativa: invertir en detectar comportamiento rinde mucho más que perseguir hashes e IPs.

---

## Práctica — Laboratorio SIEM

Montaje de un entorno defensivo completo de extremo a extremo:

- **Perímetro** con pfSense (firewall, segmentación de red).
- **Detección de red** con Suricata (IDS/IPS) generando eventos EVE en JSON.
- **SIEM** con Elastic Stack: ingesta de logs, Fleet Server para gestión de agentes, y dashboards de detección en Kibana.
- **Endpoints** enrolados (Windows y Linux) reportando telemetría.
- **Honeypot** integrado para atraer y estudiar actividad maliciosa.

El objetivo: recolectar telemetría de múltiples fuentes en un punto central, correlacionarla y generar alertas accionables.

---

## Stack

`Elastic Stack (Elasticsearch · Kibana · Fleet)` · `Suricata` · `pfSense` · `Sysmon` · `Wireshark` · `Honeypot` · `KQL`

---

## Proyecto relacionado

Este módulo es la base del proyecto capstone **[Nullsec](https://github.com/juanmalbran/nullsec-siem-elk)**, donde llevé el SIEM a producción con Threat Intelligence (MISP) y detección real de ransomware.

---

<div align="center">
  <sub>Parte del portfolio de <a href="https://github.com/juanmalbran">Juan Malbrán · M4LBYTE</a></sub>
</div>
