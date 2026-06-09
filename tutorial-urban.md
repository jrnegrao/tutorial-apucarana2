<!DOCTYPE html>  
<html lang="pt-BR">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Tutorial: Consulta de Viabilidade Econômica</title>  
    <style>  
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
        }  

        body {  
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;  
            line-height: 1.6;  
            color: #24292e;  
            background: #ffffff;  
            padding: 20px;  
            max-width: 900px;  
            margin: 0 auto;  
        }  

        h1 {  
            font-size: 2em;  
            border-bottom: 2px solid #0366d6;  
            padding-bottom: 10px;  
            margin-bottom: 10px;  
            color: #0366d6;  
        }  

        h2 {  
            font-size: 1.5em;  
            border-bottom: 1px solid #eaecef;  
            padding-bottom: 8px;  
            margin: 30px 0 15px 0;  
            color: #24292e;  
        }  

        h3 {  
            font-size: 1.2em;  
            margin: 20px 0 10px 0;  
            color: #24292e;  
        }  

        p {  
            margin-bottom: 15px;  
        }  

        ul, ol {  
            margin: 10px 0 15px 25px;  
        }  

        li {  
            margin-bottom: 5px;  
        }  

        a {  
            color: #0366d6;  
            text-decoration: none;  
        }  

        a:hover {  
            text-decoration: underline;  
        }  

        /* Índice */  
        .indice {  
            background: #f6f8fa;  
            border: 1px solid #eaecef;  
            border-radius: 8px;  
            padding: 20px 30px;  
            margin: 20px 0;  
        }  

        .indice ol {  
            margin: 0;  
        }  

        .indice li {  
            margin-bottom: 8px;  
            font-size: 1em;  
        }  

        /* Tip box */  
        .tip {  
            background: #f1f8ff;  
            border-left: 4px solid #0366d6;  
            padding: 12px 16px;  
            margin: 15px 0;  
            border-radius: 0 6px 6px 0;  
        }  

        .warning {  
            background: #fff8e1;  
            border-left: 4px solid #f9a825;  
            padding: 12px 16px;  
            margin: 15px 0;  
            border-radius: 0 6px 6px 0;  
        }  

        /* Tabelas */  
        table {  
            width: 100%;  
            border-collapse: collapse;  
            margin: 15px 0;  
            font-size: 0.95em;  
        }  

        th {  
            background: #0366d6;  
            color: white;  
            padding: 10px 14px;  
            text-align: left;  
        }  

        td {  
            padding: 9px 14px;  
            border-bottom: 1px solid #eaecef;  
        }  

        tr:nth-child(even) {  
            background: #f6f8fa;  
        }  

        tr:hover {  
            background: #f1f8ff;  
        }  

        /* Código */  
        code {  
            background: #f6f8fa;  
            border: 1px solid #eaecef;  
            border-radius: 4px;  
            padding: 2px 6px;  
            font-family: 'Courier New', monospace;  
            font-size: 0.9em;  
            color: #e36209;  
        }  

        pre {  
            background: #f6f8fa;  
            border: 1px solid #eaecef;  
            border-radius: 6px;  
            padding: 16px;  
            margin: 15px 0;  
            overflow-x: auto;  
        }  

        pre code {  
            border: none;  
            padding: 0;  
            color: #24292e;  
            font-size: 1em;  
        }  

        /* Imagens */  
        .img-container {  
            margin: 15px 0;  
            text-align: center;  
        }  

        .img-container img {  
            max-width: 100%;  
            border: 1px solid #eaecef;  
            border-radius: 8px;  
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);  
        }  

        .img-caption {  
            font-size: 0.85em;  
            color: #6a737d;  
            margin-top: 6px;  
            font-style: italic;  
        }  

        /* Divisor */  
        hr {  
            border: none;  
            border-top: 2px solid #eaecef;  
            margin: 30px 0;  
        }  

        /* Casos práticos */  
        .caso {  
            background: #f6f8fa;  
            border: 1px solid #eaecef;  
            border-radius: 8px;  
            padding: 20px;  
            margin: 20px 0;  
        }  

        .caso h3 {  
            color: #0366d6;  
            margin-top: 0;  
        }  

        /* FAQ */  
        .faq-item {  
            border-bottom: 1px solid #eaecef;  
            padding: 15px 0;  
        }  

        .faq-item:last-child {  
            border-bottom: none;  
        }  

        .faq-item h3 {  
            color: #0366d6;  
            margin-bottom: 8px;  
        }  

        /* Contato */  
        .contato {  
            background: #0366d6;  
            color: white;  
            border-radius: 8px;  
            padding: 20px 30px;  
            margin: 20px 0;  
        }  

        .contato a {  
            color: #ffffff;  
            text-decoration: underline;  
        }  

        .contato p {  
            margin-bottom: 8px;  
        }  

        /* Footer */  
        footer {  
            text-align: center;  
            color: #6a737d;  
            font-size: 0.85em;  
            margin-top: 30px;  
            padding-top: 15px;  
            border-top: 1px solid #eaecef;  
        }  

        /* Badge */  
        .badge {  
            display: inline-block;  
            background: #0366d6;  
            color: white;  
            border-radius: 12px;  
            padding: 3px 10px;  
            font-size: 0.8em;  
            margin-right: 5px;  
        }  
    </style>  
