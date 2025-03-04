# Projeto: Leitor e Gerador de Provas Semelhantes

## Introdução

Este projeto tem como objetivo auxiliar estudantes que estão se preparando para provas, no caso do exemplo desenvolvido, provas de cientista de dados.
O objetivo é usar prints disponíveis online de provas antigas para gerar provas completas utilizando tecnologias avançadas de OCR (Reconhecimento Óptico de Caracteres) e modelos de linguagem natural (LLM).
A partir de imagens de provas antigas, o programa é capaz de tratar as imagens, extrair o texto contido nelas, processá-lo e gerar novas questões de múltipla escolha com conteúdos semelhantes.

### Objetivos Específicos

1. **Leitura de Provas Antigas:** Utilizar o Tesseract OCR para extrair texto de imagens de provas antigas.
2. **Geração de Novas Questões:** Utilizar modelos de linguagem natural, como o LLaMA 3.2-3B, para gerar novas questões de múltipla escolha baseadas no texto extraído.
3. **Criação de Bases de Dados Sintéticas (em andamento):** Gerar novas bases de dados fictícias para questões de aplicação de modelos de machine learning. 
4. **Acessibilidade (em andamento):** Tornar o programa acessível através de uma interface amigável, como o Streamlit.

### Tecnologias Utilizadas

- **OCR:** Tesseract OCR
- **Processamento de Imagens:** PIL, OpenCV
- **Manipulação de PDFs:** PyPDF2, img2pdf, pymupdf
- **Modelos de Linguagem Natural:** Transformers, LLaMA 3.2
- **Criação de PDFs:** FPDF

### Estrutura do Projeto

1. **Pré-processamento de Imagens:** Tratamento das imagens para melhorar a qualidade do OCR.
2. **Extração de Texto:** Extração do texto das imagens processadas.
3. **Geração de Questões:** Utilização de modelos de linguagem natural (LLM's) para gerar novas questões.
4. **Armazenamento e Acesso:** Salvamento dos resultados no Google Drive para facilitar o acesso futuro.

Este projeto visa não apenas facilitar o estudo utilizando provas antigas (o que geralmente traz mais resultados, visando melhores notas), mas também proporcionar uma maneira inovadora de gerar novas questões que usem dados, o que permite realizar questões práticas e com um certo nível de contexto.

### Resultados

Após a implementação do projeto, obtivemos os seguintes resultados:

1. **Leitura de Provas Antigas:**
    - Utilizamos o Tesseract OCR para extrair texto de imagens de provas antigas.
    - Realizamos o pré-processamento das imagens para melhorar a qualidade do OCR, incluindo conversão para escala de cinza, ajuste de tamanho e remoção de ruídos.
    - A leitura do OCR foi eficiente e será necessário realizar apenas mais alguns tratamentos de caracteres estranhos e truncamento, para diminuir o numero de tokens que o prompt irá conter.

2. **Geração de Novas Questões:**
    - Utilizamos o modelo LLaMA 3.2-3B para gerar novas questões de múltipla escolha baseadas no texto extraído.
    - As questões geradas seguiram as regras estabelecidas, com 4 opções de resposta, sendo apenas uma correta.
    - As questões são geradas, porém, com a limitação do uso da T4 do Google Collab é possível gerar aproximadamente apenas 3 questões (200 - 500 tokens cada) por dia.
    - O modelo ainda erra o gabarito de algumas questões, mas não alucina mais, como fazia com outros modelos menos potentes de 1B de parâmetros.
    - Ainda não foi implantada uma forma de usar a biblioteca _Faker_ para gerar bases sintéticas para uso nas questões, devido às complicações de limitação de processamento do autor e do Collab.

3. **Armazenamento e Acesso:**
    - Salvamos as imagens, PDFs e texto extraído no Google Drive para facilitar futuros acessos.
    - Ainda é necessário salvar as questões obtidas manualmente.

---

## Conclusão

Enfim, o projeto é capaz de realizar o tratamento e extração das imagens de forma prática usando os tratamentos testados e o Tesseract OCR. No entanto, na aplicação da leitura do texto e geração de questões houve a maior parte das dificuldades, pois é necessário muito poder computacional para realizar a geração de questões. Apesar disso, através do Google Collab, é possível gerar algumas questões por dia dos assuntos necessários. Os principais pontos de melhoria são um tratamento mais aprofundado do prompt, melhorar o gabarito fornecido pelo código, usar modelos mais leves ou afinar o modelo para utilizar menos poder computacional e gerar mais questões.

---

## Requisitos

Para executar este projeto, é necessário ter instalado os seguintes pacotes:

- **Python 3.x**
- **NumPy**
- **os**
- **PIL** (Pillow)
- **Pytesseract**
- **img2pdf**
- **fitz**
- **io**
- **transformers**
- **torch**
- **accelerate**

---

## Como Executar

Siga os passos abaixo para configurar e executar o projeto:

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```

2. **Navegue até o diretório do projeto**:
   ```bash
   cd seu-repositorio
   ```

3. **Instale as dependências**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Execute o Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

5. **Abra o notebook e execute as células sequencialmente**.

---

## Autor

- **José Vinícius Tavares**

---

## Licença

Este projeto está licenciado sob a **Licença MIT**. Para mais detalhes, consulte o arquivo [LICENSE](LICENSE).
