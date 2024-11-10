# Projeto de Aplicações Distribuídas: Aprendizado Federado Simulado com Google Colab

Descrição do Projeto
Este projeto simula o Aprendizado Federado usando Python no Google Colab, demonstrando uma abordagem onde múltiplos clientes (nós) treinam um modelo de machine learning em dados locais. Em vez de compartilhar dados privados, cada nó treina localmente e compartilha apenas os parâmetros do modelo. O servidor central agrega os parâmetros recebidos de cada nó para formar um modelo global atualizado.

Esta abordagem é ideal para ambientes onde os dados não podem ser centralizados, como em sistemas médicos ou financeiros.

Estrutura do Projeto
O projeto simula uma rede de nós que treina um modelo de aprendizado distribuído. Abaixo estão os componentes principais:

- Inicialização dos Dados e Modelo: Cada nó inicia com um conjunto de dados exclusivo e uma cópia inicial do modelo.
- Treinamento Local em Cada Nó: Os nós executam o treinamento usando uma função que calcula os gradientes baseados nos dados locais.
- Agregação Centralizada dos Pesos: Após o treinamento, cada nó envia seus pesos atualizados ao servidor central, que os agrega para atualizar o modelo global.
- Redistribuição do Modelo Global: Após a agregação, o modelo global atualizado é redistribuído para cada nó, que usa os novos parâmetros para continuar o treinamento.

Estrutura do Código
O código é dividido em várias funções que executam as etapas de treinamento federado. As principais funções incluem:

- Função de Treinamento Local: Cada nó executa uma função de treinamento que usa os dados locais para ajustar o modelo. Isso evita o compartilhamento de dados entre os nós.

- Função de Agregação de Pesos: Essa função combina os pesos de todos os nós, calculando a média dos parâmetros para formar o modelo global. Este passo é essencial para o aprendizado federado.

- Função de Atualização Global: Após a agregação, os pesos globais são enviados de volta para os nós para que o processo de aprendizado continue.

Resultados
O projeto conseguiu simular a convergência do modelo usando aprendizado federado. As etapas de treinamento local e agregação permitiram que cada nó contribuísse para o modelo final sem a necessidade de compartilhar dados diretamente.

Limitações Observadas
Limitações de Tempo no Google Colab: A execução contínua é limitada pela infraestrutura do Colab, o que pode dificultar simulações mais longas.
Divisão Artificial de Dados: Os dados foram distribuídos manualmente para simular um cenário real; em implementações reais, os dados seriam naturalmente distribuídos entre os dispositivos.
Como Executar
Pré-requisitos
Para rodar o projeto, é necessário ter:

Conta no Google Colab para executar o notebook.
Conhecimentos básicos de Python e machine learning.
Passo a Passo
Carregar o Notebook: Abra o notebook no Google Colab.
Inicializar os Dados e o Modelo: Siga as instruções para carregar e dividir os dados entre os nós.
Treinamento Local: Execute o treinamento em cada nó.
Agregação de Pesos e Atualização: Acompanhe o processo de agregação central e distribuição dos pesos globais atualizados.
Estrutura do Repositório
notebook.ipynb: Contém o código principal do aprendizado federado simulado, com as funções de treinamento, agregação e atualização global.
README.md: Arquivo explicativo detalhando o projeto e como utilizá-lo.
