# Manus AI Agent - Proof of Concept

O Manus AI Agent opera de forma autônoma em um ambiente sandbox no lado do servidor, apresentando ao usuário todo o processo de raciocínio, pesquisas e arquivos utilizados. Vamos detalhar como isso poderá funcionar:

## Ambiente de Execução

O Manus AI roda em um **ambiente sandbox Linux** no lado do servidor. Este ambiente controlado permite que o agente execute várias tarefas de forma segura, incluindo:

- Instalação de software
- Execução de scripts
- Manipulação de arquivos
- Navegação na web - Browserless
- Processamento de dados

## Processo de Execução

Quando um usuário faz uma solicitação, o Manus AI segue um processo estruturado:

1. Analisa o pedido do usuário
2. Seleciona as ferramentas apropriadas
3. Executa comandos no ambiente sandbox
4. Itera e refina suas ações com base nos resultados
5. Submete os resultados finais ao usuário

## Apresentação ao Usuário

O Manus AI oferece uma experiência transparente ao usuário:

- Exibe uma **janela com um computador virtual** que realiza pesquisas em tempo real
- Mostra o **passo a passo seguido pela IA**, incluindo pesquisas feitas e arquivos gerados
- Apresenta uma **janela de prompt** que exibe todo o processo de raciocínio
- Lista todos os **arquivos criados durante o processo**

## Processamento em Nuvem

Uma característica importante do Manus AI é que todo o seu funcionamento ocorre remotamente:

- O processamento é feito **na nuvem**, permitindo que o usuário desligue seu dispositivo enquanto a IA continua trabalhando
- Os resultados ficam disponíveis para acesso posterior, sem perda de progresso

Esta abordagem oferece uma visão completa do processo de raciocínio do agente de IA, permitindo que os usuários entendam como as conclusões foram alcançadas e quais recursos foram utilizados.

---

# Projecto AI Agent text-to-action

Manus AI Agent pelo que parece roda do lado do servidor, mas poderá ser feito no lado do usuario combinando várias funcionalidades de automação de sistemas operacionais, captura de tela, web scraping, e controle remoto. Este projeto foi iniciado para estudo e como prova de conceito de um agente IA capaz de interagir com o sistema do usuário, realizar tarefas automatizadas e fornecer uma interface simples via UI. **AI Agent text-to-action**.


## Funcionalidades

- **Captura de Tela**: O Manu AI pode capturar screenshots em tempo real para análise.
- **Web Scraping**: Navega e interage com páginas web para extrair informações.
- **Controle do Sistema Operacional**: Executa comandos em sistemas Windows, Linux e macOS, como ler, escrever e manipular arquivos.
- **Automação de Tarefas**: Controla aplicativos e interage com o sistema via comandos de teclado e mouse.
- **Integração com IA**: Utiliza LLMs (Modelos de Linguagem) para interpretação de comandos e respostas.

## Tecnologias Utilizadas

- **Backend**: Flask
- **Captura de Tela**: PyScreenshot, OpenCV, Pillow, JS no frontend para capturar a tela do usuário
- **Web Scraping & Navegação**: Selenium, BeautifulSoup, Requests, Browserless
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
pip install flask streamlit uvicorn
pip install marvin groq  # (ou outras libs para LLMs)
pip install openai  # Se quiser usar GPTs externos
pip install flake8 mypy ruff # development
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

### **5. Code execution**
```sh
# Code execution
pip install jupyter-client nbformat

### **5. Gerenciamento de Dependências e Virtualização**  
Se quiser manter o projeto organizado e replicável:  
```sh
pip install pipenv  # Melhor que requirements.txt
pip install pyinstaller  # Para criar executáveis standalone
```
