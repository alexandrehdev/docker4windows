# docker4win
# ENG
### Step by Step

### Unfortunately this configuration could be only done on Windows 10, because older versions do not offer support.

- First thing first, we need to enable a WSL extension for windows. And we can do that running the command line bellow:

``` dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart ```

- Alright, now we need to enable another resource to install a WSL 2

``` dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart ```

- Now, it will be needed reboot your system

- After reboot your system, we need to update the linux kernel, just click the link bellow and the download will start

```https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi```

- Now we will set a default WSL version for docker

``` wsl --set-default-version 2 ```

- Install a linux distro on windows store, I recommend *Ubuntu 18.04 LTS*

- After you install, if you search for Ubuntu on cortana, you will find a Ubuntu terminal.

- Open it

- Set the initial config, username, password

- And that's it

# PT-BR

## Passo a passo 

### Infelizmente esta configuração so pode ser feita no Windows 10 por outras versões mais antigas do windows não oferecerem suporte.

- Precisamos habilitar uma configuração que possibilita um subsistema do Windows para Linux. Abra seu powershell em modo administrador, copie e cole no powershell e execute a linha de comando abaixo:

``` dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart ```

 

- Agora, vamos habilitar um recurso necessário para que possamos instalar o WSL 2... E faremos isso com o comando abaixo:

``` dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart ```

 
- Os comandos anteriores apenas realizaram as configurações... Para que elas sejam aplicadas, é necessário estar reiniciando sua máquina antes de seguir com o próximo passo.

 
- Após ter reiniciado sua máquina, nesta etapa iremos atualizar com um pacote de atualização do kernel do Linux. Acesse o link abaixo que irá baixar automaticamente. Após baixar, instale:

 

```https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi```

 
- Agora iremos definir a versão padrão do WSL que seja compatível com o docker. Segue linha de comando:

``` wsl --set-default-version 2 ```

- Agora instale alguma distribuição linux de sua escolha na Windows Store. Podendo acessar pelo link abaixo ou ir manualmente na barra de tarefas do windows.

```https://aka.ms/wslstore```

- Recomendo *Ubuntu 18.04 LTS* . Apos instalar, inicie. Você irá fazer uma configuração de usuário pedindo seu nome de usuario e senha.

- E para este ultimo passo, seja feliz. Para qualquer problema de execução, basta refazer o processo de instalação.
