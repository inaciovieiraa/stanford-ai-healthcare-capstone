# AI in Healthcare Capstone: Detecção de COVID-19 e Previsão de UTI

![Stanford Medicine](https://img.shields.io/badge/Stanford-Medicine-8C1515?style=for-the-badge&logo=stanford-university&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Focus-Clinical%20Data%20Analysis-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge)

> 🇺🇸 **English:** [Click here to read in English](README-EN.md)
> **Certificado Oficial:** [Clique aqui para visualizar o certificado de Stanford(Coursera)](certificates/Stanford%20(Coursera).pdf)

## Visão Geral do Projeto
Este repositório documenta o meu **Portfólio de Decisão** como conclusão da especialização **"AI in Healthcare"** da Stanford University. 

Neste projeto simulado, atuei como **Analista de Dados (Lead Analyst)**, sendo responsável pela **estratégia, validação e ética** dos modelos de IA, supervisionando as decisões técnicas para garantir que a tecnologia fosse segura para uso hospitalar.

---

## Meus Desafios e Soluções (Perspectiva Enfermagem + Dados)

Como estudante de Enfermagem, meu papel foi traduzir a necessidade clínica para a equipe de desenvolvimento.

### 1. Limpeza de Dados
* **O Problema:** Havia mais exames que pacientes.
* **Minha Decisão:** Orientei a separação dos dados pelo **ID do Paciente**. Se separássemos aleatoriamente, o computador poderia "decorar" o paciente em vez de aprender a doença (Data Leakage).

### 2. Visão Computacional (Raio-X)
* **O Erro Encontrado:** A equipe técnica aplicou um "Zoom Aleatório" nas imagens para tentar melhorar o modelo.
* **Minha Correção:** Identifiquei que isso cortava partes vitais do pulmão. Vetei o zoom e permiti apenas rotações leves, garantindo a **Preservação Clínica** (a imagem precisa continuar legível para um médico).

### 3. Dados Tabulares (Prontuário/EHR)
* **Validação Justa:** Como tínhamos poucos casos graves (apenas 300 intubações), exigi o uso de **Validação Cruzada Estratificada**. Isso garante que todo teste tenha a quantidade certa de pacientes doentes, evitando falsos sucessos.

---

## Métricas e Resultados

### Por que rejeitei a "Acurácia"?
O modelo tinha 91% de acurácia, mas percebi que isso era enganoso porque a maioria dos pacientes era saudável. Se o modelo "chutasse" que todos os pacientes estavam saudáveis, ele teria uma acurácia alta.
* **Decisão:** Escolhi a métrica **AUROC** (0.872), que provou ser muito melhor para distinguir quem realmente estava doente.

### Previsão de 2h vs 48h
* O modelo de **2 horas** acertava mais, mas era inútil (o paciente já estava visivelmente grave).
* Escolhi o modelo de **48 horas** porque, mesmo errando um pouco mais, ele dá tempo para a equipe de enfermagem e médica prepararem a UTI. **Utilidade Clínica > Acurácia Pura.**

---

## Ética e Segurança (FDA)

Para garantir que o software pudesse ser aprovado por órgãos reguladores (como a FDA/ANVISA):
1.  **Classificação:** Defini o sistema como **Apoio à Decisão (Nível II)**. O humano sempre tem a palavra final.
2.  **Viés:** Solicitei testes obrigatórios em grupos de diferentes raças e gêneros para garantir que a IA não fosse preconceituosa.

---

## Limitações do Projeto
Este projeto foi desenvolvido em um contexto acadêmico e simulado, com base em dados históricos e cenários controlados. 
Os modelos apresentados **não devem ser utilizados diretamente em ambientes clínicos reais** sem validação externa, estudos prospectivos, testes multicêntricos e aprovação por órgãos reguladores competentes (ex.: ANVISA/FDA).

Além disso, limitações inerentes aos dados, como desbalanceamento de classes, tamanho amostral reduzido para eventos críticos e possível viés populacional, podem impactar a generalização dos resultados.

---

## Principais Aprendizados
- Métricas tradicionais, como acurácia, podem ser inadequadas em cenários clínicos com dados desbalanceados.
- A **utilidade clínica** de um modelo pode ser mais relevante do que sua performance numérica isolada.
- Decisões em IA aplicada à saúde exigem validação rigorosa, visão ética e preocupação com segurança do paciente.
- Profissionais de Enfermagem desempenham um papel estratégico na tradução entre necessidades clínicas e soluções baseadas em dados.
- Modelos de IA devem ser concebidos como **apoio à decisão clínica**, e não como substitutos do julgamento humano.

---

### Contato
**Inácio Santos Vieira**
[LinkedIn](https://www.linkedin.com/in/inaciosantosvieira/)
