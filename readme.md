# Sistema de simulação de atendimento de caixa da supermercado

### Tarefa da disciplina de Programação Paralela e Distribuída

1. Execute a simulação para µ = 5,0, σ = 0,5, N = 100 clientes e 1000 rodadas. Registre
a média e o desvio-padrão obtidos.
R: Para os valores dados, foram obtidos a média de 5 min e o desvio-padrão 0,05 min

2. Varie o número de caixas de 1 para 2 e 3. Compare os resultados obtidos e discuta
qualitativamente como mais caixas podem reduzir o tempo médio de atendimento.
R: Atualmente no sistema, a variação no número de caixas não impacta em nada no resultado. O aumento no número de caixas tem o potencial de diminuir o tempo médio de atendimento por meio da execução de simulações paralelas, uma vez que, quando há mais um caixa em serviço, deve ser possível que ambos funcionem simultaneamente, o que aumenta a eficiencia do sistema.

3. Varie σ (ex.: 0,25, 1,0, 2,0) e observe como a variabilidade impacta os resultados
médios.
R: Para a variação do desvio-padrão, foram obtidos os resultados abaixo, que demonstram que conforme o desvio padrão de entrada aumenta a precisão geral do sistema diminui. Com desvio-padrões mais baixos, o desvio-padrão das médias é cerca de um décimo da entrada e a média se mantem por volta dos 5min, já em casos com um valor maior na variável, os valores de saída se desviam desse padrão.
0,25 | µ: 5 min     | σ: 0,025 min
1,00 | µ: 5 min     | σ: 0,1 min
2,00 | µ: 5,004 min | σ: 0,198 min
5,00 | µ: 5,435 min | σ: 0,428 min
10,0 | µ: 7,011 min | σ: 0,733 min

4. Escreva um parágrafo explicando por que este simulador é considerado estocástico e
como isso representa situações reais.
R: Dado que estocástico é um processo aleatório com variáveis não previsíveis, mas que seguem a probabilidade. O simulador segue perfeitamente a definição, uma vez que, apesar de apresentar resultados consistentes em relação a média e desvio-padrão da média dos tempos de atendimento, tem como cerne do sistema o processo de RNG (Random Number Generation) dentro da classe SimulacaoCaixaSupermercado para a criação de uma amostra de uma distribuição normal padrão, um processo de geração aleatório. Essa técnica transforma o tempo de cada atendimento em um número semi-aleatório, o que representa situações reais onde, apesar de um tempo médio, um atendimento pode durar uma quantidade aleatória de tempo.