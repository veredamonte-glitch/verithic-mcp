# Verithic MCP connector

Verithic answers one question with public data: which town to live in, near Barcelona or in the Community of Madrid. This connector gives an AI agent the same figures the website shows.

- Endpoint (Streamable HTTP, no key): https://verithic.com/api/public/mcp
- Docs and reuse terms: https://verithic.com/connector
- Official MCP Registry name: io.github.veredamonte-glitch/verithic

## What it returns

For 124 towns around Barcelona and 170 in the Community of Madrid: price per m² of second-hand homes (Notariado), median rent (Ministry of Housing, SERPAVI; around Barcelona also the Generalitat's registered contracts), property tax rate (Ministry of Finance), household income and population (INE), minutes to the centre and rent-cap zones (BOE).

Every figure comes with its source, its period and the date Verithic read it. If a source publishes nothing for a town, the value is null and the reason is given. Nothing is estimated.

In Madrid, minutes are by car with no traffic for now; public transport times are not read yet.

## Tools

13 read-only tools: ficha_municipio, comparar_municipios, listar_municipios, buscar_municipios, ranking_por_perfil, buscar_por_presupuesto, mas_por_menos, municipios_similares, calcular_mudanza, alquiler_ano_a_ano, precio_parada, zona_tensionada_2027 and metodologia_fuentes. Pass zona: "madrid" for Madrid and language: "en" for answers in English.

## Add it

In Claude, ChatGPT or any MCP client, add a remote connector with the endpoint above.

This repository only holds the public description of the connector (server.json). The website's code is not here.
