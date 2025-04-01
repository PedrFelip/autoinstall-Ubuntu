# autoinstall-Ubuntu

Este repositório contém um arquivo de configuração chamado `autoinstall` em formato YAML, projetado para automatizar a instalação do Ubuntu 24.04 LTS (Noble Numbat).

## Sobre o arquivo `autoinstall`

O arquivo `autoinstall` permite personalizar e automatizar diversos aspectos da instalação do Ubuntu. Ele é utilizado pelo sistema de instalação para configurar o sistema durante o processo, eliminando a necessidade de interação manual em várias etapas.

## Utilização no Ubuntu 24.04 LTS

Este arquivo `autoinstall` foi criado especificamente para ser utilizado durante a instalação do Ubuntu 24.04 LTS. Ao fornecer este arquivo ao instalador, você pode automatizar tarefas como:

## Usando este arquivo como base para sua instalação

Sim, você pode usar este arquivo `autoinstall` como ponto de partida para criar sua própria configuração de instalação automática do Ubuntu 24.04 LTS. Basta editar as seguintes seções com seus dados:

* **`identity`**:
    * `realname`: Substitua 'Pedro Felipe' pelo seu nome completo.
    * `username`: Substitua 'pedrofelipe' pelo nome de usuário desejado.
    * `password`: **Importante:** Gere um hash de senha seguro usando o comando `mkpasswd` (ou `mkpasswd -m sha-512` para um hash SHA-512) e substitua o hash existente.
    * `hostname`: Substitua 'ubuntu-pedro' pelo nome que você deseja para o seu computador.
* **`locale`**: Se você preferir outro idioma, altere 'pt\_BR.utf8' para o código de localidade desejado.
* **`keyboard`**: Se o layout do seu teclado for diferente, altere 'br' para o layout correto.
* **`timezone`**: Altere "America/Sao\_Paulo" para o seu fuso horário. Você pode encontrar a lista de timezones em [https://en.wikipedia.org/wiki/List_of_tz_database_time_zones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).
* **`packages`**: Adicione ou remova os pacotes que você deseja instalar automaticamente.
* **`snaps`**: Adicione ou remova os snaps que você deseja instalar automaticamente.

## Conteúdo do arquivo `autoinstall`

O arquivo `autoinstall` (neste repositório nomeado como `autoinstall`) contém as seguintes configurações principais:

* `autoinstall`: Seção principal para configurações de instalação automática.
    * `version`: Versão da configuração autoinstall.
    * `identity`: Configurações de identidade do usuário (nome real, usuário, senha, hostname).
    * `locale`: Define o idioma do sistema.
    * `keyboard`: Configura o layout do teclado.
    * `timezone`: Define o fuso horário.
    * `packages`: Lista de pacotes a serem instalados usando `apt`.
    * `snaps`: Lista de snaps a serem instalados.
    * `codecs`: Define se os codecs devem ser instalados.
    * `drivers`: Define se os drivers devem ser instalados.
    * `updates`: Configura a instalação de atualizações.
    * `shutdown`: Define a ação a ser tomada após a instalação (neste caso, `reboot`).

## Como usar

Durante o processo de instalação do Ubuntu 24.04 LTS, o instalador oferece a opção de carregar uma configuração de "autoinstall". Você pode fornecer o caminho para este arquivo `autoinstall` (por exemplo, em um pendrive ou acessível via rede) para que a instalação seja realizada de forma automática com as configurações definidas.

**Observação:** A senha fornecida neste arquivo é um hash.
