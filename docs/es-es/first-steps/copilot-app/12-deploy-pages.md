---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de cambios y comprobar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz para que cualquiera pueda probarlo. Copilot puede preparar el flujo de trabajo y guiarte durante la implementación, pero debes revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pide a Copilot que configure una implementación en GitHub Pages.
- revisa el flujo de trabajo y la solicitud de cambios antes de combinarla.
- sigue la implementación y comprueba que el sitio publicado funciona.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero la gente aún necesita una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible desde una URL pública sin añadir un servidor ni dependencias de ejecución.

## Pide a Copilot que implemente el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de tres etapas: una solicitud de cambios de space-quiz combinada; una ejecución correcta de GitHub Actions llamada Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz en directo en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y combine una solicitud de cambios, y que modifique la configuración de Pages del repositorio. Revisa las diferencias, los permisos de implementación y cualquier solicitud de aprobación de GitHub antes de continuar.

## Revisa el flujo de trabajo y comprueba la implementación

1. Confirma que el archivo README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios de la solicitud de cambios, incluidos los pasos de compilación e implementación del flujo de trabajo.
3. Combina los cambios solo después de que se superen las comprobaciones requeridas de la solicitud de cambios.
4. Sigue la ejecución de implementación de GitHub Actions hasta que finalice correctamente.
5. Abre la URL indicada y confirma que se carga Space Quiz.

Si el agente no puede habilitar Pages o combinar la solicitud de cambios, sigue las instrucciones específicas que te proporcione. No des la tarea por completada hasta que la implementación haya finalizado correctamente y el sitio esté disponible.

## Resumen y próximos pasos

Space Quiz ya está disponible como sitio web y has comprobado la implementación en lugar de confiar únicamente en el informe del agente. Continúa con la [Lección 13: Repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
