# Kadelta — Diagnóstico Adaptativo (versão 1)

Uma apresentação comercial exploratória, responsiva e baseada em regras. O representante começa pelo **setor**, investiga **sintomas** da operação, identifica uma prioridade, dimensiona o custo de manter o processo durante **mais 30 dias**, considera **soluções combinadas**, conhece **pesquisas reais**, apresenta o **Método Δ** e produz um **pré-diagnóstico**.

## Como publicar

Os arquivos `index.html`, `styles.css`, `app.js` e `favicon.svg` ficam na raiz do repositório GitHub Pages. Não há build, dependência JavaScript nem backend. A página funciona com recursos locais, mas a fonte Google pode ser carregada quando houver internet.

## O que está implementado

- 9 etapas acessíveis via desktop e celular.
- 10 setores com exemplos genéricos por operação.
- 9 sintomas multi-seleção; perguntas condicionais de acordo com o sintoma principal.
- Recomendações **hipotéticas** entre agente de IA, dashboard, integração, automação, sistema e MVP. É possível selecionar múltiplas soluções.
- Visualização de **antes e depois** dinâmica conforme sintoma prioritário e combinação de soluções, explicitamente identificada como ilustração.
- Cenário de mais 30 dias baseado exclusivamente em valores informados na conversa. Há caminho sem números.
- Referências de 2026 verificáveis e com avisos de limite.
- Guia de fala para representantes.
- Resumo copiável, baixável como TXT e imprimível em PDF.
- Exemplo fictício isolado de contatos reais; botão reiniciar.

## Limites e cuidados

Este é um **protótipo de apresentação**, não um CRM. **Nenhuma informação é enviada, gravada em servidor, armazenada localmente ou partilhada automaticamente.** Contato e empresa são opcionais e ficam apenas na sessão da página. O resumo poderá ser copiado ou baixado, sob ação do usuário. Para cadastro no CRM serão necessários autenticação, permissões, banco de dados, consentimento e regras de atribuição do representante.

Os cálculos não garantem economia ou venda: custo equivalente das horas é **capacidade comprometida**, não necessariamente despesa incremental. Em vendas, o cenário depende de hipóteses de conversão e margem. Não somar cenários sem comprovar que são independentes.

Estudos citados: 
- McKinsey *The State of AI 2026*: https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai
- Microsoft *Work Trend Index 2026*: https://www.microsoft.com/en-us/worklab/work-trend-index/agents-human-agency-and-the-opportunity-for-every-organization
- NBER *Generative AI at Work* (2023): https://www.nber.org/papers/w31161
- Gartner previsão 2025: https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027

## Próxima versão

- Catálogo de agentes configurado no backend por versão aprovada.
- Fichas de produto específicas para cada setor/dor (incluindo implantação, escopo, riscos e exemplo autorizado).
- Identificação de representantes, empresa, contato e oportunidade sem duplicatas.
- Motor de perguntas administrável pela equipe, com testes de aceitação.
- Login, RBAC/RLS, CRM, rastreio de origem, histórico da negociação e controle de LGPD.