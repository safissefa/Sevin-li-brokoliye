---
title: シークレットスキャンからのアラートを管理する
intro: リポジトリにチェックインしたシークレットのアラートを表示したりクローズしたりすることができます。
product: '{% data reusables.gated-features.secret-scanning %}'
redirect_from:
  - /github/administering-a-repository/managing-alerts-from-secret-scanning
versions:
  free-pro-team: '*'
  enterprise-server: '>=3.0'
  github-ae: '*'
topics:
  - Repositories
---

{% data reusables.secret-scanning.beta %}

### アラートを管理する

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-security %}
3. In the left sidebar, click **Secret scanning alerts**.
   {% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.22" %}
   !["Secret scanning alerts" tab](/assets/images/help/repository/sidebar-secrets.png)
   {% endif %}
   {% if currentVersion == "github-ae@latest" %}
   !["Secret scanning alerts" tab](/assets/images/enterprise/github-ae/repository/sidebar-secrets-ghae.png)
   {% endif %}
4. [Secret scanning] の下で、表示するアラートをクリックします。
   {% if currentVersion == "free-pro-team@latest" %}
   ![シークレットスキャンからのアラートのリスト](/assets/images/help/repository/secret-scanning-click-alert.png)
   {% endif %}
   {% if currentVersion ver_gt "enterprise-server@2.22" %}
   ![シークレットスキャンからのアラートのリスト](/assets/images/help/repository/secret-scanning-click-alert-ghe.png)
   {% endif %}
   {% if currentVersion == "github-ae@latest" %}
   ![シークレットスキャンからのアラートのリスト](/assets/images/enterprise/github-ae/repository/secret-scanning-click-alert-ghae.png)
   {% endif %}
5. Optionally, use the "Mark as" drop-down menu and click a reason for resolving an alert.
   {% if currentVersion == "free-pro-team@latest" %}
   ![シークレットスキャンからのアラートを解決するためのドロップダウンメニュー](/assets/images/help/repository/secret-scanning-resolve-alert.png)
   {% endif %}
   {% if currentVersion ver_gt "enterprise-server@2.22" or currentVersion == "github-ae@latest" %}
   ![シークレットスキャンからのアラートを解決するためのドロップダウンメニュー](/assets/images/help/repository/secret-scanning-resolve-alert-ghe.png)
   {% endif %}

### 侵害されたシークレットを保護する

シークレットがリポジトリにコミットされたら、シークレットが侵害されたと考える必要があります。 {% data variables.product.prodname_dotcom %} は、侵害されたシークレットに対して次のアクションを行うことをおすすめします。

- 侵害された {% data variables.product.prodname_dotcom %} の個人アクセストークンについては、侵害されたトークンを削除し、新しいトークンを作成し、古いトークンを使っていたサービスを更新してください。 詳しい情報については[コマンドラインのための個人のアクセストークンの作成](/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)を参照してください。
- それ以外のすべてのシークレットについては、最初に {% data variables.product.product_name %} にコミットされたシークレットが有効であることを確認してください。 有効である場合は、新しいシークレットを作成し、古いシークレットを使用するサービスを更新してから、古いシークレットを削除します。
