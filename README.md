Este mod foi descontinuado no momento e pode ser reescrito no futuro.


[![Github All Releases](https://img.shields.io/github/downloads/electricgun/video-to-logic/total.svg)]() <br>
[Baixe a versão mais recente.](https://github.com/ElectricGun/video-to-logic/releases/latest) <br>
# Registro de alterações:
* Adicionado *sem bloqueio* para configurar o processador. Defina como 1 para permitir o processamento de quadros grandes em vários processadores
  
## Chegando (not) breve:
* Buffer de quadros
* Edição em tempo real
  
# Sobre:
Converte uma sequência para uma animação de exibição lógica Mindustry <Converte uma sequência para uma animação de exibição lógica Mindustry <br> <br>
Dependências:[electricgun/message-block-commands](https://github.com/ElectricGun/message-block-commands)

## Como usar:
0. Use o [video converter script](https://github.com/ElectricGun/video-converter/releases/latest "Video Converter") para converter um vídeo em um formato utilizável (ou criar seu próprio script, o formato de saída deve ser o mesmo) <br> <br>
1. Instalar electricgun/message-block-commands *(en)* <br> <br>
2. Copie a saída do conversor de vídeo para a pasta animations no diretório mod. Talvez seja necessário descompactar a pasta mod primeiro <br> <br>
![example1](resources/guide1.gif)
3. Coloque um bloco de mensagem em um Sandbox World <br> <br>
4. Tipo "/v2logic args= **(medianame)**, **(maxCol**), **(scale)**, **(processorType)**" no bloco de mensagens, onde <br>**- (medianame)** é o nome da sua pasta de sequência na pasta de animações, <br> **- (maxCol)** é o número máximo de "desenhar cores" por cores adjacentes. Valores mais altos levam a um tamanho de esquema menor, <br> **- (scale)** é o fator de escala <br> **- (processorType)** é o tipo dos processadores (in camelcase e.g. worldProcessor) <br>  <br>Example comando: <br> 
![example1](resources/example1.png) <br> <br>
5. Sair do bloco de mensagens da interface gráfica (this will lag for a few moments). <br> <br>
6. Wait for it to finish, building the processors might take a while depending on your CPU and the overall size of the sequence <br> <br>
7. Exit the world and rejoin to refresh the processors <br> <br>
8. Edit the config processor (the microprocessor to the right of the clock processor) to your liking <br> <br>
![example1](resources/example2.png)
9. Activate the switch to play. <br> <br>
## Important: 
- If your animation is very crusty and choppy, the instructions per tick may be too high. Consider lowering it to about 750, or disable *forceRender* in the config processor.
- The processors will overwrite blocks around the main display, only use this mod on **disposable sandbox worlds**, you can then save it as a scheme after it's done <br>
- The *ipt* variable only works on world processors, obviously <br>
- Multiprocessing is currently not supported to reduce crust, large animations are very slow unless you use world processors or cheating the ipt of regular processors up. Might give the option to enable multiprocessing if you really don't mind the crust <br>
- Config file directory: data/config.hjson <br>
<br>
The mod itself doesn't work on multiplayer, but the schematics should.
