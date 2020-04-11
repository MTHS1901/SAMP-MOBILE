# SAMP MOBILE BUILD 6.9 (MTHS1901)
#### Mudanças feitas por mim
##### Jogo rodar em 60FPS e Exibir a taxa de FPS dentro do jogo.
##### Possibilidade de alterar o servidor, busque por "// IP SERVIDOR" dentro de main.ccp.
##### Nova tela de carregamento com logo oficial do SAMP.
##### - **Essa é minha primeira BUILD publica, não sei se vou continuar o projeto, pois é muito complicado e limitado.**
---------- # # # # ----------
# TUTORIAL DE COMPILAÇÃO NO WINDOWS
### Não é algo pra leigos, exige um certo conhecimento para executar o procedimento.
## Programas necessarios:
##### Android NDK 14 #necessario para compilação# (https://developer.android.com/ndk/downloads/older_releases#ndk-14b-downloads)
##### Notepad++ #necessario para edição/programação dos arquivos .ccp# (https://notepad-plus-plus.org/downloads/)
##### O Ideal seria utilizar o Visual Studio, porem como os arquivos são compilados fora do Visual Studio, você pode editar os arquivos fora do Visual Studio tambem.
# COMO COMPILAR
##### Essa é a forma como eu compilo, mais existe outras formas, crie comandos .cmd para executar isso automaticamente para você e economize seu tempo, primeiramente acesse a pasta do ANDROID-NDK-R14, dentro da pasta "BUILD" tem um arquivo com nome "NDK-BUILD.cmd", edite o arquivo com BLOCO DE NOTAS e adicione um "PAUSE" no final, igual mostra abaixo, isso será essencial na hora de compilar, pois toda vez que é compilado abre uma tela no PROMPT DE COMANDO rapidamente, as vezes acontece erros na compilação e você não vai ver a tempo e o comando "PAUSE" vai pausar o PROMPT DE COMANDO fazendo com que seja possivel você ver os erros.
```
@echo off
set NDK_ROOT=%~dp0\..
set PREBUILT_PATH=%NDK_ROOT%\prebuilt\windows-x86_64
if exist %PREBUILT_PATH% goto FOUND
set PREBUILT_PATH=%NDK_ROOT%\prebuilt\windows
:FOUND
"%PREBUILT_PATH%\bin\make.exe" -f "%NDK_ROOT%\build\core\build-local.mk" SHELL=cmd %*
PAUSE
```
## Arquivo .CMD que deve ser criado para fazer a compilação.
```
#PRIMEIRA LINHA# cd "diretorio onde a BUILD esta descompactada"
#SEGUNDA LINHDA# "diretorio do Android NDK com "\ndk-build" no final"
```
## Exemplo:
```
cd C:\Users\MATHEUS\Desktop\SAMP-Master
C:\android-ndk-r14\ndk-build
```
## Exemplo em foto:
![alt text](https://raw.githubusercontent.com/MTHS1901/SAMP-MOBILE/master/ex-compile.png)
### Observação: apos compilar a libsamp.so fica dentro do diretorio "SAMP-Master/libs/armeabi-v7a/libsamp.so"
## Exemplo em foto:
![alt text](https://raw.githubusercontent.com/MTHS1901/SAMP-MOBILE/master/ex-compile2.png)
## Em caso de pequenas duvidas entre em contato comigo, https://www.mths1901.com/suporte




