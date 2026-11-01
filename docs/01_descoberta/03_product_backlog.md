# PRODUCT BACKLOG

## 1. Product Backlog Itens

> O objetivo desta tarefa é elaborar a versão preliminar do backlog do produto, contendo dez funcionalidades que atendam às necessidades do usuário. Utilize os modelos de tabela a seguir.

| #   | Persona (Quem) | Dor/Necessidade (Por Quê) | Expectativa (Para Quê) | Funcionalidade (O Quê - Ação) |
| --- | -------------- | ------------------------- | ---------------------- | ----------------------------- |
| F1  | Carlos (Gestor de Manutenção) | Não tem uma lista confiável dos equipamentos, que ficam em planilhas e papéis diferentes | Ter todos os equipamentos organizados em um só lugar | Cadastrar, editar e consultar equipamentos com dados como tipo, localização, data de aquisição e situação |
| F2  | Ana (Operadora de Equipamentos) | Não sabe como avisar sobre um problema e o aviso verbal se perde | Comunicar o problema de forma simples e acompanhar o chamado | Registrar solicitação de manutenção corretiva informando o equipamento, a descrição e a urgência do problema |
| F3  | Carlos (Gestor de Manutenção) | Perde datas de revisão por controlar tudo manualmente | Planejar as revisões com antecedência e evitar quebras | Agendar manutenções preventivas, definindo equipamento, data e periodicidade de repetição |
| F4  | Marcos (Técnico de Manutenção) | Perde tempo procurando o que já foi feito antes em cada equipamento | Consultar rapidamente o histórico antes de atender o chamado | Consultar o histórico de manutenções de um equipamento, com filtros por período e tipo de serviço |
| F5  | Carlos (Gestor de Manutenção) | Só descobre que uma revisão venceu depois que o equipamento falha | Ser avisado a tempo de agir | Receber alertas de manutenções próximas do vencimento e atrasadas |
| F6  | Carlos (Gestor de Manutenção) | Não consegue justificar nem controlar os gastos com reparos | Decidir com base em dados e reduzir custos | Gerar relatório de custos de manutenção por equipamento e por período |
| F7  | Carlos (Gestor de Manutenção) | Não sabe quais equipamentos quebram com mais frequência | Identificar equipamentos problemáticos e decidir sobre reparo ou troca | Gerar relatório de frequência de falhas por equipamento |
| F8  | Carlos (Gestor de Manutenção) | Distribui os chamados de forma desorganizada e não sabe o andamento de cada um | Garantir que todo chamado tenha um responsável e prazo | Atribuir chamados a técnicos e acompanhar o status (aberto, em andamento, concluído) |
| F9  | Marcos (Técnico de Manutenção) | Precisa refazer em papel as anotações do serviço depois de executá-lo | Registrar o trabalho feito de forma rápida e sem retrabalho | Registrar a execução do serviço, informando descrição, peças utilizadas, custo e tempo gasto |
| F10 | Carlos (Gestor de Manutenção) | Informações de manutenção podem ser vistas ou alteradas por qualquer pessoa | Controlar quem pode ver e alterar cada informação | Autenticar usuários e controlar o acesso por perfil (gestor, técnico e operador) |

## 2. Revisão Técnica, UX e Negócios

> Avalie as funcionalidades listadas na tabela anterior com base em quatro perspectivas: Valor para o Negócio, Esforço Técnico de Implementação, Experiência do Usuário (UX) e Nível de Confiança (O quê / Como).

**Métricas:**

- **Valor de Negócio:** `$` (Baixo) a `$$$` (Alto)
- **Esforço Técnico:** `E` (Baixo) a `EEE` (Alto)
- **Valor UX:** ❤️ (Baixo) a ❤️❤️❤️ (Alto)
- **Confiança:** 🟢 (Alto), 🟡 (Médio), 🔴 (Baixo)

