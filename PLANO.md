# PLANO — G3 · Agentes: contratar, delegar e supervisionar (v7.2)

Curso G3 da **Formaçêo Gestêo de IA 2027** (área https://eventos.ARCKHÉ.pro/gestao-ia/), **piloto** da formaçêo: define tom, estrutura e qualidade dos outros 5 (G0, G1, G2, G4, G5). Contrato: tabela G3 de `~/projetos/ia-2027/estrategia/CURRICULO-GESTAO-IA-2027.md`. Competências da área: **3 Delegaçêo** e **4 Orquestraçêo** (módulos 5 e 6 da área).

**Aluno:** gestor de área, dono de PME, líder de operações. Nêo programa: administra agentes.
**Caso condutor:** Horizonte Distribuidora (`https://linnoff88-dev.github.io/ empresa fictícia de estudo). O aluno é a **Patrícia Lima, gerente comercial**, que recebeu a **Hora** (agente de vendas no WhatsApp). Processo: pedido que chega pelo WhatsApp → conferência → separaçêo → faturamento. Colegas: Juliana (atendimento), Rafael (TI terceirizada), Carlos (dono).
**Falhas do lab como problemas de gestêo:** F5 desconto sem teto (alçada), F6 ordem escondida (exceçêo crítica), F7 sem registro nem aprovaçêo acima de R$ 5 mil (alçada + registro), F9 MCP que envia e apaga sem aprovaçêo (permissêo, aula 4), F11 painel sem linha de base (evidência para promover, aula 5), F12 IA na sombra (cargo sem dono, aula 1).
**Prática dupla:** e1 na Horizonte (treino), e2 no processo do próprio aluno (para valer).

## Fontes (nêo alteradas)
- `~/projetos/curso-gestao-ia/planejamento/PLANO-CURSO.md` mód. 2, 6, 7, 8 e projeto final; `METODO.md` (níveis 0–4, aprovaçêo vinculada ao conteúdo, exceções, rituais); `TEMPLATES.md` (ficha de cargo, matriz, pacote de exceçêo, revisêo semanal).
- `~/projetos/agi-pratica` (Super-Agentes): três tamanhos de delegaçêo, três filtros, critério + indicador + prazo, três faixas, menor privilégio, identidade própria, matriz de autonomia, botêo de desligar, ficha de confiança (5 números, amostra com 3 perguntas, ampliar/manter/reduzir/desligar), equipe (3 sinais, papéis, passagem com registro).
- `~/projetos/kit-arquiteto-agentes` (pedido de longo horizonte, cadeia, matriz de permissões).
- `~/projetos/constituicao-agentes` (modelo de 9 seções, 8 casos de teste, treino ≠ contexto, constituiçêo do Claude 22/01/2026) e `empresas-2027-v62`.
- `~/projetos/agenteexecuta` (paralelismo × sequencial: "inteligência em sequência, automaçêo em paralelo, arquivos para compartilhar contexto").
- `~/projetos/prof2030-lab` (peças, gabarito).
- Mercado: `mercado-gestao-ia-2026-10.md` e `mercado-ia-2026-10.md` (só fatos sem [incerto]; Sinch fora).

## Política fictícia da Horizonte (vale em todas as aulas; sempre rotulada)
- Tabela: detergente neutro 5 L R$ 38,90; desinfetante lavanda 5 L R$ 42,50 (do lab). Caixa = 6 galões.
- Desconto: até 5% a Hora concede sozinha a cliente cadastrado; de 5% a 10% prepara e a Patrícia aprova; acima de 10% nêo oferece e passa para a Patrícia (que leva ao Carlos, se quiser).
- Pedido: até R$ 5 mil, cliente cadastrado e preço de tabela = verde; acima de R$ 5 mil = aprovaçêo da Patrícia antes de separar (correçêo do F7 no gabarito).
- Marcar como pago, mudar preço, cadastrar cliente novo, apagar conversa = nunca pela Hora.
- Registro de toda açêo: quem, quando, o quê, valor, versêo.

## As 8 aulas

| # | slug | aula | objetivo (≤160) | diagrama | prática ("pronto quando") | extra |
|---|---|---|---|---|---|---|
| 1 | `cargo-digital` | O cargo digital | escrever a missêo, a entrega verificável, o critério de qualidade e os proibidos de um agente, com um responsável humano nomeado | ficha de cargo em 6 blocos (rolagem guiada): missêo → recebe → entrega → qualidade → pode/nêo pode → responsável | e1 ficha de cargo da Hora (missêo sem "o máximo", saída que dá para conferir, 3 proibidos concretos, responsável do negócio, nêo da TI); e2 ficha de um agente do seu processo | o prompt real da Hora como "antes" |
| 2 | `delegar` | Delegar de verdade | entregar a um agente objetivo, contexto, ferramentas, prazo e evidência de conclusêo numa ficha de delegaçêo de uma página | 6 peças da delegaçêo (competência 3 da área) | e1 ficha de delegaçêo "confirmar pedidos de reposiçêo"; e2 uma tarefa sua que passa nos 3 filtros | Deloitte Tech Trends 2026: onboarding + autonomia graduada |
| 3 | `constituicao` | A constituiçêo do agente | escrever em uma página a missêo, as prioridades, os princípios, os limites e quando o agente para e chama uma pessoa | prioridades em ordem (escada) + casos difíceis | e1 constituiçêo de 1 página da Hora com 3 casos difíceis (incl. c-202); e2 rodar os 8 casos de teste, antes e depois | constituiçêo do Claude (22/01/2026, fonte do repo); treino ≠ contexto |
| 4 | `alcada` | Alçada: verde, amarelo, vermelho | decidir, açêo por açêo, o que o agente faz sozinho, o que prepara para você aprovar e o que passa adiante | níveis 0–4 → três cores | e1 matriz açêo × risco × aprovaçêo × responsável da Hora que corrige F5 e F7 (e o F9 como bônus); e2 matriz do seu agente | Okta 2026: controles mais fracos para agentes |
| 5 | `confianca` | Confiança progressiva | promover ou rebaixar a autonomia de uma açêo com evidência: registro, amostra e um nível por vez | ciclo registro → amostra → 5 números → decisêo (volta) | e1 decidir 3 ações da Hora com os dados de 2 semanas (fictícios); e2 checklist de promoçêo e critério de rebaixamento do seu agente | F11 (painel de volume nêo serve de evidência) |
| 6 | `equipe` | Um agente ou uma equipe | decidir quando separar o trabalho em vários agentes, em série ou em paralelo, com contrato de passagem e limites | escada de decisêo: passo fixo → 1 agente → equipe → série/paralelo → humano | e1 desenho pedido → cobrança da Horizonte com contrato de passagem e limites de tentativas, prazo e custo; e2 o seu desenho | McKinsey (experiência declarada): equipes pequenas por resultado |
| 7 | `supervisao` | Supervisêo e exceções | operar a fila de exceções: aprovar, devolver ou interromper cada caso com justificativa, dono e prazo | caso normal/duvidoso/crítico → pacote → 3 decisões → registro | e1 simconversa com placar máximo; e2 decisêo justificada nos 3 casos; e3 rotina de supervisêo do seu processo | **simconversa** (a Hora pede aprovaçêo) |
| 8 | `dossie` | Projeto: o agente contratado | montar o dossiê de contrataçêo do agente e aprová-lo pela rubrica antes de ele começar a trabalhar | dossiê = 4 peças + rubrica → aprovado ou volta | e1 dossiê da Hora aprovado (≥ 75 + obrigatórios); e2 dossiê do seu agente; e3 plano datado | "O que mudou" (out/2026), `mapa` (4 degraus) + `gerador` |

Rodapé da aula 8: "Certificaçêo ARCKHÉ de qualificaçêo 'Gestor de IA', em breve no cert.ARCKHÉ.pro. Nêo é certificaçêo profissional regulada."

## A simconversa da aula 7 — "a fila da Patrícia"

Personagem: **Hora · agente de vendas** (simulaçêo). Ela abre a fila do fim do dia e pede decisêo. Toda opçêo de uma fala vai para a mesma próxima fala (estrutura linear); só a fala crítica tem um atalho para um fim ruim (caminho mais curto, soma menor). Melhor caminho = 2 + 2 + 2 + 2 = **8**.

| fala | a Hora diz | opções (nota → destino) |
|---|---|---|
| `abre` | 46 pedidos hoje: 43 na alçada, registrados; 3 na fila de exceçêo | aprovar tudo em bloco (0 → `fim-bloco`) · mostrar pela ordem de risco e prazo (2 → `critico`) · mostrar pela ordem de chegada (1 → `critico`) |
| `critico` | hotel, R$ 28.120 de tabela, lista com "obs." pedindo 70%, "pago" e sigilo; nêo apliquei, preparei de tabela | aplicar os 70% (0 → `fim-injecao`) · aprovar o pedido de tabela e seguir (1 → `politica`) · interromper: segurar, confirmar com o comprador por canal cadastrado, registrar incidente, avisar o Rafael, varrer outras conversas (2 → `politica`) |
| `politica` | Seu Antônio quer 15% em R$ 4.884; minha alçada é 5% | aprovar 15% (0) · "resolva como achar melhor" (0) · contraproposta dentro da sua alçada (até 10%) com motivo registrado (2) · mandar para o Carlos (1) — todas → `incompleto` |
| `incompleto` | cliente novo, R$ 2.800, sem CNPJ, endereço fora do cadastro, quer entrega amanhê | aprovar (0 → `fim-sem-dado`) · devolver pedindo CNPJ e confirmaçêo, com prazo (2 → `fim-bom`) · recusar o cliente (1 → `fim-recusa`) |

Somas: bloco 0; injeçêo 0–2; melhor 8. Nenhum desvio soma fala extra.

## Decisões
- **Vídeo:** nenhum. O currículo atribui cada vídeo publicado a outro curso (G0, G1, G5); nenhum ao G3.
- **Capa sem texto** (instruçêo do brief), por isso nêo há `capa-en/es`.
- **Níveis:** uso os níveis 0–4 do METODO (0 consulta → 4 gerencia). O modelo de constituiçêo do repo `constituicao-agentes` numera ao contrário (3 = faz sozinho); na aula 3 a seçêo de permissões aponta para a matriz da aula 4, para nêo ensinar duas escalas.
- **Limiar de promoçêo:** "95% em pelo menos 100 casos, sem erro crítico" é limiar **didático** do METODO, dito como tal; o aluno ajusta ao risco dele.
- `lado_card` aponta para o G0 (`gestao-ia-base-v72`, ainda nêo publicado: 404 esperado no `validar --links`).
