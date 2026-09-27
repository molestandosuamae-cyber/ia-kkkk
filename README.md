# ResolveAI — Gerador de Soluções com IA

MVP em HTML + CSS + JavaScript, preparado para Cloudflare Pages.

## O que já funciona

- Interface futurista e responsiva
- Campo para descrever qualquer problema
- Exemplos rápidos
- Geração de solução
- Histórico salvo no navegador
- Copiar solução
- Baixar solução em TXT
- Modo demonstração quando a API não está configurada
- Endpoint `/api/generate` preparado para Cloudflare Pages Functions + Workers AI

## Ativar IA real no Cloudflare

1. Crie um projeto no Cloudflare Pages usando este repositório/pasta.
2. O diretório `functions/` precisa estar na raiz do projeto.
3. No Cloudflare, abra:
   Workers & Pages > seu projeto > Settings > Bindings > Add > Workers AI.
4. Dê ao binding o nome `AI`.
5. Faça um novo deploy.
6. O frontend continuará chamando `/api/generate`; a Function usa `env.AI`.

O código usa o modelo `@cf/meta/llama-3.1-8b-instruct`.

## Importante

Não coloque chaves de API secretas no `app.js`. Neste MVP, a IA é chamada no servidor/Pages Function.

## Teste local

Com Wrangler instalado:

`npx wrangler pages dev . --ai AI`

A documentação do Cloudflare também permite configurar o binding no projeto e acessar `env.AI` dentro da Pages Function.

## Monetização futura

- Free: 1 solução por dia
- Pro: soluções ilimitadas
- Créditos: pacotes de gerações
- Templates premium
- Exportação para Excel/Google Sheets
- Conta de usuário + pagamentos
- Biblioteca de soluções
