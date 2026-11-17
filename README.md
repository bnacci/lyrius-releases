<p align="center">
  <img src="assets/logo.png" width="96" height="96" alt="Lyrius">
</p>

<h1 align="center">Lyrius</h1>

<p align="center">
  Letras, Bíblia e mídia no telão, com a equipe no controle pelo celular.<br>
  <a href="https://lyrius.app">lyrius.app</a> ·
  <a href="https://github.com/bnacci/lyrius-releases/releases/latest"><b>Baixar a versão mais recente</b></a> ·
  <a href="#english">English</a>
</p>

---

Este repositório guarda só os **instaladores** do Lyrius e da extensão do
navegador. Cada versão fica em [Releases](https://github.com/bnacci/lyrius-releases/releases),
com as novidades e os arquivos para baixar.

## Qual arquivo baixar

Abra a [versão mais recente](https://github.com/bnacci/lyrius-releases/releases/latest)
e escolha pelo seu sistema (`<versão>` é o número da versão, ex.: `1.0.0`):

| Sistema | Arquivo |
|---|---|
| Windows 10 e 11 (64 bits) | `Lyrius-<versão>-windows-x64-setup.exe` — instalador<br>`Lyrius-<versão>-windows-x64-portable.zip` — sem instalar |
| Ubuntu 24.04 ou mais novo, Debian 13 | `lyrius_<versão>_amd64.deb` |
| Ubuntu 22.04 | `lyrius_<versão>_amd64-ubuntu22.04.deb` |
| Fedora e outras distros Linux | `lyrius-<versão>-linux-x64.tar.gz` |
| Android 7.0 ou mais novo (controle remoto) | `Lyrius-<versão>-android.apk` |
| Extensão do navegador (Cifra Club) | `Lyrius-extensao-<versão>-*.zip` |

Ainda não há versão para macOS nem para iPhone.

## Como instalar

**Windows** — abra o `setup.exe` e siga os passos. Se o Windows mostrar
"O Windows protegeu o computador", clique em **Mais informações › Executar
assim mesmo**.

**Ubuntu e Debian** — instale pelo terminal, para vir junto o que o
Lyrius precisa:

```sh
sudo apt install ./lyrius_<versão>_amd64.deb
```

**Outras distros Linux** — extraia o `.tar.gz` e rode `./lyrius` dentro
da pasta.

**Android** — abra o `.apk` no celular. Se pedir, permita instalar apps
desta fonte. O celular e o computador precisam estar na mesma rede.

**Extensão do navegador** — em breve nas lojas oficiais. Até lá, veja
[lyrius.app/extensions](https://lyrius.app/extensions).

## Atualizações

O Lyrius se atualiza sozinho: **Sobre › Atualizações** baixa a versão
nova daqui, confere o arquivo e instala quando você pedir. Nunca com o
telão no ar.

## Conferir o download

Cada versão tem um `SHA256SUMS.txt`. No Linux, na pasta dos arquivos:

```sh
sha256sum -c SHA256SUMS.txt --ignore-missing
```

No Windows (PowerShell): `Get-FileHash .\arquivo.exe` e compare com a
linha do arquivo no `SHA256SUMS.txt`.

## Ajuda

- Problemas comuns e passo a passo: [lyrius.app/support](https://lyrius.app/support)
- Perguntas frequentes: [lyrius.app/faq](https://lyrius.app/faq)
- Contato: [lyrius.app/contact](https://lyrius.app/contact)

Ao usar o Lyrius você aceita a [Licença de uso](https://lyrius.app/license)
e os [Termos de Uso](https://lyrius.app/legal/terms). Privacidade:
[lyrius.app/legal/privacy](https://lyrius.app/legal/privacy).

---

## English

Lyrius puts lyrics, the Bible and media on the big screen, with the team
in control from their phones. This repository only holds the installers;
each version is in [Releases](https://github.com/bnacci/lyrius-releases/releases).

| System | File |
|---|---|
| Windows 10 and 11 (64-bit) | `Lyrius-<version>-windows-x64-setup.exe` (installer) or `-portable.zip` |
| Ubuntu 24.04 or newer, Debian 13 | `lyrius_<version>_amd64.deb` |
| Ubuntu 22.04 | `lyrius_<version>_amd64-ubuntu22.04.deb` |
| Fedora and other Linux distros | `lyrius-<version>-linux-x64.tar.gz` (extract and run `./lyrius`) |
| Android 7.0 or newer (remote control) | `Lyrius-<version>-android.apk` |

Not yet available for macOS or iPhone. On Ubuntu/Debian, install with
`sudo apt install ./lyrius_<version>_amd64.deb`. If Windows shows "Windows
protected your PC", click **More info › Run anyway**. Lyrius updates
itself from **About › Updates**. Check downloads with `SHA256SUMS.txt`.

Help: [lyrius.app/en/support](https://lyrius.app/en/support) ·
[License agreement](https://lyrius.app/en/license) ·
[Privacy](https://lyrius.app/en/legal/privacy)

---

<p align="center">Feito pela <a href="https://triooo.com.br">triooo</a> · © 2026 triooo. Todos os direitos reservados.</p>
