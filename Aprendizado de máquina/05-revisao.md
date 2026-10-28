<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Questões de revisão — Registro individual

## Identificação

- Estudante ou equipe: Anna Beatriz Oki
- Turma: Ciência de Dados
- Data de realização: 28/10/2026
- Integrantes e contribuições (se em equipe): Atividade individual, realizada apenas por mim.

Responda com suas palavras e apresente os cálculos quando solicitados. Os números dos exercícios manuais não são os resultados do laboratório.

## 1. Explique a diferença entre regra programada para bloquear uma palavra e modelo de spam treinado com exemplos.

**Resposta:** Na regra, uma pessoa escreve à mão o que bloquear, e ela só pega o que foi previsto. O modelo aprende com mensagens já marcadas como spam ou não, descobre os sinais sozinho e pega casos novos, mas pode errar.

## 2. Por que codificar evadiu/permaneceu como 1/0 não transforma classificação em regressão?

**Resposta:** O que define o tipo é o significado do alvo, não o número. Evadiu e permaneceu são duas categorias, e 1 e 0 são só códigos. Regressão prevê uma quantidade, como reais ou minutos.

## 3. Uma biblioteca quer estimar empréstimos e descobrir perfis. Que tarefas correspondem a cada pergunta?

**Resposta:** Estimar empréstimos (um número) é regressão. Descobrir perfis de usuários, sem categorias prévias, é agrupamento (aprendizado não supervisionado).

## 4. O que são atributo, alvo e unidade de análise no laboratório educacional?

**Resposta:** Atributo é a informação usada para prever (frequência, nota e entregas até a semana 4). Alvo é o que se quer prever (evasão no fim do semestre). Unidade de análise é o que cada linha representa: um estudante fictício.

## 5. Por que calcular a mediana antes de dividir os dados pode invalidar a avaliação?

**Resposta:** Porque a mediana usaria informação do teste, que deixa de ser "novo". A avaliação fica otimista demais (vazamento de dados). A mediana deve ser calculada só no treino.

## 6. Em uma matriz didática com TN=80, FP=5, FN=10, TP=5, calcule acurácia e sensibilidade. O resultado é suficiente para aprovar o modelo?

**Resposta:** Acurácia = (80 + 5) ÷ 100 = **0,85**. Sensibilidade = 5 ÷ (5 + 10) = 5 ÷ 15 ≈ **0,33**. Não é suficiente: 85% parece bom, mas o modelo acha só 1 em cada 3 que evadem. É preciso olhar os falsos negativos e comparar com uma referência.

## 7. Valores reais 100, 120, 140 e previsões 110, 115, 130. Calcule MAE e informe a unidade se o alvo for vendas em reais.

**Resposta:** Os erros absolutos são |100−110| = 10, |120−115| = 5 e |140−130| = 10. MAE = (10 + 5 + 10) ÷ 3 = 25 ÷ 3 ≈ **8,33 reais**.

## 8. Um R² de -0,2 significa “20% de acertos negativos”? Explique.

**Resposta:** Não. R² não é porcentagem de acertos. Um R² negativo quer dizer que o modelo está pior do que sempre prever a média.

## 9. Uma árvore tem acurácia 1,00 no treino e 0,65 na validação. Que hipótese investigar e como?

**Resposta:** A hipótese é sobreajuste: a árvore decorou o treino. Para investigar, comparar treino e validação com validação cruzada e limitar a profundidade ou aumentar a folha mínima, vendo se a validação melhora.

## 10. Por que escolher a profundidade pelo teste prejudica a estimativa final?

**Resposta:** Porque o teste deixa de ser dado não visto, e a acurácia final fica otimista. A escolha deve usar treino e validação, e o teste só no final.

## 11. Baixa frequência associada à evasão demonstra causa? Proponha explicação alternativa.

**Resposta:** Não, só mostra associação. Uma explicação alternativa é o estudante ter problema de trabalho ou de transporte, que causa a baixa frequência e também a evasão.

## 12. Um modelo sinaliza um estudante como possível evasão. Que ação responsável pode ser adotada?

**Resposta:** Uma pessoa da equipe revisa o caso e faz um convite voluntário de apoio (monitoria, orientação), sem punição nem decisão automática. O estudante pode recusar e contestar a indicação.

## Fontes adicionais consultadas

Material da disciplina e notebook de apoio. O uso de IA está declarado no arquivo 06 (autoavaliação).

[Voltar ao início](README.md).
