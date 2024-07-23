# Plano de Coleta dos Dados

## Sistema de Coleta de Resultados:

O sistema utilizado para a coleta e análise dos dados será o Looker Studio (anteriormente Google Data Studio), da Pearson. Esta plataforma permite a integração com diversas fontes de dados, incluindo o Google Analytics, que será a principal fonte de informações para os testes A/B.

### Métricas Coletadas:

1. **Porcentagem de Cliques no Botão WhatsApp:**
    - **Descrição:** Mede a proporção de visitantes que clicam no botão do WhatsApp em relação ao total de visitantes.
    - **Importância:** Avalia a eficácia do tamanho e posicionamento do botão WhatsApp na versão B da página.
    - **Coleta:** Eventos de cliques no botão são rastreados via tags e triggers configurados no Google Tag Manager (GTM) e importados para o LookerStudio.
2. **Porcentagem de Usuários que Rolam a Página:**
    - **Descrição:** Mede a proporção de visitantes que rolam a página até o fim, mostrando o nível de engajamento com o conteúdo da página.
    - **Importância:** Indica se a disposição do conteúdo e a redução de elementos distrativos estão melhorando a navegação, assim permitindo novas hipóteses sobre a arquitetura da informação.
    - **Coleta:** Eventos de rolagem são configurados no GTM para acionar quando um usuário alcança o final da página, sendo esses dados sincronizados com o LookerStudio.
3. **Número de Acessos à Página:**
    - **Descrição:** Conta o número total de visitantes que acessam a landing page.
    - **Importância:** Fornece a base para calcular outras métricas como taxas de cliques e conversão.
    - **Coleta:** Dados de acessos são coletados diretamente pelo Google Analytics e integrados ao LookerStudio.
4. **Taxa de Conversão:**
    - **Descrição:** Mede a proporção de visitantes que completam o formulário de lead em relação ao total de visitantes.
    - **Importância:** Principal métrica para avaliar o sucesso do teste A/B em aumentar as conversões de leads.
    - **Coleta:** Eventos de submissão do formulário são rastreados no GTM e os dados são enviados para o LookerStudio.

## Objetivos e Avaliação de Cumprimento

O teste A/B teve como principal objetivo o melhor posicionamento da Wizard, buscando aumentar a exposição de seus produtos e serviços. Sendo assim, 

### Objetivos do Teste A/B:

- **Aumentar a Taxa de Conversão:** Aumentar a proporção de visitantes (Views) que completam o formulário de lead (Conversions).
- **Melhorar o Engajamento:** Aumentar a porcentagem de usuários que rolam a página até o fim.
- **Otimizar a Usabilidade:** Reduzir cliques acidentais no botão WhatsApp, melhorando a experiência do usuário.

### Avaliação:

- **Comparar as Métricas:** Comparar as métricas de cliques, rolagem, acessos e conversão entre as versões A e B da página.
- **Feedback da Equipe:** Incorporar feedback qualitativo da equipe e, se possível, dos próprios usuários para complementar os dados quantitativos.
- **Análise Estatística:** Utilizar análises estatísticas para determinar se as diferenças observadas são significativas.

### Análise Estatística

Para medir a eficácia das mudanças, podemos usar métricas estatísticas aplicadas tanto às amostras históricas quantos as de teste, sendo a última proveniente da implementação da Variável B. Uma das principais métricas é a estatística t, que nos ajuda a determinar a significância dos resultados do nosso teste. Um valor absoluto elevado da estatística t (x>0) sugere que é menos provável que a diferença observada seja devida ao acaso. Para medir a relevância do teste, comparamos as médias de conversão das diferentes campanhas (Variável A e Variável B) e calculamos o erro padrão das médias. A estatística t é então calculada como a diferença entre as médias dividida pelo erro padrão, permitindo avaliar se a diferença entre as campanhas é estatisticamente significativa, sendo menos provável que a diferença observada seja devida ao acaso.

Com a mesma finalidade podemos obter o valor p, que é uma ferramenta essencial para determinar a significância dos resultados em testes A/B. Considerando que nível de significância que utilizaremos é de 0.05, se o valor p calculado é 0.02, então rejeitamos a hipótese nula. Isso indica que a diferença nas taxas de conversão entre as variáveis A e B é estatisticamente significativa. Afim de trazer ainda mais evidências e novas hipóteses para futuros testes A/B, mediremos o impacto desse teste pelo Cohen’s d.

A métrica Cohen’s d nos ajuda a quantificar a magnitude da diferença entre duas médias. Enquanto as métricas anteriores nos diz se a diferença é significativa, o Cohen's d nos diz o quão grande essa diferença é. Um valor absoluto de d em torno de:

- 0.2: Pequeno efeito
- 0.5: Efeito médio
- acima de 0.8: Efeito muito grande

Suponha que, após realizar o teste A/B, calculemos um Cohen's d de 0.6. Isso indicará que a diferença nas taxas de conversão entre as varíaveis A e B teve um efeito médio.

Concluindo, a implementação deste plano permitirá uma coleta de dados estruturada e uma análise detalhada, fornecendo um direcionamento sobre a eficácia das mudanças propostas e permitindo ajustes contínuos para as próximas de landing pages da Wizard-On.
