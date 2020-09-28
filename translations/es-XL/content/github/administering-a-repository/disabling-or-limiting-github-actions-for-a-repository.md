---
title: Inhabilitar o limitar las acciones de GitHub para un repositorio
intro: 'Los dueños de repositorios pueden inhabilitar, habilitar y limitar {{ site.data.variables.product.prodname_actions }} para un repositorio específico.'
versions:
  free-pro-team: '*'
  enterprise-server: '>=2.22'
---

{{ site.data.reusables.actions.enterprise-beta }}
{{ site.data.reusables.actions.enterprise-github-hosted-runners }}

### Acerca de los permisos de {{ site.data.variables.product.prodname_actions }} para tu repositorio

{{ site.data.reusables.github-actions.disabling-github-actions }}Para obtener más información acerca de {{ site.data.variables.product.prodname_actions }}, consulta la sección "[Acerca de {{ site.data.variables.product.prodname_actions }}](/actions/getting-started-with-github-actions/about-github-actions)".

Puedes habilitar {{ site.data.variables.product.prodname_actions }} para tu repositorio. {{ site.data.reusables.github-actions.enabled-actions-description }} Puedes inhabilitar {{ site.data.variables.product.prodname_actions }} totalmente para tu repositorio. {{ site.data.reusables.github-actions.disabled-actions-description }}

De manera alterna, puedes habilitar {{ site.data.variables.product.prodname_actions }} en tu repositorio, pero limitar las acciones que un flujo de trabajo puede ejecutar. {{ site.data.reusables.github-actions.enabled-local-github-actions }}

### Administrar los permisos de {{ site.data.variables.product.prodname_actions }} para tu repositorio

{% note %}

**Nota:** Tal vez no pueds administrar estas configuraciones si tu organización tiene una política de anulación o si la administra una cuenta empresarial que tiene dicha configuración. Para obtener más información, consulta la sección "[Inhabilitar o limitar las {{ site.data.variables.product.prodname_actions }} para tu organización](/github/setting-up-and-managing-organizations-and-teams/disabling-or-limiting-github-actions-for-your-organization)" o la sección "[Requerir las políticas de {{ site.data.variables.product.prodname_actions }} en tu cuenta empresarial](/github/setting-up-and-managing-your-enterprise-account/enforcing-github-actions-policies-in-your-enterprise-account)".

{% endnote %}

{{ site.data.reusables.repositories.navigate-to-repo }}
{{ site.data.reusables.repositories.sidebar-settings }}
{{ site.data.reusables.repositories.settings-sidebar-actions }}
4. Selecciona una opción debajo de "Permisos de las acciones". ![Habilita, inhabilita o limita las acciones para este repositorio](/assets/images/help/repository/enable-repo-actions.png)

{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.22" %}
### Habilitar flujos de trabajo para las bifurcaciones de repositorios privados

{{ site.data.reusables.github-actions.private-repository-forks-overview }}

#### Configurar la política de bifurcaciones privadas para un repositorio

{{ site.data.reusables.repositories.navigate-to-repo }}
{{ site.data.reusables.repositories.sidebar-settings }}
{{ site.data.reusables.repositories.settings-sidebar-actions }}
{{ site.data.reusables.github-actions.private-repository-forks-configure }}
{% endif %}