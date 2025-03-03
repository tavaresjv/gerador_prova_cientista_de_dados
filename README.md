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
