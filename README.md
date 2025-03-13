# Manus AI Agent - Proof of Concept

Manus AI Agent pelo que parece roda do lado do servidor, sandbox, onde é apresentado ao usuario todo o raciocinio, procuras e ficheiros usados, mas poderá ser feiro no lado do usuario combinando várias funcionalidades de automação de sistemas operacionais, captura de tela, web scraping, e controle remoto. Este projeto foi iniciado para estudo e como prova de conceito de um agente IA capaz de interagir com o sistema do usuário, realizar tarefas automatizadas e fornecer uma interface simples via UI. AI Agent text2action.

## Processo de execução Manu

Quando um usuário faz uma solicitação, o Manus AI Agent segue um processo estruturado:

- Analisa o pedido do usuário
- Seleciona as ferramentas apropriadas
- Executa comandos no ambiente sandbox
- Itera e refina suas ações com base nos resultados
- Submete os resultados finais ao usuário3

## Apresentação ao usuario

O Manus AI Agent oferece uma experiência transparente ao usuário:

- Exibe uma janela com um computador virtual que realiza pesquisas em tempo real4
- Mostra o passo a passo seguido pela IA, incluindo pesquisas feitas e arquivos gerados4
- Apresenta uma janela de prompt que exibe todo o processo de raciocínio4
- Lista todos os arquivos criados durante o processo4

---

# Conceito do lado do usuario

## Funcionalidades

- **Captura de Tela**: O Manu AI pode capturar screenshots em tempo real para análise.
- **Web Scraping**: Navega e interage com páginas web para extrair informações.
- **Controle do Sistema Operacional**: Executa comandos em sistemas Windows, Linux e macOS, como ler, escrever e manipular arquivos.
- **Automação de Tarefas**: Controla aplicativos e interage com o sistema via comandos de teclado e mouse.
- **Integração com IA**: Utiliza LLMs (Modelos de Linguagem) para interpretação de comandos e respostas.

## Tecnologias Utilizadas

- **Backend**: Flask
- **Captura de Tela**: PyScreenshot, OpenCV, Pillow, JS no frontend para capturar a tela do usuário
- **Web Scraping & Navegação**: Selenium, BeautifulSoup, Requests
- **Automação de Sistema**: PyWinAuto (Windows), PyAutoGUI, Keyboard (Linux/macOS)
- **IA & NLP**: Marvin, OpenAI, Transformers
- **Manipulação de Arquivos & Comandos**: Pyperclip, Psutil, Watchdog

## Instalação

### Requisitos

- Python 3.x
- Sistema Operacional: Windows, Linux ou macOS
- ChromeDriver (para Selenium)
- Inferencias rapidas com Groq e Inferencias com LLM de raciocinio e visão

1. Baixe o [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) e coloque-o no mesmo diretório do script ou configure o caminho corretamente.

## Bibliotecas Essenciais  

#### **Base (Core AI & Backend)**  
```sh
pip install flask
pip install marvin groq  # (ou outras libs para LLMs)
pip install openai  # Se quiser usar GPTs externos
```

#### **Captura e análise de tela**  
```sh
pip install pyscreenshot opencv-python pillow
pip install pytesseract  # Para OCR (se precisar ler texto das capturas)
```

#### **Web Scraping & Navegação Automática**  
```sh
pip install selenium webdriver-manager
pip install beautifulsoup4 requests
```
(O **Selenium** com **ChromeDriver** permite navegar na web e interagir com páginas.)

#### **Automação de Sistema Operacional**  
Para **Windows**:  
```sh
pip install pywinauto
```
Para **Linux/macOS**:  
```sh
pip install pyautogui
pip install keyboard mouse
```
(PyAutoGUI e Keyboard funcionam em todos os sistemas, mas PyWinAuto é mais poderoso para Windows.)  

#### **Manipulação de Arquivos & Comandos do Sistema**  
```sh
pip install watchdog
```
(Útil para monitorar arquivos em tempo real.)  

Se quiser um sistema mais seguro e isolado para comandos:  
```sh
pip install subprocess
```
(Usar subprocess pode dar mais controle sobre os processos que a IA executa.)  

---

Algumas bibliotecas extras podem ser úteis dependendo do que quiseres aprimorar. Aqui estão algumas sugestões adicionais:  

### **1. Melhor Controle do Sistema Operacional**  
Se quiser uma automação mais refinada e controle sobre processos:  
```sh
pip install psutil  # Para monitoramento de processos e uso de recursos
pip install pygetwindow  # Para manipular janelas abertas
pip install pyperclip  # Para copiar e colar texto
```

### **2. Segurança e Execução Segura**  
Se o Manu AI for executar comandos no sistema, segurança é essencial:  
```sh
pip install shlex  # Para sanitizar comandos antes de executar
pip install cryptography  # Para encriptar dados se for necessário
```

### **3. Melhor Manipulação de Texto e Conversação**  
Para melhorar a compreensão de comandos:  
```sh
pip install nltk spacy  # NLP avançado se necessário
pip install transformers  # Se quiser LLMs locais (como Llama, Mistral)
```

### **4. Integração com APIs e Serviços**  
Se quiser integrar o Manu com APIs externas:  
```sh
pip install httpx  # Alternativa mais rápida ao requests
pip install websocket-client  # Para comunicação em tempo real
```

### **5. Gerenciamento de Dependências e Virtualização**  
Se quiser manter o projeto organizado e replicável:  
```sh
pip install pipenv  # Melhor que requirements.txt
pip install pyinstaller  # Para criar executáveis standalone
```
