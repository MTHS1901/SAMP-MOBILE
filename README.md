# SAMP MOBILE BUILD 6.9 (MTHS1901)
#### Mudanças feitas por mim
##### ﹥ Jogo rodar em 60FPS e Exibir a taxa de FPS dentro do jogo.
##### ﹥ Possibilidade de alterar o servidor, busque por "// IP SERVIDOR" dentro de main.ccp.
##### ★ Essa é minha primeira BUILD publica, não sei se vou continuar o projeto, pois é muito complicado e limitado.
##### ★ BUILD ORIGINAL: https://github.com/4x11/build69
---------- # # # # ----------
# TUTORIAL DE COMPILAÇÃO NO WINDOWS
### Não é algo pra leigos, exige um certo conhecimento para executar o procedimento.
## Programas necessarios:
##### ﹥ Android NDK 14 #necessario para compilação# (https://developer.android.com/ndk/downloads/older_releases#ndk-14b-downloads)
##### ﹥ Notepad++ #necessario para edição/programação dos arquivos .ccp# (https://notepad-plus-plus.org/downloads/)
# COMO COMPILAR A "libsamp.so"
##### É assim que eu compilo, mas existem outras maneiras de compilar, crie comandos .cmd para executar automaticamente para você vai economizar muito seu tempo, primeiro de tudo acesse a pasta "ANDROID-NDK-R14" dentro da pasta "BUILD" existe um arquivo com um nome "NDK-BUILD.cmd", edite o arquivo com o NOTEPAD e adicione uma "PAUSE" no final, como mostrado abaixo, isso será essencial ao compilar, porque toda vez que é compilado abre rapidamente uma tela no PROMPT DE COMANDO, às vezes há erros na compilação e você não o verá a tempo e o comando "PAUSE" fará uma pausa no PROMPT DE COMANDO, possibilitando a visualização dos erros.
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
## Arquivo .CMD que deve ser criado para fazer a compilação rapida.
```
#PRIMEIRA LINHA# cd "diretorio onde a BUILD esta descompactada"
#SEGUNDA LINHDA# "diretorio do Android NDK com "\ndk-build" no final"
```
## Exemplo:
```
cd C:\Users\MATHEUS\Desktop\SAMP-Master
D:\android-ndk-r14\ndk-build
```
## Exemplo em foto:
![alt text](https://1.bp.blogspot.com/-QwJidaE2J20/XpJTdn6gcOI/AAAAAAAAPbI/pFsRkSvv1ccp19oWkEtXS8FDCtg3IT2PACLcBGAsYHQ/s1600/ex-compile.png)
### Observação: apos compilar a libsamp.so fica dentro do diretorio "SAMP-Master/libs/armeabi-v7a/libsamp.so"
## Exemplo em foto:
![alt text](https://2.bp.blogspot.com/-XQJS3OzEp4U/XpJTehaxQRI/AAAAAAAAPbM/byNDtMguyeQVzvgFw0Gj-_feAp5rOyz0QCLcBGAsYHQ/s1600/ex-compile2.png)
# COMO COMPILAR O APK
## Programas necessarios:
##### ﹥ Easy APK Tool: https://forum.xda-developers.com/android/software-hacking/tool-apk-easy-tool-v1-02-windows-gui-t3333960 (ferramenta para compilar/descompilar/instalar/registrar arquivos .apk)
##### ﹥ APK do SAMP na BUILD 6.9: https://www.androgamer.org/samp-mobile-6-9/ ou https://github.com/MTHS1901/SAMP-MOBILE/raw/master/SAMP_MTHS1901_b.0.0.1.apk (ambas compativel com o GTA LITE)
##### ﹥ ADB Minimal Fastboot: https://forum.xda-developers.com/showthread.php?t=2317790 (para conseguir instalar o APK via cabo USB)
##### Use o programa para compilar o APK, copie a "libsamp.so" modificada para a pasta "1-Decompiled APKs" do Easy APK Tool, e compile o APK pelo programa.
## DUVIDAS? ENTRE EM CONTATO: 
##### www.mths1901.com/suporte ou www.androgamer.org/contato






