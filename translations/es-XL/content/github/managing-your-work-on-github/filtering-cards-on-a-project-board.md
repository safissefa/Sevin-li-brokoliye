---
title: Filtrar tarjetas en un tablero de proyecto
intro: Puedes filtrar las tarjetas en un tablero de proyecto para buscar tarjetas específicas o ver un subconjunto de tarjetas.
redirect_from:
  - /articles/filtering-cards-on-a-project-board
versions:
  free-pro-team: '*'
  enterprise-server: '*'
  github-ae: '*'
topics:
  - Pull requests
---

En una tarjeta, puedes hacer clic en cualquier asignatario {% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.17" %}, hito,{% endif %} o etiqueta para filtrar el tablero de proyecto en función de ese calificador. Para borrar la búsqueda, puedes hacer clic otra vez en el mismo asignatario {% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.17" %}, hito,{% endif %} o etiqueta.

También puedes usar la barra de búsqueda "Filtrar tarjetas" en la parte superior de cada tablero de proyecto para buscar tarjetas. Puedes filtrar tarjetas usando los siguientes calificadores de búsqueda en cualquier combinación, o simplemente escribir el texto que deseas buscar.

- Filtrar tarjetas por autor usando `author:USERNAME`
- Filtrar tarjetas por asignatario usando `assignee:USERNAME` o `no:assignee`
- Filtrar tarjetas por etiqueta usando `label:LABEL`, `label:"MULTI-WORD LABEL NAME"` o `no:label`{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.17" %}
- Filtrar por hito usando `milestone:MY-MILESTONE`{% endif %}
- Filtrar tarjetas por estado usando `state:open`, `state:closed` o `state:merged`
- Filtrar por estado de revisión usando `review:none`, `review:required`, `review:approved`, o `review:changes_requested`
- Filtrar por comprobación de estado usando `status:pending`, `status:success` o `status:failure`
- Filtrar tarjetas por tipo usando `type:issue`, `type:pr` o `type:note`
- Filtrar tarjetas por estado y tipo usando `is:open`, `is:closed` o `is:merged` y `is:issue`, `is:pr` o `is:note`
- Filtrar tarjetas por informes de problemas que se enlazan con alguna solicitud de extracción mediante una referencia de cierre utilizando `linked:pr`{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.20" %}
- Filtrar tarjetas por repositorio en un tablero de proyecto de toda la organización utilizando `repo:ORGANIZATION/REPOSITORY`{% endif %}

1. Dirígete al tablero de proyecto que contenga las tarjetas que desees filtrar.
2. Sobre las columnas de las tarjetas del proyecto, haz clic en la barra de búsqueda "Filtrar tarjetas" y escribe la consulta de búsqueda para filtrar las tarjetas. ![Barra de búsqueda Filtrar tarjetas](/assets/images/help/projects/filter-card-search-bar.png)

{% tip %}

**Sugerencia:** Puedes arrastrar y soltar las tarjetas filtradas o usar los atajos del teclado para moverlas entre las columnas. {% data reusables.project-management.for-more-info-project-keyboard-shortcuts %}

{% endtip %}

### Leer más

- "[Acerca de los tablero de proyecto](/articles/about-project-boards)"
- "[Agregar propuestas y solicitudes de extracción a un tablero de proyecto](/articles/adding-issues-and-pull-requests-to-a-project-board)"
- "[Agregar notas a un tablero de proyecto](/articles/adding-notes-to-a-project-board)"
