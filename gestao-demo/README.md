# Kadelta | Central comercial e gestão de diagnósticos — V1 demonstrativa

Protótipo visual e funcional para testar o comportamento comercial **após a apresentação adaptativa**. Interface responsiva em HTML, CSS e JavaScript, sem frameworks e sem backend.

## Páginas e ações existentes

- **Visão geral:** empresas únicas, oportunidades ativas, diagnósticos incompletos, retornos até hoje e sintomas recorrentes da base simulada.
- **Carteira:** pesquisa por empresa, contato, setor, sintoma ou solução; filtros de etapa e segmento; uma empresa pode ter várias oportunidades.
- **Diagnósticos:** ficha com problema relatado, sintomas, objetivo, fluxo atual, sistemas, linha de base, métrica de sucesso, responsável e restrições; índice de campos preenchidos, não indicador de qualidade.
- **Negociação:** quadro de etapas comerciais com movimentação simulada e histórico de mudanças; representantes acompanham, gestão atualiza.
- **Agenda:** retornos vencidos, do dia e futuros.
- **Representantes:** carteira por origem e número de contratos fictícios concluídos; NÃO calcula comissão.
- **Ficha individual:** quatro abas (Visão geral, Diagnóstico, Negociação, Histórico), notas, registro de contato, agendamento e impressão.
- **Importação:** cole ou envie o resumo `.txt` exportado pela última etapa da apresentação adaptativa.
- **Cadastro manual:** simule uma empresa, seu contato e a necessidade encontrada.
- **Troca de perfil:** demonstra visualmente diferenças entre gestor Kadelta e representantes.

## Segurança e limites

**Todos os exemplos iniciais são fictícios.** Os dados adicionados manualmente ficam no `localStorage` do próprio navegador e **não são transmitidos** para Supabase ou API. Não insira nome, WhatsApp, e-mail ou qualquer dado pessoal real em uma demonstração pública. Como não há autenticação, as restrições de perfil são apenas uma simulação de interface, **não são controle de acesso seguro**.

O visualizador público existe para aprovar a experiência antes de criar banco de dados, políticas de acesso, identidade, trilha auditável, tratamento de duplicidades, regras de atribuição, LGPD, e coleta adequada de consentimento/legítimo interesse conforme contexto.

## Integração demonstrativa com a apresentação

A apresentação pública terá um modo de teste opcional no endereço `/?demo=1`. Ao usar **Testar exemplo fictício** e chegar à última etapa, o botão **Enviar para gestão (simulação)** fará a passagem do resumo pelo `localStorage` para a rota `/gestao-demo/?from=presentation`. Esse recurso **não** é habilitado na apresentação normal. **Não utilizar o modo demo com dados reais**.

## Modelo proposto para Supabase (etapa seguinte)

Entidades: `profiles` / `representatives`, `companies`, `contacts`, `opportunities`, `opportunity_symptoms`, `opportunity_solutions`, `diagnoses`, `commercial_events`, `tasks`, `proposals`, `attributions`.

Regras importantes:

1. Companhia é única e pode ter várias oportunidades; decidir deduplicação por identificador fiscal quando legal e necessário, nome e canais, com revisão humana de conflitos.
2. Oportunidade retém representante de origem, sem atribuir comissão automaticamente.
3. Diagnóstico é versionado; diferenciar relatos, hipóteses, evidência e aprovação técnica.
4. Cálculos de horas / custos da apresentação são cenários com premissas, nunca perdas ou ROI comprovados.
5. Acesso autenticado com políticas RLS por papel e vínculo; gestão pode ler/editar o que precisa, representante vê apenas oportunidades autorizadas.
6. Não hospedar documentos privados e chaves em GitHub Pages; o site estático não faz autenticação por si só.

## Publicação

Arquivos do painel demonstrativo no repositório `carlamacedooli14-gif/kadelta-apresentacao` em `/gestao-demo/`. GitHub Pages publica a branch `main` pelo workflow já existente. Não utilizar esta implementação como CRM de produção.