| #       | Esforço Técnico | Valor UX | Valor de Negócio | Nível de Confiança (O que/Como) |
| :------ | :-------------- | :------- | :--------------- | :------------------------------ |
| **F1**  | E               | ❤️❤️     | $$$              | 🟢 Alto/Alto                    |
| **F2**  | EE              | ❤️❤️❤️   | $$$              | 🟢 Alto/Alto                    |
| **F3**  | EE              | ❤️❤️     | $$$              | 🟡 Alto/Médio                   |
| **F4**  | E               | ❤️❤️     | $$               | 🟢 Alto/Alto                    |
| **F5**  | EEE             | ❤️❤️❤️   | $$$              | 🟡 Alto/Médio                   |
| **F6**  | EEE             | ❤️❤️     | $$$              | 🟡 Alto/Médio                   |
| **F7**  | EE              | ❤️❤️     | $$               | 🔴 Médio/Baixo                  |
| **F8**  | EE              | ❤️❤️     | $$               | 🟢 Alto/Alto                    |
| **F9**  | EE              | ❤️❤️     | $$$              | 🟢 Alto/Alto                    |
| **F10** | EE              | ❤️❤️     | $$               | 🟢 Alto/Alto                    |

### Justificativas

> Justifique a análise da tabela acima para cada funcionalidade, explicando a racionalidade por trás das métricas atribuídas.

- **F1:** Esforço baixo, pois é um cadastro simples com poucos campos. O valor de negócio é alto porque todas as outras funcionalidades dependem de ter os equipamentos registrados. A equipe tem alta confiança no que e no como fazer.
- **F2:** Esforço médio, pois envolve formulário, vínculo com o equipamento e definição de urgência. O valor de UX é alto porque resolve a maior dor do operador, que hoje não tem como avisar. O valor de negócio é alto porque é a porta de entrada das manutenções corretivas.
- **F3:** Esforço médio por conta da regra de periodicidade e da criação das próximas ocorrências. Gera alto valor de negócio por ser a base da manutenção preventiva. A confiança no como é média porque as regras de repetição ainda precisam ser validadas com usuários.
- **F4:** Esforço baixo, pois é uma consulta sobre dados já registrados. O valor de negócio é médio, pois apoia a decisão do técnico, mas não gera sozinho economia direta. Depende dos registros feitos em F9.
- **F5:** Esforço alto, pois exige rotina automática de verificação e envio de notificações. Tem alto valor de UX e de negócio porque é o diferencial em relação a planilhas e evita atrasos. A confiança no como é média, já que o canal de envio (e-mail, notificação no sistema) ainda será definido.
- **F6:** Esforço alto por envolver cálculos, agrupamentos e filtros por período. O valor de negócio é alto porque permite controlar e justificar os custos. A confiança é média porque o formato ideal do relatório ainda deve ser validado com o gestor.
- **F7:** Esforço médio, pois precisa contar ocorrências por equipamento e por período. O valor de negócio é médio. A confiança é baixa porque ainda não está claro como definir "falha" e quais indicadores o gestor considera úteis.
- **F8:** Esforço médio, pois envolve atribuição, mudança de status e listagem por responsável. O valor de negócio é médio, pois melhora a organização da equipe. A equipe conhece bem esse tipo de fluxo, por isso a confiança é alta.
- **F9:** Esforço médio, pois reúne vários campos de registro (peças, custo e tempo). O valor de negócio é alto porque alimenta o histórico e os relatórios. A confiança é alta.
- **F10:** Esforço médio por envolver autenticação e perfis de acesso. O valor de negócio é médio, pois protege as informações, e a equipe tem experiência com esse tipo de funcionalidade.

## 3. Product Backlog Itens (priorizado)

> Liste os itens do backlog do produto, priorizados conforme as regras do sequenciador vistas em aula. Ordene-os da maior para a menor prioridade dentro de cada onda.

**Regras do Sequenciador:**

