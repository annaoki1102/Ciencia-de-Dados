<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# PBL integrador — Apoio à Permanência

## Identificação

- Estudante ou equipe: Anna Beatriz Oki
- Turma: Ciência de Dados
- Data de realização: 28/10/2026
- Integrantes e contribuições (se em equipe): Atividade individual, realizada apenas por mim.

## Contexto

Uma instituição quer compreender sinais associados à evasão e oferecer apoio antes do fim do semestre. Público-alvo: estudantes matriculados e equipe de apoio acadêmico. O cenário é didático e a prática usa dados sintéticos.

**Questão norteadora:** como identificar situações que merecem atenção e oferecer apoio, reconhecendo erros do modelo e dificuldades que os dados não capturam?

## Proposta da equipe

### 1. Delimitação

- Problema e público: Alguns estudantes abandonam o curso antes do fim do semestre. O público é formado por estudantes matriculados e pela equipe de apoio acadêmico.
- Decisão que o resultado pode apoiar: Quem convidar para um apoio voluntário antes do fim do semestre.
- Definição de evasão, unidade e horizonte: Evasão é o estudante deixar o curso antes do fim do semestre. A unidade é um estudante. A previsão é feita na semana 4, para o desfecho no fim do semestre.

### 2. Perguntas de negócio

1. Quais sinais observados até a semana 4 (frequência, nota e entregas) estão ligados à evasão no fim do semestre?
2. Dá pra usar uma árvore de decisão para apontar quem merece um convite de apoio, e que tipos de erro ela comete?

### 3. Dados necessários

| Dado | Papel no projeto | Disponível quando? | Origem pretendida | Necessidade e risco |
| --- | --- | --- | --- | --- |
| Frequência | Atributo | Semana 4 | Sistema acadêmico | Ajuda a prever. Pode refletir problemas fora do controle do estudante, como trabalho ou saúde. |
| Nota | Atributo | Semana 4 | Sistema acadêmico | Ajuda a prever. Pode faltar (30 ausências) e penalizar quem começa devagar. |
| Entregas | Atributo | Semana 4 | Ambiente virtual | Ajuda a prever. Varia entre disciplinas. |
| Evasão | Alvo | Fim do semestre | Registro de matrícula | Necessária para treinar. Só é conhecida no fim, e a definição pode variar (ex.: trancamento). |

Diferencie dados usados na simulação e dados que seriam necessários para uma investigação real: Na simulação usei só 3 atributos e o alvo, gerados por uma função. Numa investigação real seriam necessários dados reais de várias turmas, com autorização e proteção de dados (LGPD), definição clara de evasão e só os dados realmente necessários, evitando os sensíveis.

### 4. Abordagem e algoritmo

- Classificação, regressão ou outra formulação, com justificativa: Classificação, porque o alvo é uma categoria (evadiu ou permaneceu).
- Algoritmo introdutório escolhido: Árvore de decisão (profundidade 5, folha mínima 10), por ser simples e fácil de explicar.
- Referência simples: Sempre prever "permaneceu", a classe mais frequente.

### 5. Avaliação

- Preparação, divisão e validação: Mediana nas ausências, divisão estratificada de 75% treino e 25% teste (450 e 150) e validação cruzada de 5 partes só no treino.
- Métricas e razão da escolha: Acurácia comparada com a referência, e matriz de confusão com sensibilidade. A acurácia sozinha engana, e o erro mais grave é deixar de apoiar quem evadiu.
- Resultados efetivamente calculados e link da evidência: Acurácia no teste de 0,78 contra 0,5933 da referência, e sensibilidade de 0,69. Evidência em [03-aula2-laboratorio.md](03-aula2-laboratorio.md) e no notebook [notebooks/laboratorio-equipe.ipynb](notebooks/laboratorio-equipe.ipynb).
- Erros relevantes e consequências: 19 falsos negativos (evadiram sem convite), o erro mais grave. 14 falsos positivos (convite desnecessário), de baixo custo.

### 6. Limites e proteção

- Por que os resultados não demonstram causalidade? Os dados mostram associação, não causa. Tirar a nota piorou a previsão, mas isso não prova que ela causa a evasão. As relações vieram da simulação.
- Por que dados sintéticos não validam uso institucional? As relações foram escolhidas pela função que criou os dados e não vêm de estudantes reais. Por isso o desempenho não vale para uma instituição de verdade.
- Que grupos podem ser mal representados? Como investigar isso com evidências apropriadas? Estudantes que trabalham, com deficiência ou de grupos pequenos podem ficar mal representados. Dá pra investigar comparando os erros por grupo, com dados coletados com autorização. No conjunto sintético não há grupos reais, então não dá pra afirmar equidade.
- Como minimizar dados, restringir acesso e definir retenção? Usar só frequência, nota e entregas, sem nome nem matrícula. Acesso só para a equipe de apoio. Guardar só durante o semestre e depois apagar ou anonimizar.
- Como garantir revisão humana e contestação? O modelo só sugere. Uma pessoa da equipe revisa cada caso antes de qualquer contato. O estudante pode recusar o convite e contestar a indicação. Sem decisões automáticas nem punições.

### 7. Recomendações de apoio

- Ação voluntária proposta: Convite individual para conversar com a equipe de apoio acadêmico (orientação, monitoria, plano de estudos), sem obrigatoriedade.
- Como acolher estudantes não sinalizados pelo modelo: O modelo erra, então os serviços de apoio devem ser divulgados para toda a turma, e qualquer estudante pode pedir ajuda mesmo sem convite.
- O que precisa ser verificado antes de aplicação real: Testar com dados reais de várias turmas, avaliar por período (turmas futuras), comparar erros por grupo, ter aprovação de proteção de dados e planejar a revisão humana.

Previsões não são certezas. Priorize apoio e revisão humana, sem punições ou decisões automáticas prejudiciais.

## Apresentação de cinco minutos

| Tempo | Conteúdo | Responsável |
| --- | --- | --- |
| 1 minuto | Problema e dados | Anna Beatriz Oki |
| 2 minutos | Método e resultados | Anna Beatriz Oki |
| 1 minuto | Limitações | Anna Beatriz Oki |
| 1 minuto | Recomendações de apoio | Anna Beatriz Oki |

## Contribuições

| Integrante | Contribuição verificável |
| --- | --- |
| Anna Beatriz Oki | Atividade individual: preenchimento de todo o arquivo, com histórico nos commits do repositório. |

[Voltar ao início](README.md).
