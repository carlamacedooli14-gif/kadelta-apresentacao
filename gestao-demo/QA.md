# Verificações do protótipo Kadelta Gestão

Testes do painel estático, executados com Chromium + Playwright via injeção de conteúdo (o ambiente restringe navegação de testes para arquivo/localhost).

- [x] JavaScript validado com `node --check`.
- [x] Layout desktop 1440×900; tablet 820×1100; celular 390×844; celular compacto 320×700.
- [x] Sem erro de JavaScript nos testes principais.
- [x] Sem rolagem horizontal na página principal nas quatro larguras.
- [x] Navegação por menu lateral e menu mobile.
- [x] Carteira: 10 oportunidades fictícias, pesquisa por nome, empresa com duas oportunidades.
- [x] Ficha: abrir, consultar diagnóstico, navegar por abas e fechar.
- [x] Funil: 7 etapas renderizadas.
- [x] Cadastro demonstrativo manual gera nova oportunidade.
- [x] Atualização do diagnóstico preenche 6 de 6 campos de referência.
- [x] Alteração de etapa comercial gera evento no histórico.
- [x] Visão de representante filtra a carteira de terceiros.
- [x] Importação de resumo no formato da apresentação funciona.
- [ ] Envio real de dados / login / Supabase **não implementados por decisão de escopo**.
- [ ] Persistência em `localStorage` em recarga real não foi testada no Chromium deste ambiente (navegação bloqueada para localhost e arquivos); lógica de salvamento implementada e verificada por inspeção.
- [ ] GitHub Pages deve ser conferido separadamente após publicação.

Aviso: a troca de perfil no navegador não protege os dados. Para uso real, a implementação futura deve usar autenticação e controle de acesso no banco, incluindo RLS.