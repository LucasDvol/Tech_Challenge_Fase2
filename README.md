Thech Challenge Fase 2 [Grupo 33]

Etapa 1: Extração dos dados
Dados foram extraídos de forma manual a partir das tabelas disponibilizadas em https://br.investing.com/indices/bovespa-historical-data. 
Foi selecionado o perído de 01/1990 a 06/2024, e posteriormente feito o upload para este repositório.


Etapa 2: Processamento das informações via Python
Utilizando notebook deste repoitório foi possível a relização das análises conforme tópicos abaixo:

Passo 1: Importando os dados

Utilizando a biblioteca Pandas, importamos os dados diretamente deste repositório.

Passo 2: Limpeza e Análise Exploratória de Dados

Neste passo, avaliamos as informações contantes no dataframe, para verificamos:
Primeiras linhas do arquivo:

![image](https://github.com/user-attachments/assets/9de94446-5dc8-4737-a2a2-3979e2815ec5)

Avaliamos informações utilizando a função describe:

![image](https://github.com/user-attachments/assets/b5237336-fcc1-419b-83fd-ec934d004cdc)

Durante a análise, verificamos também a existência de uma linha null no campo "Vol.", o que fez necessária a interpolação dos dados.

![image](https://github.com/user-attachments/assets/830a8ffa-c20a-4f5d-a787-4956e2d5f768)

Por fim, plotamos a informação do valor de fechamento ao longo do período selecionado, para verificar de forma visual como se deu o comportamento da base durante os anos:

![image](https://github.com/user-attachments/assets/7b29604a-6c48-4228-89ef-ed4b29dd3b2c)


Passo 3: Desenvolvimento do Modelo Preditivo

Nesta etapa, dicidimos pela utilização do modelo LSTM (Long Short-Term Memory)

O modelo LSTM foi escolhido para o projeto devido à sua capacidade de aprender dependências temporais de alta complexidade e de longo prazo, sua flexibilidade em lidar com sequências variáveis e dados irregulares, e sua eficácia demonstrada em diversas aplicações práticas. 
A possibilidade de captar relações não lineares entre os dados ao longo do tempo também foi decisivo, considerando que a série histórica da base de fechamento da IBOVESPA tem essa característica.

Dividimos a base em 80% para treino e 20% teste.

Passo 4: Avaliação do Modelo


![image](https://github.com/user-attachments/assets/90f0f51a-992c-47c1-afd6-65a4d672be66)
![image](https://github.com/user-attachments/assets/5957b2a3-16fd-4498-94af-e47ff701ea0a)


Etapa 3: Conclusão











![image](https://github.com/user-attachments/assets/2eedbbe2-da72-4883-8f92-c2e8a1233890)

