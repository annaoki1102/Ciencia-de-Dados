<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Aula 1 — Conceitos e classificação de problemas

## Identificação

- Estudante ou equipe: Anna Beatriz Oki
- Turma: Ciência de Dados
- Data de realização: 19/10/2026
- Integrantes e contribuições (se em equipe): Atividade individual, realizada apenas por mim.

## Objetivos

Distinguir programação tradicional e Machine Learning, identificar atributos e alvo e diferenciar classificação, regressão e agrupamento.

## 1. Explicação com suas palavras

1. Como um modelo aprende com dados? O modelo aprende olhando muitos exemplos que já têm a resposta. Por exemplo, dados de estudantes (frequência, nota e entregas) e se ele evadiu ou permaneceu. Ele procura a relação entre esses dados e o resultado, e ajusta seus valores internos quando erra. Depois, usa o que aprendeu para prever casos novos, sem ninguém escrever as regras.
2. Qual diferença entre algoritmo e modelo? O algoritmo é o passo a passo que o computador segue para aprender, como a árvore de decisão. O modelo é o resultado desse aprendizado: o que sobra depois que o algoritmo treinou com os dados e que a gente usa para fazer previsões.
3. Compare uma regra de bloqueio de palavra com um modelo de spam. Na regra de bloqueio, uma pessoa escreve a regra à mão: se a mensagem tem tal palavra, bloqueia. Ela só pega o que já foi previsto e é fácil de driblar, basta trocar a palavra. No modelo de spam, ele aprende com mensagens já marcadas como spam ou não spam e descobre sozinho os sinais, então consegue pegar casos novos. Em compensação, ele pode errar e precisa de bons dados para treinar.
4. Dê um exemplo de atributo e alvo e defina o momento da previsão. Um exemplo é prever se um estudante vai evadir. Os **atributos** são a frequência, a nota e o número de entregas do estudante. O **alvo** é se ele evadiu ou permaneceu no fim do semestre. O **momento da previsão** é a semana 4, usando só o que já se sabe até ali, para dar tempo de oferecer apoio antes do fim do semestre.

## 2. Quadro comparativo

| Critério | Supervisionado | Não supervisionado |
| --- | --- | --- |
| Presença de alvo no treino | Sim, os dados já têm a resposta (rótulo) | Não, os dados não têm resposta |
| Pergunta que pode responder | "Qual será o resultado deste caso?" (ex.: vai evadir?) | "Que grupos ou padrões existem nos dados?" |
| Tipo de saída | Uma categoria ou um número | Grupos de dados parecidos |
| Tarefas e exemplo | Classificação (spam ou não) e regressão (prever vendas em reais) | Agrupamento (perfis de compra de clientes) |
| Dados necessários | Atributos e alvo conhecido | Só atributos, sem alvo |
| Forma de avaliação | Compara a previsão com a resposta real em dados de teste (acurácia, erro médio) | Não há resposta certa, então se avalia se os grupos fazem sentido |
| Limitação | Precisa de dados rotulados, que dão trabalho para conseguir | Difícil saber se o resultado está certo, e os grupos podem não ter significado |

## 3. Situações-problema

Os casos são cenários didáticos. Escolha **pelo menos cinco** e justifique sua classificação pelo significado do alvo ou por sua ausência.

| Caso | Situação-problema |
| --- | --- |
| 1 Educação | Prever evadiu/permaneceu com histórico rotulado de turmas anteriores. |
| 2 Saúde | Estimar o tempo de espera em minutos a partir de registros de atendimento. |
| 3 Comércio | Descobrir perfis de compra sem categorias prévias de clientes. |
| 4 Finanças | Prever inadimplente/adimplente com contratos e desfechos conhecidos. |
| 5 Segurança digital | Distinguir spam/legítima com mensagens já revisadas. |
| 6 Comércio | Estimar o total de vendas em reais na próxima semana. |
| 7 Educação | Agrupar perfis de acesso ao ambiente virtual sem rótulo de evasão. |
| 8 Saúde | Classificar exames em categorias previamente definidas por especialistas. |

| Caso escolhido | Alvo ou ausência de alvo | Categoria, quantidade ou grupos? | Abordagem e justificativa | Dados necessários e limitação |
| --- | --- | --- | --- | --- |
| 1 Educação | Alvo: evadiu ou permaneceu | Categoria | Supervisionada (classificação), porque há histórico de turmas com resposta conhecida | Frequência, notas e entregas das turmas anteriores. Pode não valer para turmas novas |
| 2 Saúde | Alvo: tempo de espera em minutos | Quantidade | Supervisionada (regressão), porque o alvo é um número | Registros de atendimento. Imprevistos, como dias de pico, não aparecem nos dados |
| 3 Comércio | Sem alvo | Grupos | Não supervisionada (agrupamento), porque não há categorias prévias de clientes | Dados de compras dos clientes. Os grupos precisam ser interpretados e podem não ter sentido |
| 5 Segurança digital | Alvo: spam ou legítima | Categoria | Supervisionada (classificação), porque as mensagens já foram revisadas e têm rótulo | Mensagens já revisadas. Golpistas mudam o texto, e o modelo pode bloquear mensagem legítima |
| 7 Educação | Sem alvo (sem rótulo de evasão) | Grupos | Não supervisionada (agrupamento), porque não há rótulo | Registros de acesso ao ambiente virtual. O grupo não diz se o estudante vai evadir |

## 4. Raciocínio crítico

“Detectar fraude” define sozinho o tipo de aprendizado? Compare o uso de exemplos rotulados e a busca de operações atípicas sem rótulos. Não. "Detectar fraude" é só o objetivo, e o tipo de aprendizado depende dos dados que existem. Se a empresa tem operações já marcadas como fraude ou não fraude, dá pra usar aprendizado **supervisionado**, e o modelo aprende com esses exemplos. Se não tem rótulos, dá pra usar aprendizado **não supervisionado** e procurar operações atípicas, que fogem do padrão. A diferença é que o supervisionado só reconhece o tipo de fraude que já viu, e o não supervisionado pode achar casos novos, mas também aponta operações diferentes que não são fraude.

## Entrega

Salve este arquivo preenchido. Critérios: distinção conceitual, pertinência dos dados, justificativa e clareza. [Voltar ao início](README.md).
