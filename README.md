# MSB Calculator - Minecraft Server Benchmark

O **MSB Calculator** é uma ferramenta baseada em HTML e JavaScript para realizar benchmarks de servidores de Minecraft. Ela calcula o desempenho do servidor a partir de várias métricas de performance, como TPS (Ticks Per Second), MSPT (Milliseconds per Tick), Ping, número de Chunks carregados, e entidades ativas.

## Lógica do Cálculo

O cálculo da pontuação final do servidor é baseado em várias métricas essenciais para o desempenho de um servidor de Minecraft:

1. **TPS (Ticks Per Second)**
   - O **TPS** é uma medida de quantos "ticks" o servidor consegue processar por segundo. Normalmente, o ideal é manter o valor do TPS o mais próximo possível de 20 (o máximo suportado pelo Minecraft).
   - O cálculo considera a média dos valores de TPS de 1, 5 e 15 minutos, e atribui um peso de 35% no cálculo final.

2. **MSPT (Milliseconds per Tick)**
   - **MSPT** mede o tempo que o servidor leva para processar cada tick. Quanto menor for o valor de MSPT, melhor, pois significa que o servidor é mais eficiente.
   - O cálculo é feito levando em conta o valor médio e o valor máximo de MSPT, com um peso de 20% no cálculo final.

3. **Ping**
   - O **Ping** indica a latência entre o cliente e o servidor. Valores mais baixos indicam uma melhor performance de rede.
   - O cálculo leva em conta a média e o valor máximo de Ping, com um peso de 15%.

4. **Chunks Carregados**
   - O número de **Chunks carregados** influencia diretamente no desempenho, já que o servidor precisa processar os dados de cada Chunk.
   - Este valor é ponderado considerando a quantidade de TPS e a quantidade de Chunks, com um peso de 15%.

5. **Entidades Ativas**
   - O número de **Entidades ativas** (mobs, animais, etc.) também afeta o desempenho do servidor. Muitas entidades podem sobrecarregar o servidor.
   - A quantidade de entidades é calculada levando em consideração o número de TPS, com um peso de 15%.

## Tabela de Desempenho

Com base na média final, o servidor será classificado em uma das seguintes faixas de desempenho:

| Faixa de Pontuação | Classificação  | Feedback |
|--------------------|----------------|----------|
| 0 - 10             | Horrível       | Servidor quebrado, performance inaceitável. |
| 11 - 30            | Ruim           | Performance fraca, instabilidade e lag. |
| 31 - 50            | Regular        | Desempenho aceitável, mas com falhas ocasionais. |
| 51 - 70            | Bom            | Desempenho estável, algumas pequenas falhas. |
| 71 - 90            | Ótimo          | Desempenho excelente, sem grandes falhas. |
| 91 - 100           | Perfeito       | Desempenho impecável, servidor muito bem otimizado. |

## Como Usar

1. Clone ou baixe o repositório em sua máquina local.
2. Abra o arquivo `index.html` em seu navegador.
3. Insira as métricas de desempenho do seu servidor de Minecraft nos campos fornecidos:
   - **TPS (1 Minuto)**, **TPS (5 Minutos)**, **TPS (15 Minutos)**.
   - **MSPT (Média)** e **MSPT (Máximo)**.
   - **Ping (Média)** e **Ping (Máximo)**.
   - **Chunks Carregados** e **Entidades Ativas**.
4. Clique no botão **Calcular** para ver os resultados de desempenho e a classificação do seu servidor.

## Exemplo de Uso

### Resultados de Exemplo:

- **TPS Score**: 20.25
- **MSPT Score**: 12.34
- **Ping Score**: 15.67
- **Chunks Score**: 18.23
- **Entidades Score**: 10.50
- **Média Final**: 15.58 (Classificação: Ruim)

### Feedback:

O servidor está em uma faixa de **Ruim**, o que indica performance fraca com lag e instabilidade.

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

