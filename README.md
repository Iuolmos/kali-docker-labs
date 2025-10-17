# Kali + Docker Labs — Laboratorio de Hacking Ético

Este repositorio explica cómo montar un laboratorio local para prácticas de **hacking ético** usando:
- Una **máquina virtual Kali Linux** como estación atacante.
- **Docker / Docker Compose** para crear laboratorios reproducibles, aislados y fáciles de resetear.

> ⚠️ Este repositorio es solo para uso ético y educativo. Solo realiza pruebas en entornos que posees o donde tienes permiso explícito.

## Contenidos
- `docs/` — guías: instalación de Kali en VM, Docker, y buenas prácticas de seguridad.
- `lab-examples/` — ejemplos de labs con `docker-compose`.
- `scripts/` — scripts para instalar Docker y construir imágenes.

## Requisitos previos
- Host con soporte de virtualización (VT-x/AMD-V).
- VirtualBox o VMware para importar la VM de Kali. Puedes descargar imágenes oficiales de Kali en el sitio oficial. :contentReference[oaicite:1]{index=1}
- Docker Engine (o Docker Desktop) instalado en el host o en una VM separada. Consulta la guía oficial de Docker para tu SO. :contentReference[oaicite:2]{index=2}

## Quickstart (resumen)
1. Descargar e importar la VM oficial de Kali (VirtualBox/VMware). :contentReference[oaicite:3]{index=3}  
2. Iniciar Kali, actualizar `apt` y herramientas básicas (`sudo apt update && sudo apt full-upgrade`).  
3. En tu host o en otra VM, instalar Docker usando el script `scripts/install-docker-ubuntu.sh`. :contentReference[oaicite:4]{index=4}  
4. Entrar a `lab-examples/docker-lab-1/` y ejecutar `docker compose up -d`.  
5. Seguir `lab-examples/*/README.md` para cada ejercicio (objetivos, métricas, limpieza).

## Seguridad y aislamiento
- Usa redes Docker custom (uno por lab) o máquinas virtuales de laboratorio separadas para evitar fugas a la red local.  
- Mantén imágenes actualizadas y escanéalas por vulnerabilidades (ej.: Trivy).  
- Nunca publiques datos sensibles, credenciales o resultados de pruebas. :contentReference[oaicite:5]{index=5}

## Contribuciones
Pull requests con nuevos labs, ejercicios y correcciones son bienvenidos. Usa la rama `main` protegida y un `PR` por funcionalidad.
