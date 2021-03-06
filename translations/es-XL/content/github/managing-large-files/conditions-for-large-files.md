---
title: Condiciones para archivos de gran tamaño
intro: '{% data variables.product.product_name %} limita el tamaño permitido para los archivos de los repositorios y bloqueará una subida de información si estos superan el tamaño máximo.'
redirect_from:
  - /articles/conditions-for-large-files
versions:
  free-pro-team: '*'
  enterprise-server: '*'
  github-ae: '*'
---

{% data reusables.large_files.use_lfs_tip %}

### Advertencia para archivos mayores a {% data variables.large_files.warning_size %}

Recibirás una advertencia de Git si intentas añadir o actualizar un archivo mayor a {% data variables.large_files.warning_size %}. Los cambios aún se subirán a tu repositorio, pero puedes considerar eliminar la confirmación para minimizar el impacto en el rendimiento. Para obtener más información, consulta la sección "[Eliminar archivos del historial de un repositorio](/github/managing-large-files/removing-files-from-a-repositorys-history)".

### Subidas bloquadas para archivos grandes

{% if currentVersion != "free-pro-team@latest" %}Predeterminadamente, {% endif %}{% data variables.product.product_name %} bloquea las subidas que excedan {% data variables.large_files.max_github_size %}. {% if currentVersion != "free-pro-team@latest" %}Sin embargo, los administradores de sitio pueden configurar un límite diferente para tu instancia de {% data variables.product.prodname_ghe_server %}. Para obtener más información, consulta la sección "[Configurar los límites de subida de Git](/enterprise/{{ currentVersion }}/admin/guides/installation/setting-git-push-limits)".{% endif %}
