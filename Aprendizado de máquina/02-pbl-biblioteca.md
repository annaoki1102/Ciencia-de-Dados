<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# PBL — Biblioteca em Foco

## Identificação

- Estudante ou equipe: Anna Beatriz Oki
- Turma: Ciência de Dados
- Data de realização: 20/10/2026
- Integrantes e contribuições (se em equipe): Atividade individual, realizada apenas por mim.

## Situação-problema

Uma biblioteca universitária enfrenta filas em horários específicos e baixa utilização de alguns serviços. A coordenação deseja melhorar o atendimento e planejar recursos. Este é um cenário didático.

**Público-alvo:** estudantes usuários, equipe de atendimento e gestão.

**Questão norteadora:** como os dados podem orientar o planejamento da biblioteca e a oferta de serviços sem identificar ou discriminar seus usuários?

## Investigação em equipe

1. Delimitem o problema e a decisão a apoiar.
2. Registrem o que já sabem e o que precisam investigar.
3. Formulem duas perguntas de negócio.
4. Definam a unidade de análise, os atributos e o alvo, quando houver.
5. Justifiquem a abordagem e indiquem se uma análise descritiva já seria suficiente.
6. Proponham avaliação, cuidados com os dados e limitações.

## Canvas da equipe

| Campo | Registro |
| --- | --- |
| Problema e decisão | A biblioteca tem filas em horários específicos e alguns serviços são pouco usados. A decisão é como organizar o atendimento e os recursos (horário da equipe, serviços oferecidos) para reduzir as filas e usar melhor os serviços. |
| Público-alvo | Estudantes que usam a biblioteca, equipe de atendimento e gestão. |
| O que sabemos | Existem filas em certos horários e alguns serviços têm pouco uso. A coordenação quer melhorar o atendimento e planejar os recursos. Este é um cenário didático, sem dados reais. |
| O que precisamos investigar | Em quais dias e horários as filas se formam. Quais serviços são pouco usados e por quê. Quantas visitas e empréstimos acontecem por período. Se o movimento muda em épocas do semestre, como semana de provas. |
| Pergunta de negócio 1 | Em quais dias e horários a biblioteca fica mais cheia, e como isso muda ao longo do semestre? |
| Pergunta de negócio 2 | Dá pra prever quantos empréstimos a biblioteca terá por semana, a partir do número de usuários ativos e das horas de abertura? |
| Unidade de análise e período | Uma semana de funcionamento da biblioteca, durante um semestre (ex.: 2026.2). Para a pergunta 1, também por faixa de horário dentro de cada dia. |
| Atributos, unidades e origem pretendida | Usuários ativos na semana (número de pessoas), horas de abertura na semana (horas) e semana do semestre (número). Origem: sistema de empréstimos e controle de acesso da biblioteca, e a tabela de horários de funcionamento. |
| Alvo e momento em que será conhecido, ou ausência de alvo | Pergunta 2: o alvo é o número de empréstimos por semana, conhecido só no fim da semana. A previsão seria feita antes, para planejar. Pergunta 1: sem alvo, é uma análise dos horários de maior movimento. |
| Abordagem e justificativa | Pergunta 1: análise descritiva, com gráficos de movimento por dia e horário. Pergunta 2: aprendizado supervisionado (regressão linear), porque o alvo é um número e existe histórico de semanas anteriores. |
| Alternativa sem ML | Usar a média de empréstimos por semana e por horário, em tabelas e gráficos. Já ajuda a decidir o horário da equipe sem precisar de modelo. |
| Como avaliar a proposta | Pergunta 2: separar os dados em treino e teste e medir o erro médio (MAE) em empréstimos por semana, comparando com uma referência simples que sempre prevê a média. Pergunta 1: conferir com a equipe da biblioteca se os horários apontados batem com o que eles observam. No fim, ver se a decisão tomada reduziu as filas. |
| Privacidade e limitações | Usar só dados agregados (contagens por semana ou horário), sem nome, matrícula ou histórico de usuário. Acesso restrito e guarda só pelo tempo necessário. Limitações: o cenário é didático e os dados são sintéticos, há poucas semanas de dados, o modelo mostra associação e não causa (mais horas de abertura não prova que geram mais empréstimos), e feriados ou greves podem distorcer os números. |

## Registro de colaboração

| Integrante | Papel | Contribuição |
| --- | --- | --- |
| Anna Beatriz Oki | Autora (atividade individual) | Definiu o problema, as perguntas, os atributos, a abordagem e a avaliação. |

## Conclusão da equipe

**Proposta:** Analisar os horários de maior movimento da biblioteca com gráficos e tabelas, e testar uma regressão linear para prever os empréstimos por semana a partir dos usuários ativos e das horas de abertura. Os dados seriam só agregados, sem identificar os usuários.

**Dúvida ainda aberta:** Não sabemos se poucas semanas de dados são suficientes para um modelo confiável, nem se fatores como provas, feriados e greves mudam muito a demanda.

**Feedback recebido e melhoria realizada:** Não recebi feedback de colegas nem da professora até a entrega. Revisei os campos para conferir se as perguntas, os dados e a avaliação combinavam entre si.

## Entrega

Canvas preenchido e síntese para apresentação de dois minutos. Avaliar coerência da pergunta, dados, abordagem, responsabilidade e colaboração. [Voltar ao início](README.md).