- **Regra 1:** Uma onda pode conter, no máximo, três funcionalidade.
- **Regra 2:** Uma onda não pode conter mais de uma funcionalidade em vermelho.
- **Regra 3:** Uma onda não pode conter três funcionalidades em amarelo e vermelho.
- **Regra 4:** A soma de esforço dos cartões não pode ultrapassar cinco Es.
- **Regra 5:** A soma de valor dos cartões de uma onda não pode ser menos de quatro $s e quatro corações.
- **Regra 6:** Se um cartão depende de outro cartão, esse outro deve estar em alguma onda anterior.

| #       | Esforço<br>Técnico | Valor<br>UX | Valor de<br>Negócio | Nível de Confiança <br> (O que/Como) | Depende de | Onda |
| :------ | :----------------- | :---------- | :------------------ | :----------------------------------- | :--------- | ---- |
| F1      | E                  | ❤️❤️        | $$$                 | 🟢 Alto/Alto                         | -          | 1    |
| F10     | EE                 | ❤️❤️        | $$                  | 🟢 Alto/Alto                         | -          | 1    |
| F2      | EE                 | ❤️❤️❤️      | $$$                 | 🟢 Alto/Alto                         | F1         | 2    |
| F3      | EE                 | ❤️❤️        | $$$                 | 🟡 Alto/Médio                        | F1         | 2    |
| F9      | EE                 | ❤️❤️        | $$$                 | 🟢 Alto/Alto                         | F2         | 3    |
| F8      | EE                 | ❤️❤️        | $$                  | 🟢 Alto/Alto                         | F2         | 3    |
| F4      | E                  | ❤️❤️        | $$                  | 🟢 Alto/Alto                         | F9         | 4    |
| F5      | EEE                | ❤️❤️❤️      | $$$                 | 🟡 Alto/Médio                        | F3         | 4    |
| F6      | EEE                | ❤️❤️        | $$$                 | 🟡 Alto/Médio                        | F9         | 5    |
| F7      | EE                 | ❤️❤️        | $$                  | 🔴 Médio/Baixo                       | F9         | 5    |

> **Conferência das regras por onda:** Onda 1 (F1, F10): 3 Es, 5 $s e 4 corações. Onda 2 (F2, F3): 4 Es, 6 $s e 5 corações. Onda 3 (F9, F8): 4 Es, 5 $s e 4 corações. Onda 4 (F4, F5): 4 Es, 5 $s e 5 corações. Onda 5 (F6, F7): 5 Es, 5 $s e 4 corações, com apenas uma funcionalidade em vermelho. Todas as dependências estão em ondas anteriores.

## 4. Especificação Suplementar de Requisitos Não Funcionais

> Especifique os requisitos não funcionais do produto de software, certificando-se de que atendam aos critérios SMART.

| Requisito não-funcional | Descrição                                                                                                 | Categoria       | Prioridade |
| :---------------------- | :-------------------------------------------------------------------------------------------------------- | :-------------- | :--------- |
| RNF.1                   | O tempo de resposta para consultas ao histórico de manutenções de um equipamento não deverá exceder 3 segundos para até 5.000 registros | Desempenho      | Alta       |
| RNF.2                   | O produto de software deverá ser compatível com os navegadores Chrome (versão >= 100) e Edge (versão >= 100).                           | Suportabilidade | Alta       |
| RNF.3                   | O sistema deverá estar disponível pelo menos 99% do tempo no horário comercial (08h às 18h), medido mensalmente.                         | Confiabilidade  | Média      |
| RNF.4                   | As senhas dos usuários deverão ser armazenadas com hash e o acesso às funcionalidades deverá respeitar o perfil do usuário (gestor, técnico ou operador). | Segurança       | Alta       |
| RNF.5                   | Um usuário sem treinamento deverá conseguir abrir uma solicitação de manutenção em até 2 minutos e no máximo 5 cliques.                  | Usabilidade     | Alta       |
| RNF.6                   | Os alertas de manutenção deverão ser gerados com antecedência configurável de 1 a 30 dias e disponibilizados em até 5 minutos após a geração. | Confiabilidade  | Média      |

---

[⬅ Anterior](01_visao_do_produto.md) | [Próximo ➡](99_video_etapa_1.md)
