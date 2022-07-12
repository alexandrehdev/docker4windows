# docker4win
# ENG
### hold on...




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