</head>  
<body>  

    <!-- CABEÇALHO -->  
    <h1>📘 Tutorial: Consulta de Viabilidade Econômica</h1>  
    <p><strong>Município de Apucarana - Guia Prático de Uso</strong></p>  

    <hr>  

    <!-- ÍNDICE -->  
    <h2>📑 Índice</h2>  
    <div class="indice">  
        <ol>  
            <li><a href="#introducao">Introdução</a></li>  
            <li><a href="#interface">A Interface</a></li>  
            <li><a href="#legendas">Legendas e Cores</a></li>  
            <li><a href="#zoneamento">Zoneamento</a></li>  
            <li><a href="#como-buscar">Como Buscar</a></li>  
            <li><a href="#casos-praticos">Casos Práticos</a></li>  
            <li><a href="#faq">FAQ</a></li>  
        </ol>  
    </div>  

    <hr>  

    <!-- INTRODUÇÃO -->  
    <h2 id="introducao">🎯 Introdução</h2>  
    <p>Bem-vindo ao tutorial da aplicação <strong>Consulta de Viabilidade Econômica</strong>! Esta ferramenta foi desenvolvida para ajudar você a consultar informações sobre terrenos e avaliar a viabilidade econômica de empreendimentos no município de Apucarana.</p>  

    <h3>O que você vai aprender:</h3>  
    <ul>  
        <li>Como acessar e navegar na aplicação</li>  
        <li>Entender o mapa interativo e suas legendas</li>  
        <li>Conhecer os diferentes zoneamentos</li>  
        <li>Realizar buscas por inscrição cadastral</li>  
        <li>Interpretar as informações de viabilidade</li>  
    </ul>  

    <div class="tip">  
        💡 <strong>Dica:</strong> Este tutorial leva aproximadamente 20 minutos para ser concluído. Você pode navegar pelas seções clicando no índice acima.  
    </div>  

    <hr>  

    <!-- A INTERFACE -->  
    <h2 id="interface">🖥️ A Interface</h2>  

    <h3>1️⃣ O Mapa Interativo Central</h3>  
    <p>A parte central da tela mostra um mapa do município de Apucarana com a localização dos terrenos, zoneamentos e áreas de interesse.</p>  

    <div class="img-container">  
        <img src="./img/mapa-principal.png" alt="Mapa Principal">  
        <p class="img-caption">Mapa interativo do município de Apucarana</p>  
    </div>  

    <div class="tip">  
        💡 Você pode ampliar (zoom) e mover o mapa usando o mouse. Use a rodinha do mouse para zoom!  
    </div>  

    <h3>2️⃣ O Painel Lateral Direito</h3>  
    <p>À direita, você encontra as abas de consulta com as seguintes opções:</p>  
    <ul>  
        <li><strong>Inscrição:</strong> Busca por inscrição cadastral do terreno</li>  
        <li><strong>CNAE:</strong> Atividades econômicas permitidas</li>  
        <li><strong>Endereço:</strong> Busca por localização</li>  
        <li><strong>Viabilidade:</strong> Análise de viabilidade econômica</li>  
    </ul>  

    <div class="img-container">  
        <img src="./img/painel-lateral-direito.png" alt="Painel Lateral Direito">  
        <p class="img-caption">Painel lateral direito com abas de consulta</p>  
    </div>  

    <h3>3️⃣ Controles do Mapa</h3>  
    <p>À esquerda do mapa, você encontra os botões de controle:</p>  
    <ul>  
        <li><strong>+/-</strong> Zoom in e zoom out</li>  
        <li><strong>🏠</strong> Voltar para a visão inicial</li>  
        <li><strong>⬅️➡️</strong> Navegar entre visualizações anteriores</li>  
        <li><strong>⬆️</strong> Bússola / orientação do mapa</li>  
        <li><strong>ℹ️</strong> Informações</li>  
        <li><strong>🗑️</strong> Limpar seleção</li>  
    </ul>  

    <h3>4️⃣ Barra Superior</h3>  
    <p>Na parte superior da tela você encontra:</p>  
    <ul>  
        <li><strong>Logo GeoAPUC</strong> e título da aplicação</li>  
        <li><strong>Barra de busca</strong> central: "Encontrar endereço ou lugar"</li>  
        <li><strong>Ícones</strong> no canto direito: camadas, lista, grid, régua, impressora e gráfico</li>  
    </ul>  

    <div class="img-container">  
        <img src="./img/barra-superior.png" alt="Barra Superior">  
        <p class="img-caption">Barra superior da aplicação</p>  
    </div>  

    <hr>  

    <!-- LEGENDAS E CORES -->  
    <h2 id="legendas">🎨 Legendas e Cores</h2>  
    <p>Entenda cada elemento do mapa e o que suas cores representam:</p>  

    <h3>📍 Mapa Cadastral</h3>  
    <table>  
        <tr>  
            <th>Símbolo</th>  
            <th>Cor</th>  
            <th>Significado</th>  
        </tr>  
        <tr>  
            <td>🟨</td>  
            <td>Amarelo (#FFFF99)</td>  
            <td>Lotes - Terrenos e propriedades urbanas</td>  
        </tr>  
    </table>  

    <h3>🏛️ Dados da Prefeitura</h3>  
    <table>  
        <tr>  
            <th>Símbolo</th>  
            <th>Cor</th>  
            <th>Significado</th>  
        </tr>  
        <tr>  
            <td>📍</td>  
            <td>Azul (#87CEEB)</td>  
            <td>Lagos - Corpos de água e reservatórios</td>  
        </tr>  
        <tr>  
            <td>❌</td>  
            <td>Vermelho (tracejado)</td>  
            <td>Perímetro Urbano e Distrital</td>  
        </tr>  
    </table>  

    <div class="img-container">  
        <img src="./img/legenda-completa.png" alt="Legenda Completa">  
        <p class="img-caption">Legenda completa do mapa</p>  
    </div>  

    <hr>  

    <!-- ZONEAMENTO -->  
    <h2 id="zoneamento">📊 Zoneamento - Tipos de Uso</h2>  
    <p>O zoneamento define o tipo de atividade permitida em cada área.</p>  

    <h3>🏘️ Zoneamento Residencial (ZR)</h3>  
    <table>  
        <tr>  
            <th>Zona</th>  
            <th>Cor</th>  
            <th>Descrição</th>  
        </tr>  
        <tr>  
            <td><strong>ZR1</strong></td>  
            <td>#FFFFCC (Amarelo Claro)</td>  
            <td>Zona Residencial 1</td>  
        </tr>  
        <tr>  
            <td><strong>ZR2</strong></td>  
            <td>#FFE0B2 (Bege)</td>  
            <td>Zona Residencial 2</td>  
        </tr>  
        <tr>  
            <td><strong>ZR3</strong></td>  
            <td>#FFCC99 (Laranja Claro)</td>  
            <td>Zona Residencial 3</td>  
        </tr>  
        <tr>  
            <td><strong>ZR5</strong></td>  
            <td>#999999 (Cinza)</td>  
            <td>Zona Residencial 5</td>  
        </tr>  
    </table>  

    <h3>💼 Zoneamento Especializado (ZE)</h3>  
    <table>  
        <tr>  
            <th>Zona</th>  
            <th>Cor</th>  
                        <th>Descrição</th>  
        </tr>  
        <tr>  
            <td><strong>ZEA</strong></td>  
            <td>#ADD8E6 (Azul Claro)</td>  
            <td>Zona Especializada Administrativa</td>  
        </tr>  
        <tr>  
            <td><strong>ZEC28</strong></td>  
            <td>#FFAACC (Rosa)</td>  
            <td>Zona Especializada Comercial</td>  
        </tr>  
        <tr>  
            <td><strong>ZER28</strong></td>  
            <td>#FFAACC (Rosa)</td>  
            <td>Zona Especializada Residencial</td>  
        </tr>  
        <tr>  
            <td><strong>ZEOC</strong></td>  
            <td>#E6CCFF (Roxo Claro)</td>  
            <td>Zona Especializada de Comércio</td>  
        </tr>  
        <tr>  
            <td><strong>ZEPC</strong></td>  
            <td>#CCFFCC (Verde Claro)</td>  
            <td>Zona Especializada de Produção</td>  
        </tr>  
    </table>  

    <h3>🌳 Outros Zoneamentos</h3>  
    <table>  
        <tr>  
            <th>Zona</th>  
            <th>Cor</th>  
            <th>Descrição</th>  
        </tr>  
        <tr>  
            <td><strong>ZPC</strong></td>  
            <td>#FFAA99 (Salmão)</td>  
            <td>Zona de Proteção da Comunidade</td>  
        </tr>  
        <tr>  
            <td><strong>ZRCH</strong></td>  
            <td>#90EE90 (Verde)</td>  
            <td>Zona de Patrimônio Histórico</td>  
        </tr>  
        <tr>  
            <td><strong>ZP</strong></td>  
            <td>#FFDDAA (Amarelo Forte)</td>  
            <td>Zona de Proteção</td>  
        </tr>  
        <tr>  
            <td><strong>ZI2</strong></td>  
            <td>#CCCCCC (Cinza Claro)</td>  
            <td>Zona Industrial</td>  
        </tr>  
    </table>  

    <div class="img-container">  
        <img src="./img/zoneamento-completo.png" alt="Zoneamento Completo">  
        <p class="img-caption">Mapa com todos os zoneamentos</p>  
    </div>  

    <div class="warning">  
        ⚠️ Cada zoneamento tem restrições específicas. Consulte a prefeitura para detalhes sobre o que é permitido em cada zona.  
    </div>  

    <hr>  

    <!-- COMO BUSCAR -->  
    <h2 id="como-buscar">🔍 Como Buscar um Terreno</h2>  

    <h3>1️⃣ Use a Barra de Busca Superior</h3>  
    <p>Na parte superior, há uma barra de busca onde você pode digitar endereço ou lugar.</p>  

    <div class="img-container">  
        <img src="./img/barra-busca.png" alt="Barra de Busca">  
        <p class="img-caption">Barra de busca superior</p>  
    </div>  

    <h3>2️⃣ Busque por Inscrição Cadastral</h3>  
    <p>No painel lateral direito, clique na aba <strong>"Inscrição"</strong> e digite o número no campo indicado.</p>  
    <p>O formato da inscrição é:</p>  

    <pre><code>000.000.0000.000</code></pre>  

    <p><strong>Exemplo:</strong> <code>109.011.0204.001</code> ou <code>103.068.0123.001</code></p>  

    <div class="tip">  
        💡 Se não souber a inscrição, use a aba <strong>"Endereço"</strong> para buscar pela rua ou bairro.  
    </div>  

    <h3>3️⃣ Clique em "Próximo"</h3>  
    <p>Após digitar a inscrição, clique no botão <strong>"Próximo >"</strong> para avançar.</p>  

    <h3>4️⃣ Visualize o Resultado</h3>  
    <p>O mapa irá centralizar no lote encontrado e exibirá as informações no painel direito.</p>  

    <div class="img-container">  
        <img src="./img/resultado-busca.png" alt="Resultado da Busca">  
        <p class="img-caption">Resultado da busca no mapa</p>  
    </div>  

    <div class="warning">  
        ⚠️ Se a busca não encontrar resultado, verifique se digitou corretamente a inscrição ou endereço.  
    </div>  

    <hr>  

    <!-- CASOS PRÁTICOS -->  
    <h2 id="casos-praticos">💼 Casos Práticos</h2>  

    <div class="caso">  
        <h3>Caso 1: Encontrar Terreno para Comércio</h3>  
        <p><strong>Objetivo:</strong> Buscar lotes em zona comercial ou especializada.</p>  
        <p><strong>Passos:</strong></p>  
        <ol>  
            <li>Na legenda, identifique as zonas comerciais: <strong>ZEC28, ZEOC e ZPC</strong></li>  
            <li>O mapa mostrará as áreas correspondentes nas cores indicadas</li>  
            <li>Use a barra de busca para encontrar endereços nessas zonas</li>  
            <li>Clique no lote para ver a inscrição e viabilidade</li>  
        </ol>  
    </div>  

    <div class="caso">  
        <h3>Caso 2: Verificar Zoneamento de um Endereço</h3>  
        <p><strong>Objetivo:</strong> Saber qual é o zoneamento de um terreno específico.</p>  
        <p><strong>Passos:</strong></p>  
        <ol>  
            <li>Busque o endereço na barra de busca superior</li>  
            <li>O mapa vai centralizar no local</li>  
            <li>Verifique a cor da área no mapa</li>  
            <li>Consulte a tabela de zoneamento para entender as regras</li>  
        </ol>  
    </div>  

    <div class="caso">  
        <h3>Caso 3: Identificar Propriedade pelo Cadastro</h3>  
        <p><strong>Objetivo:</strong> Localizar um terreno usando sua inscrição cadastral.</p>  
        <p><strong>Passos:</strong></p>  
        <ol>  
            <li>No painel direito, clique na aba <strong>"Inscrição"</strong></li>  
            <li>Digite a inscrição: <code>109.011.0204.001</code></li>  
            <li>Clique em <strong>"Próximo >"</strong></li>  
            <li>O mapa vai centralizar no lote e exibir todos os dados</li>  
        </ol>  
    </div>  

    <hr>  

    <!-- FAQ -->  
    <h2 id="faq">❓ FAQ - Perguntas Frequentes</h2>  

    <div class="faq-item">  
        <h3>Como saber a viabilidade econômica de um terreno?</h3>  
        <p>Após buscar o terreno, clique na aba <strong>"Viabilidade"</strong> no painel direito. Lá você encontrará informações sobre a viabilidade econômica do empreendimento.</p>  
    </div>  

    <div class="faq-item">  
        <h3>O que é CNAE?</h3>  
        <p>CNAE (Classificação Nacional de Atividades Econômicas) indica que tipo de atividades econômicas são permitidas naquele terreno. Exemplo: comércio, serviços, indústria.</p>  
    </div>  

    <div class="faq-item">  
        <h3>Os dados são atualizados?</h3>  
        <p>Sim, os dados são atualizados conforme novas informações são registradas na prefeitura.</p>  
    </div>  

    <div class="faq-item">  
        <h3>Posso usar esse mapa como prova legal?</h3>  
        <p>Este mapa é informativo. Para questões legais e documentos oficiais, procure a <strong>Idepplan</strong> - Instituto de Desenvolvimento, Pesquisa e Planejamento de Apucarana.</p>  
    </div>  

    <div class="faq-item">  
        <h3>A aplicação funciona em celular?</h3>  
        <p>Sim! A aplicação é responsiva e funciona bem em smartphones e tablets. Acesse pelo navegador do seu dispositivo.</p>  
    </div>  

    <div class="faq-item">  
        <h3>Encontrei um erro nos dados. Como reportar?</h3>  
        <p>Entre em contato com a Prefeitura de Apucarana através do email: <strong>suporte@apucarana.gov.br</strong></p>  
    </div>  

    <hr>  

    <!-- CONTATO -->  
    <h2>📞 Contato</h2>  
    <div class="contato">  
        <p><strong>Tutorial - Consulta de Viabilidade Econômica | Apucarana - PR</strong></p>  
        <p>📧 Email: <a href="mailto:suporte@apucarana.gov.br">suporte@apucarana.gov.br</a></p>  
        <p>📱 Tel: (43) 3422-0000</p>  
    </div>  

    <footer>  
        <p>Última atualização: 2026 | Município de Apucarana - PR</p>  
    </footer>  

</body>  
</html>
