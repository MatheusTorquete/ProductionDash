# Dashboard de Produção
Este projeto consiste em um dashboard para a área de produção, desenvolvido utilizando Power BI e dados fornecidos em Excel. 

O objetivo principal é monitorar e analisar a eficiência e a qualidade da produção, permitindo identificar pontos de melhoria e garantir uma operação otimizada.

Descrição do Projeto
O dashboard de produção foi criado para responder às principais perguntas e métricas relacionadas ao desempenho da linha de produção. 

A base de dados contém informações detalhadas sobre as ordens de produção, operadores, produtos, ocorrências e tempos de trabalho.

# Visão Geral: Um resumo das principais métricas de produção.
![image](https://github.com/user-attachments/assets/a32f336f-cd28-4a2b-9434-54fe5e9ae715)


Eficiência da Produção: Análise detalhada das horas produtivas versus horas paradas.<br>
Qualidade da Produção: Avaliação da qualidade, mostrando o percentual de peças aprovadas.<br>
Desempenho por Operador: Comparação do desempenho entre os operadores.<br>
Análise Temporal: Visualizações das métricas ao longo do tempo para identificar tendências e padrões.<br>

# Principais Métricas Analisadas
Horas Trabalhadas: Soma total de horas trabalhadas. <br>
Horas Produtivas: Total de horas em que não houve ocorrência (horas produtivas). <br>
Horas Paradas: Diferença entre horas trabalhadas e horas produtivas.<br>
% Produtividade: Razão entre horas produtivas e horas trabalhadas.<br>
% Qualidade: Percentual de peças aprovadas sobre o total produzido.<br>
Total de Peças Produzidas: Soma de peças aprovadas e rejeitadas.<br>

# Regras de Negócio
Ocorrência: Se houve ocorrência, considera-se como hora parada. Se não houve ocorrência, considera-se como hora produtiva. <br>
Total Horas Produtivas: CALCULATE(SUM('BaseProdução'[Total Horas]), 'BaseProdução'[Ocorrência] = BLANK()) <br>
Horas Paradas: Total de Horas Trabalhadas - Horas Produtivas<br>
% Produtividade: (Horas Produtivas / Horas Trabalhadas) * 100<br>
% Qualidade: (Total de Aprovados / Total Produzido) * 100<br>
Total de Peças Produzidas: Aprovadas + Rejeitadas<br>




# Tecnologias Utilizadas

Power BI: Ferramenta principal para visualização de dados e criação do dashboard.<br>
Excel: Utilizado para armazenar e manipular a base de dados.<br>
DAX (Data Analysis Expressions): Linguagem de expressão utilizada no Power BI para cálculos e medidas.<br>
