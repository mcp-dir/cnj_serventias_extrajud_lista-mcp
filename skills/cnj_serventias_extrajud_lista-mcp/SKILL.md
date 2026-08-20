---
name: cnj_serventias_extrajud_lista-mcp
description: Skill da REST API do Conselho Nacional de Justiça: Serventias Extrajudiciais (Lista) na MCP.AI: 1 endpoint em /api/cnj_serventias_extrajud_lista. Conselho Nacional de Justiça: Serventias Extrajudiciais (Lista), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Conselho Nacional de Justiça: Serventias Extrajudiciais (Lista) — REST API skill

Você tem acesso à **Conselho Nacional de Justiça: Serventias Extrajudiciais (Lista)** REST API na MCP.AI.

> Conselho Nacional de Justiça: Serventias Extrajudiciais (Lista), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/cnj_serventias_extrajud_lista
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/cnj_serventias_extrajud_lista/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"uf":"...","municipio":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/cnj_serventias_extrajud_lista/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `cnj_serventias_extrajud_lista_consultar`

Conselho Nacional de Justiça: Serventias Extrajudiciais (Lista), consulta em fonte oficial. _(POST /api/cnj_serventias_extrajud_lista/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `uf` | string | Sim | Parâmetro de consulta "uf". |
| `municipio` | string | Sim | Parâmetro de consulta "municipio". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_cnj_serventias_extrajud_lista` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
