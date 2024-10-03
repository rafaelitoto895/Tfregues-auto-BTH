# Tfregues-auto-BTH

Este é um macro para o jogo *Bit Heroes*, desenvolvido pelo fregues com o objetivo de facilitar o jogo ao máximo. Ainda estou trabalhando nele e muitas mudanças podem ser feitas no futuro. Atualmente, o macro utiliza um método de detecção de imagens para realizar o *AFKFARM*, tornando-o útil para deixar rodando enquanto você dorme.



## Arquivos

- **data**: Contém as imagens e recursos necessários para o funcionamento do macro.
- **logs**: Armazena os registros das atividades realizadas pelo macro, permitindo monitorar o desempenho e identificar possíveis problemas.
- **[level0.py](https://github.com/rafaelitoto895/Tfregues-auto-BTH/blob/main/level0.py)**: Contém funções comuns usadas por outros arquivos do macro, incluindo:
  - `stop_macro()`: Ativado pela GUI, interrompe o macro.
  - `verificar_interrupcao()`: Verifica se a tecla 'ESC' foi pressionada para interromper o macro.
  - `detectar_aspecto_na_tela(imagem_modelo, threshold=0.8)`: Detecta uma imagem específica na tela.
  - `encontrar_imagem_e_clicar(imagem, descricao)`: Encontra uma imagem na tela e clica nela.
  - `macro_leaving_mission()`: Executa uma sequência para sair de uma missão.
  - `verificar_reconectar(imagem_condicao, descricao)`: Verifica uma condição especial na tela. Se a imagem for encontrada, clica nela e reinicia o processo.
- **[level1.py](https://github.com/rafaelitoto895/Tfregues-auto-BTH/blob/main/level1.py)**: Implementa a lógica principal para a execução do macro, focando nas missões.
- **[main.py](https://github.com/rafaelitoto895/Tfregues-auto-BTH/blob/main/main.py)**: O ponto de entrada do programa, onde a execução do macro é iniciada.

Futuramente, planejamos adicionar os macros `level2`, `level3`, `level4`, `level5`, `level6`, e `level7`.

## Considerações

Atualmente o macro só foi testado na resolução 800x480, então talvez não funcione corretamente com as demais resoluções.

Apenas suportado no Idioma PT BR, futuramente irei adicionar suporte para o Inglês. 

O arquivo `level1.py`, responsável por automatizar as missões, ainda não está 100% completo. Na seleção de fases, não consegui incluir todas as opções. Enquanto isso, você pode ir até `data\level\level1` e trocar a imagem `m2` pela fase que deseja jogar. Recomendo o uso do Lightshot para capturar as imagens.

Exemplo:

![m2](https://github.com/user-attachments/assets/95392baf-6313-4640-bd8a-a125bf0ba589) ![m2b](https://github.com/user-attachments/assets/c02adeff-acad-41db-bda0-06ce5db8d23c) ![m2c](https://github.com/user-attachments/assets/a677a861-27c8-4d58-8e85-6d828d4b41ec)

No momento, o macro está configurado apenas para missões.

Ainda em desenvolvimento, interface gráfica (GUI) usando a biblioteca Pygame.
 
## Executando

1. Clone o repositório:
	```bash
	git clone https://github.com/rafaelitoto895/Tfregues-auto-BTH.git
	```
2. Instale as dependências necessárias:
	```bash
	pip install opencv-python numpy pyautogui pygame
	```
3. Execute o macro com o seguinte comando:
	```bash
	python main.py
	```
   
## Compilando
	
1. certifique-se que as dependências estão instaladas:
	```bash
	pip install opencv-python numpy pyautogui pygame pyinstaller
	```
2. compile o projeto em um único arquivo:
	```bash
	pyinstaller --onefile --noconsole --icon=icon.ico --add-data "data;data" main.py
	```
	
## Dicas e Soluções de Problemas

- **Problema: O macro não encontra a imagem.**
  - Certifique-se de que a imagem está na resolução correta e no formato suportado.
  - Verifique se o arquivo de imagem está no diretório correto (`data\level\level$`).
  
- **Problema: O macro trava ou não responde.**
  - Pressione a tecla 'ESC' no console para interromper o macro. 
  - Verifique se a resolução da tela está configurada para 800x480.

- **Problema: O macro não está executando as missões corretamente.**
  - Tente trocar a imagem `m2` pela fase que deseja jogar, conforme indicado na seção de considerações.

## Contribuições

![marca_small](https://github.com/user-attachments/assets/3a29afa3-0b39-43ee-9760-cca03d978e62)

-------

Sinta-se à vontade para contribuir! Abra um issue ou envie um pull request.

## Licença

Este projeto está licenciado sob a [MIT License.](https://github.com/rafaelitoto895/Tfregues-auto-BTH/blob/main/LICENSE.txt)
