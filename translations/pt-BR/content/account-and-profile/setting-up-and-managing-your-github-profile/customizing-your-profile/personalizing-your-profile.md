---
title: Personalizar seu perfil
intro: 'É possível compartilhar informações sobre você mesmo com outros usuários do {% data variables.product.product_name %} definindo uma imagem e adicionando uma bio ao seu perfil.'
redirect_from:
  - /articles/adding-a-bio-to-your-profile
  - /articles/setting-your-profile-picture
  - /articles/how-do-i-set-up-my-profile-picture
  - /articles/gravatar-problems
  - /articles/how-do-i-set-up-my-avatar
  - /articles/personalizing-your-profile
  - /github/setting-up-and-managing-your-github-profile/personalizing-your-profile
  - /github/setting-up-and-managing-your-github-profile/customizing-your-profile/personalizing-your-profile
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Profiles
shortTitle: Personalizar
---

## Alterar sua imagem de perfil

Sua imagem de perfil ajuda a identificá-lo no {% data variables.product.product_name %} em pull requests, comentários, páginas de contribuições e gráficos.

Ao se inscrever em uma conta, o {% data variables.product.product_name %} fornece a você uma "identicon" gerada aleatoriamente. [Sua identicon](https://github.com/blog/1586-identicons) é gerada a partir de um hash de seu ID de usuário e não há como controlar suas cores ou padrão. É possível substituir sua identicon por uma imagem que represente você.

{% note %}

**Observação{% ifversion ghec %}s{% endif %}**: {% ifversion ghec %}

* {% endif %}Sua foto de perfil deve ser um arquivo PNG, JPG ou GIF, e deve ter um tamanho inferior a 1 MB de tamanho e menor que 3000 por 3000 pixels. Para melhor qualidade de renderização, recomendamos uma imagem de aproximadamente 500 por 500 pixels.
{% ifversion ghec %}* As imagens de perfil do Gravatar não são compatíveis com {% data variables.product.prodname_emus %}.{% endif %}

{% endnote %}

### Definir uma imagem de perfil

{% data reusables.user-settings.access_settings %}
2. Em **Profile Picture** (Imagem de perfil), clique em {% octicon "pencil" aria-label="The edit icon" %} **Edit** (Editar). ![Editar imagem de perfil](/assets/images/help/profile/edit-profile-photo.png)
3. Clique em **Fazer o upload de uma foto...**.{% ifversion not ghae %} ![Update profile picture](/assets/images/help/profile/edit-profile-picture-options.png){% endif %}
3. Recorte sua imagem. Quando terminar, clique em **Set new profile picture** (Definir nova imagem de perfil). ![Cortar foto carregada](/assets/images/help/profile/avatar_crop_and_save.png)

### Redefinir sua imagem de perfil para a identicon

{% data reusables.user-settings.access_settings %}
2. Em **Profile Picture** (Imagem de perfil), clique em {% octicon "pencil" aria-label="The edit icon" %} **Edit** (Editar). ![Editar imagem de perfil](/assets/images/help/profile/edit-profile-photo.png)
3. Para reverter para sua identicon, clique em **Remove photo** (Remover foto). {% ifversion not ghae %}}Se o seu endereço de e-mail estiver associado a um [Gravatar](https://en.gravatar.com/), você não poderá reverter para o seu identicon. Em vez disso, clique em **Revert to Gravatar** (Reverter para Gravatar). ![Update profile picture](/assets/images/help/profile/edit-profile-picture-options.png){% endif %}

## Alterar seu nome de perfil

Você pode alterar o nome que é exbido em seu perfil. Este nome também pode ser exibido ao lado dos comentários que você fizer em repositórios privados pertencentes a uma organização. Para obter mais informações, consulte "[Gerenciar a exibição de nomes de integrantes na organização](/articles/managing-the-display-of-member-names-in-your-organization)".

{% ifversion fpt or ghec %}
{% note %}

**Observação:** Se você for integrante de um {% data variables.product.prodname_emu_enterprise %}, todas as alterações no nome do seu perfil devem ser feitas por meio do seu provedor de identidade ao invés de {% data variables.product.prodname_dotcom_the_website %}. {% data reusables.enterprise-accounts.emu-more-info-account %}

{% endnote %}
{% endif %}

{% data reusables.user-settings.access_settings %}
2. Em "Name" (Nome), digite o nome que deseja exibir em seu perfil. ![Campo nome em configurações de perfil](/assets/images/help/profile/name-field.png)

## Adicionar uma bio ao seu perfil

Adicione uma bio em seu perfil para compartilhar informações sobre si mesmo com outros usuários {% data variables.product.product_name %}. Com a ajuda de [@menções](/articles/basic-writing-and-formatting-syntax) e emojis, você pode incluir informações sobre onde está trabalhando agora ou já trabalhou, que tipo de trabalho faz ou mesmo que tipo de café toma.

{% ifversion fpt or ghes or ghec %}

Para um formulário mais longo e uma maneira mais proeminente de exibir informações personalizadas sobre você, também é possível usar um README do perfil. Para obter mais informações, consulte "[Gerenciar seu perfil README](/github/setting-up-and-managing-your-github-profile/managing-your-profile-readme)."

{% endif %}

{% note %}

**Observação:** Se a seção de visão geral de atividade está habilitada em seu perfil e na bio você faz @menção a uma organização da qual é integrante, a organização será a primeira apresentada na visão geral de atividade. Para obter mais informações, consulte "[Mostrar uma visão geral da sua atividade no seu perfil](/articles/showing-an-overview-of-your-activity-on-your-profile)".

{% endnote %}

{% data reusables.user-settings.access_settings %}
2. Em **Bio**, adicione o conteúdo que deseja exibir em seu perfil. O campo bio é limitado a 160 caracteres. ![Atualizar a bio no perfil](/assets/images/help/profile/bio-field.png)

  {% tip %}

  **Dica:** Ao fazer @menção a uma organização, somente aquelas das quais você é integrante serão preenchidas automaticamente. Você ainda pode fazer @menção a organizações das quais não é integrante, como um empregador anterior, mas o nome da organização não será preenchido automaticamente.

  {% endtip %}

3. Clique em **Update profile** (Atualizar perfil). ![Botão Update profile (Atualizar perfil)](/assets/images/help/profile/update-profile-button.png)

## Definir um status

Você pode definir um status para exibir informações sobre sua disponibilidade atual no {% data variables.product.product_name %}. Seu status será mostrado:
- em sua página de perfil do {% data variables.product.product_name %}.
- quando as pessoas passarem o mouse em cima de seu nome de usuário ou avatar no {% data variables.product.product_name %}.
- em uma página de equipe da qual você é integrante. Para obter mais informações, consulte "[Sobre equipes](/articles/about-teams/#team-pages)".
- no painel da organização da qual você é integrante. Para obter mais informações, consulte "[Sobre o painel de sua organização](/articles/about-your-organization-dashboard/)".

Ao definir o seu status, você também pode informar às pessoas que sua disponibilidade é limitada no {% data variables.product.product_name %}.

![Usuário mencionado apresenta "busy" (ocupado) ao lado do nome de usuário](/assets/images/help/profile/username-with-limited-availability-text.png)

![Revisor solicitado apresenta "busy" (ocupado) ao lado do nome de usuário](/assets/images/help/profile/request-a-review-limited-availability-status.png)

Se você selecionar a opção "Busy" (Ocupado), quando as pessoas fizerem @menção ao seu nome de usuário, atribuírem um problema ou pull request a você ou solicitarem a você uma revisão de pull request, uma observação ao lado do seu nome mostrará que você está ocupado. Você também será excluído da atribuição automática de revisão para os pull requests atribuídos a qualquer equipe a que você pertença. Para obter mais informações, consulte "[Gerenciando as configurações de revisão de código para a sua equipe](/organizations/organizing-members-into-teams/managing-code-review-settings-for-your-team)."

1. No canto superior direito de {% ifversion fpt or ghec %}{% data variables.product.prodname_dotcom_the_website %}{% else %}{% data variables.product.product_name %}{% endif %}, clique na sua foto de perfil e, em seguida clique em **Definir seu status** ou, se você já tiver um status definido, clique em seu status atual. ![Botão no perfil para definir seu status](/assets/images/help/profile/set-status-on-profile.png)
2. Para adicionar um texto personalizado ao seu status, clique no campo de texto e digite uma mensagem. ![Campo para digitar mensagem de status](/assets/images/help/profile/type-a-status-message.png)
3. Opcionalmente, para definir um status com emoji, clique no ícone de carinhas e selecione um emoji da lista.![Botão para selecionar status com emoji](/assets/images/help/profile/select-emoji-status.png)
4. Como opção, se você deseja compartilhar que tem disponibilidade limitada, selecione "Busy" (Ocupado). ![Opção Busy (Ocupado) marcado nas opções Edit status (Editar status)](/assets/images/help/profile/limited-availability-status.png)
5. Use o menu suspenso **Clear status** (Limpar status) e selecione quando deseja que seu status expire. Caso não selecione um prazo de validade, o status será mantido até que você o limpe ou o edite. ![Menu suspenso para escolher quando o status expira](/assets/images/help/profile/status-expiration.png)
6. Use o menu suspenso e clique na organização para a qual você deseja que seu status esteja visível. Se não selecionar uma organização, seu status será público. ![Menu suspenso para escolher para quem seu status é visível](/assets/images/help/profile/status-visibility.png)
7. Clique em **Set status** (Definir status). ![Botão para definir o status](/assets/images/help/profile/set-status-button.png)

{% ifversion fpt or ghec %}
## Exibir selos no seu perfil

Ao participar de determinados programas, {% data variables.product.prodname_dotcom %} exibe automaticamente um selo no seu perfil.

| Selo                                                            | Programa                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| --------------------------------------------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| {% octicon "cpu" aria-label="The Developer Program icon" %}     | **Membro do programa de desenvolvedores**                                  | Se você for um integrante registrado do Programa de Desenvolvedor de {% data variables.product.prodname_dotcom %}, ao criar um aplicativo com a API de {% ifversion fpt or ghec %}{% data variables.product.prodname_dotcom %}{% else %}{% data variables.product.product_name %}{% endif %}, você receberá um selo de integrante do Programa no seu perfil. Para obter mais informações sobre o Programa de Desenvolvedores de {% data variables.product.prodname_dotcom %}, consulte o [Desenvolvedor do GitHub](/program/).                              |
| {% octicon "star-fill" aria-label="The star icon" %}            | **Pro**                                                                    | Se você usar {% data variables.product.prodname_pro %}, você receberá um selo PRO no seu perfil. Para obter mais informações sobre o {% data variables.product.prodname_pro %}, consulte "[Produtos do {% data variables.product.prodname_dotcom %}](/github/getting-started-with-github/githubs-products#github-pro)".                                                                                                                                                                                                                                       |
| {% octicon "lock" aria-label="The lock icon" %}                 | **Security Bug Bounty Hunter**                                             | Se você ajudou a identificar vulnerabilidades de segurança, o seu perfil receberá um selo Security Bug Bounty Hunter. Para obter mais informações sobre o programa de segurança {% data variables.product.prodname_dotcom %}, consulte [{% data variables.product.prodname_dotcom %} Segurança.](https://bounty.github.com/).                                                                                                                                                                                                                                   |
| {% octicon "mortar-board" aria-label="The mortar-board icon" %} | **Especialista de campus de {% data variables.product.prodname_dotcom %}** | Se você participar do {% data variables.product.prodname_campus_program %}, você receberá um selo do especialista de campus de {% data variables.product.prodname_dotcom %} no seu perfil. Para obter mais informações sobre o programa de Especialistas de Campus, consulte [Especialistas de campus](https://education.github.com/experts).                                                                                                                                                                                                                 |
| {% octicon "shield" aria-label="The shield icon" %}             | **Crédito da consultoria de segurança**                                    | Se uma assessoria de segurança que você enviar ao [Banco de dados da consultoria de{% data variables.product.prodname_dotcom %}](https://github.com/advisories) for aceita, você receberá um crachá de crédito da consultoria de segurança no seu perfil. Para obter mais informações sobre as consultorias de segurança de {% data variables.product.prodname_dotcom %}, consulte [Consultorias de segurança de{% data variables.product.prodname_dotcom %}](/code-security/repository-security-advisories/about-github-security-advisories-for-repositories). |
| {% octicon "check" aria-label="The check icon" %}               | **Discussão respondida**                                                   | Se sua resposta a uma discussão for marcada como a resposta, você receberá um selo respondido por Discussão no seu perfil. Para obter mais informações sobre as Discussões de {% data variables.product.prodname_dotcom %}, consulte [Sobre discussões](/discussions/collaborating-with-your-community-using-discussions/about-discussions).                                                                                                                                                                                                                    |

{% endif %}

{% ifversion fpt or ghec %}

## Ganhando conquistas

As conquistas comemoram eventos e ações específicos que acontecem em {% data variables.product.prodname_dotcom %}. Eles aparecerão como pequenos selos listados na barra lateral do seu perfil. Clicar ou passar o sobre uma conquista mostrará uma visão detalhada que indica como a conquista foi realizada com uma breve descrição e links para os eventos contribuintes. Os links do evento só serão visíveis para os usuários que têm acesso ao repositório ou organização em que o evento ocorreu. Os links de eventos parecerão inacessíveis para todos os usuários sem acesso.

Para parar contribuições privadas de contar para suas conquistas ou para desabilitar completamente as Conquistas, consulte "[Mostrando suas contribuições privadas e Conquistas no seu perfil](/articles/publicizing-or-hiding-your-private-contributions-on-your-profile)".

{% note %}

**Observação**: Este recurso está atualmente na versão beta e está sujeito a alterações.

{% endnote %}

{% endif %}

## Lista de repositórios qualificados para a conquista de contribuidor Helicóptero de Marte de 2020

Se você criou qualquer commit presente no histórico de commit da tag listada em um ou mais dos repositórios abaixo, você receberá a conquista do Contribuidor de Marte do Helicóptero 2020 no seu perfil. O commit da autoria tem que estar com um endereço de e-mail verificado associado à sua conta no momento em que {% data variables.product.prodname_dotcom %} determinou as contribuições elegíveis, para ser atribuído a você. Você pode ser o autor original ou [um dos coautores](/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors) do commit. As alterações futuras em e-mails verificados não terão efeito no selo. Criamos a lista com base nas informações recebidas do Laboratório de Propulsão de Jato da NASA.

| {% data variables.product.prodname_dotcom %} Repositório                      | Versão    | Tag                                                                                                        |
| ----------------------------------------------------------------------------- | --------- | ---------------------------------------------------------------------------------------------------------- |
| [torvalds/linux](https://github.com/torvalds/linux)                           | 3.4       | [v3.4](https://github.com/torvalds/linux/releases/tag/v3.4)                                                |
| [python/cpython](https://github.com/python/cpython)                           | 3.9.2     | [v3.9.2](https://github.com/python/cpython/releases/tag/v3.9.2)                                            |
| [boto/boto3](https://github.com/boto/boto3)                                   | 1.17.17   | [1.17.17](https://github.com/boto/boto3/releases/tag/1.17.17)                                              |
| [boto/botocore](https://github.com/boto/botocore)                             | 1.20.11   | [1.20.11](https://github.com/boto/botocore/releases/tag/1.20.11)                                           |
| [certifi/python-certifi](https://github.com/certifi/python-certifi)           | 2020.12.5 | [2020.12.05](https://github.com/certifi/python-certifi/releases/tag/2020.12.05)                            |
| [chardet/chardet](https://github.com/chardet/chardet)                         | 4.0.0     | [4.0.0](https://github.com/chardet/chardet/releases/tag/4.0.0)                                             |
| [matplotlib/cycler](https://github.com/matplotlib/cycler)                     | 0.10.0    | [v0.10.0](https://github.com/matplotlib/cycler/releases/tag/v0.10.0)                                       |
| [elastic/elasticsearch-py](https://github.com/elastic/elasticsearch-py)       | 6.8.1     | [6.8.1](https://github.com/elastic/elasticsearch-py/releases/tag/6.8.1)                                    |
| [ianare/exif-py](https://github.com/ianare/exif-py)                           | 2.3.2     | [2.3.2](https://github.com/ianare/exif-py/releases/tag/2.3.2)                                              |
| [kjd/idna](https://github.com/kjd/idna)                                       | 2.10      | [v2.10](https://github.com/kjd/idna/releases/tag/v2.10)                                                    |
| [jmespath/jmespath.py](https://github.com/jmespath/jmespath.py)               | 0.10.0    | [0.10.0](https://github.com/jmespath/jmespath.py/releases/tag/0.10.0)                                      |
| [nucleic/kiwi](https://github.com/nucleic/kiwi)                               | 1.3.1     | [1.3.1](https://github.com/nucleic/kiwi/releases/tag/1.3.1)                                                |
| [matplotlib/matplotlib](https://github.com/matplotlib/matplotlib)             | 3.3.4     | [v3.3.4](https://github.com/matplotlib/matplotlib/releases/tag/v3.3.4)                                     |
| [numpy/numpy](https://github.com/numpy/numpy)                                 | 1.20.1    | [v1.20.1](https://github.com/numpy/numpy/releases/tag/v1.20.1)                                             |
| [opencv/opencv-python](https://github.com/opencv/opencv-python)               | 4.5.1.48  | [48](https://github.com/opencv/opencv-python/releases/tag/48)                                              |
| [python-pillow/Pillow](https://github.com/python-pillow/Pillow)               | 8.1.0     | [8.1.0](https://github.com/python-pillow/Pillow/releases/tag/8.1.0)                                        |
| [pycurl/pycurl](https://github.com/pycurl/pycurl)                             | 7.43.0.6  | [REL_7_43_0_6](https://github.com/pycurl/pycurl/releases/tag/REL_7_43_0_6)                             |
| [pyparsing/pyparsing](https://github.com/pyparsing/pyparsing)                 | 2.4.7     | [pyparsing_2.4.7](https://github.com/pyparsing/pyparsing/releases/tag/pyparsing_2.4.7)                     |
| [pyserial/pyserial](https://github.com/pyserial/pyserial)                     | 3.5       | [v3.5](https://github.com/pyserial/pyserial/releases/tag/v3.5)                                             |
| [dateutil/dateutil](https://github.com/dateutil/dateutil)                     | 2.8.1     | [2.8.1](https://github.com/dateutil/dateutil/releases/tag/2.8.1)                                           |
| [yaml/pyyaml ](https://github.com/yaml/pyyaml)                                | 5.4.1     | [5.4.1](https://github.com/yaml/pyyaml/releases/tag/5.4.1)                                                 |
| [psf/requests](https://github.com/psf/requests)                               | 2.25.1    | [v2.25.1](https://github.com/psf/requests/releases/tag/v2.25.1)                                            |
| [boto/s3transfer](https://github.com/boto/s3transfer)                         | 0.3.4     | [0.3.4](https://github.com/boto/s3transfer/releases/tag/0.3.4)                                             |
| [enthought/scimath](https://github.com/enthought/scimath)                     | 4.2.0     | [4.2.0](https://github.com/enthought/scimath/releases/tag/4.2.0)                                           |
| [scipy/scipy](https://github.com/scipy/scipy)                                 | 1.6.1     | [v1.6.1](https://github.com/scipy/scipy/releases/tag/v1.6.1)                                               |
| [benjaminp/six](https://github.com/benjaminp/six)                             | 1.15.0    | [1.15.0](https://github.com/benjaminp/six/releases/tag/1.15.0)                                             |
| [enthought/traits](https://github.com/enthought/traits)                       | 6.2.0     | [6.2.0](https://github.com/enthought/traits/releases/tag/6.2.0)                                            |
| [urllib3/urllib3](https://github.com/urllib3/urllib3)                         | 1.26.3    | [1.26.3](https://github.com/urllib3/urllib3/releases/tag/1.26.3)                                           |
| [python-attrs/attrs](https://github.com/python-attrs/attrs)                   | 19.3.0    | [19.3.0](https://github.com/python-attrs/attrs/releases/tag/19.3.0)                                        |
| [CheetahTemplate3/cheetah3](https://github.com/CheetahTemplate3/cheetah3/)    | 3.2.4     | [3.2.4](https://github.com/CheetahTemplate3/cheetah3/releases/tag/3.2.4)                                   |
| [pallets/click](https://github.com/pallets/click)                             | 7.0       | [7.0](https://github.com/pallets/click/releases/tag/7.0)                                                   |
| [pallets/flask](https://github.com/pallets/flask)                             | 1.1.1     | [1.1.1](https://github.com/pallets/flask/releases/tag/1.1.1)                                               |
| [flask-restful/flask-restful](https://github.com/flask-restful/flask-restful) | 0.3.7     | [0.3.7](https://github.com/flask-restful/flask-restful/releases/tag/0.3.7)                                 |
| [pytest-dev/iniconfig](https://github.com/pytest-dev/iniconfig)               | 1.0.0     | [v1.0.0](https://github.com/pytest-dev/iniconfig/releases/tag/v1.0.0)                                      |
| [pallets/itsdangerous](https://github.com/pallets/itsdangerous)               | 1.1.0     | [1.1.0](https://github.com/pallets/itsdangerous/releases/tag/1.1.0)                                        |
| [pallets/jinja](https://github.com/pallets/jinja)                             | 2.10.3    | [2.10.3](https://github.com/pallets/jinja/releases/tag/2.10.3)                                             |
| [lxml/lxml](https://github.com/lxml/lxml)                                     | 4.4.1     | [lxml-4.4.1](https://github.com/lxml/lxml/releases/tag/lxml-4.4.1)                                         |
| [Python-Markdown/markdown](https://github.com/Python-Markdown/markdown)       | 3.1.1     | [3.1.1](https://github.com/Python-Markdown/markdown/releases/tag/3.1.1)                                    |
| [pallets/markupsafe](https://github.com/pallets/markupsafe)                   | 1.1.1     | [1.1.1](https://github.com/pallets/markupsafe/releases/tag/1.1.1)                                          |
| [pypa/packaging](https://github.com/pypa/packaging)                           | 19.2      | [19.2](https://github.com/pypa/packaging/releases/tag/19.2)                                                |
| [pexpect/pexpect](https://github.com/pexpect/pexpect)                         | 4.7.0     | [4.7.0](https://github.com/pexpect/pexpect/releases/tag/4.7.0)                                             |
| [pytest-dev/pluggy](https://github.com/pytest-dev/pluggy)                     | 0.13.0    | [0.13.0](https://github.com/pytest-dev/pluggy/releases/tag/0.13.0)                                         |
| [pexpect/ptyprocess](https://github.com/pexpect/ptyprocess)                   | 0.6.0     | [0.6.0](https://github.com/pexpect/ptyprocess/releases/tag/0.6.0)                                          |
| [pytest-dev/py](https://github.com/pytest-dev/py)                             | 1.8.0     | [1.8.0](https://github.com/pytest-dev/py/releases/tag/1.8.0)                                               |
| [pyparsing/pyparsing](https://github.com/pyparsing/pyparsing)                 | 2.4.5     | [pyparsing_2.4.5](https://github.com/pyparsing/pyparsing/releases/tag/pyparsing_2.4.5)                     |
| [pytest-dev/pytest](https://github.com/pytest-dev/pytest)                     | 5.3.0     | [5.3.0](https://github.com/pytest-dev/pytest/releases/tag/5.3.0)                                           |
| [stub42/pytz](https://github.com/stub42/pytz)                                 | 2019.3    | [release_2019.3](https://github.com/stub42/pytz/releases/tag/release_2019.3)                               |
| [uiri/toml](https://github.com/uiri/toml)                                     | 0.10.0    | [0.10.0](https://github.com/uiri/toml/releases/tag/0.10.0)                                                 |
| [pallets/werkzeug](https://github.com/pallets/werkzeug)                       | 0.16.0    | [0.16.0](https://github.com/pallets/werkzeug/releases/tag/0.16.0)                                          |
| [dmnfarrell/tkintertable](https://github.com/dmnfarrell/tkintertable)         | 1.2       | [v1.2](https://github.com/dmnfarrell/tkintertable/releases/tag/v1.2)                                       |
| [wxWidgets/wxPython-Classic](https://github.com/wxWidgets/wxPython-Classic)   | 2.9.1.1   | [wxPy-2.9.1.1](https://github.com/wxWidgets/wxPython-Classic/releases/tag/wxPy-2.9.1.1)                    |
| [nasa/fprime](https://github.com/nasa/fprime)                                 | 1.3       | [NASA-v1.3](https://github.com/nasa/fprime/releases/tag/NASA-v1.3)                                         |
| [nucleic/cppy](https://github.com/nucleic/cppy)                               | 1.1.0     | [1.1.0](https://github.com/nucleic/cppy/releases/tag/1.1.0)                                                |
| [opencv/opencv](https://github.com/opencv/opencv)                             | 4.5.1     | [4.5.1](https://github.com/opencv/opencv/releases/tag/4.5.1)                                               |
| [curl/curl](https://github.com/curl/curl)                                     | 7.72.0    | [curl-7_72_0](https://github.com/curl/curl/releases/tag/curl-7_72_0)                                     |
| [madler/zlib](https://github.com/madler/zlib)                                 | 1.2.11    | [v1.2.11](https://github.com/madler/zlib/releases/tag/v1.2.11)                                             |
| [apache/lucene](https://github.com/apache/lucene)                             | 7.7.3     | [releases/lucene-solr/7.7.3](https://github.com/apache/lucene/releases/tag/releases%2Flucene-solr%2F7.7.3) |
| [yaml/libyaml](https://github.com/yaml/libyaml)                               | 0.2.5     | [0.2.5](https://github.com/yaml/libyaml/releases/tag/0.2.5)                                                |
| [elastic/elasticsearch](https://github.com/elastic/elasticsearch)             | 6.8.1     | [v6.8.1](https://github.com/elastic/elasticsearch/releases/tag/v6.8.1)                                     |
| [twbs/bootstrap](https://github.com/twbs/bootstrap)                           | 4.3.1     | [v4.3.1](https://github.com/twbs/bootstrap/releases/tag/v4.3.1)                                            |
| [vuejs/vue](https://github.com/vuejs/vue)                                     | 2.6.10    | [v2.6.10](https://github.com/vuejs/vue/releases/tag/v2.6.10)                                               |
| [carrotsearch/hppc](https://github.com/carrotsearch/hppc)                     | 0.7.1     | [0.7.1](https://github.com/carrotsearch/hppc/releases/tag/0.7.1)                                           |
| [JodaOrg/joda-time](https://github.com/JodaOrg/joda-time)                     | 2.10.1    | [v2.10.1](https://github.com/JodaOrg/joda-time/releases/tag/v2.10.1)                                       |
| [tdunning/t-digest](https://github.com/tdunning/t-digest)                     | 3.2       | [t-digest-3.2](https://github.com/tdunning/t-digest/releases/tag/t-digest-3.2)                             |
| [HdrHistogram/HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)     | 2.1.9     | [HdrHistogram-2.1.9](https://github.com/HdrHistogram/HdrHistogram/releases/tag/HdrHistogram-2.1.9)         |
| [locationtech/spatial4j](https://github.com/locationtech/spatial4j)           | 0.7       | [spatial4j-0.7](https://github.com/locationtech/spatial4j/releases/tag/spatial4j-0.7)                      |
| [locationtech/jts](https://github.com/locationtech/jts)                       | 1.15.0    | [jts-1.15.0](https://github.com/locationtech/jts/releases/tag/jts-1.15.0)                                  |
| [apache/logging-log4j2](https://github.com/apache/logging-log4j2)             | 2.11      | [log4j-2.11.0](https://github.com/apache/logging-log4j2/releases/tag/log4j-2.11.0)                         |

## Leia mais

- "[Sobre seu perfil](/articles/about-your-profile)"
