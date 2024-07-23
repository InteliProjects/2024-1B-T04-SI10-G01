# Análise Final dos Resultados do Teste A/B

## Introdução 

Este documento fornece uma visão completa e detalhada do desempenho e impacto das variáveis e ajustes testados, fundamentando todas as conclusões e recomendações com dados robustos. Inicialmente, está sendo recapitulado o propósito e as metas do teste, abordando as hipóteses iniciais e a estrutura do teste para proporcionar um contexto claro. Em seguida, está sendo apresentado os dados acumulados e a descrição das ferramentas e técnicas estatísticas utilizadas na análise. 

## Teste A/B

### Propósito e Metas

O principal objetivo deste teste A/B foi aumentar a taxa de conversão de leads para 7%, com base em três hipóteses específicas. A primeira hipótese sugere que alterar a mensagem de confirmação de envio do formulário poderia transmitir a informação de forma mais clara e objetiva ao usuário, além de criar uma experiência mais positiva, resultando em um aumento na retenção de leads. A segunda hipótese propõe que diminuir o tamanho do botão do WhatsApp e remover o CTA "Clique Aqui e Fale Conosco" reduziria a distração do usuário, liberando a zona do polegar para uma melhor usabilidade em dispositivos móveis e, consequentemente, aumentaria a taxa de conversão dos formulários de inscrição. A terceira hipótese argumenta que simplificar o conteúdo da página, removendo informações excessivas e focando nos principais benefícios do curso, reduziria a sobrecarga cognitiva e aumentaria a taxa de inscritos.

### Estrutura do Teste

Para testar as hipóteses acima, o experimento foi estruturado com variáveis independentes englobando mudanças no design, na estrutura e nos conteúdos da landing page, comparando a Proposta A (versão atual) com a Proposta B (nova versão). As variáveis dependentes focaram na taxa de conversão de usuário para lead. O público-alvo consistiu nos visitantes da landing page, com o tamanho da amostra determinado por simulações de Monte Carlo que consideraram períodos sazonais. Uma estratégia de randomização foi utilizada, alocando 30% dos visitantes à versão B, estabelecendo um período de teste de duas semanas.

A implementação técnica empregou ferramentas integradas de teste A/B, facilitando a revisão contínua de códigos e designs. O teste foi programado para iniciar em 5 de junho e terminar em 17 de junho. Durante esse período, o desempenho foi monitorado continuamente por meio de ferramentas analíticas, e a análise dos dados foi conduzida através de métodos estatísticos, como testes t de Student e análise de intervalos de confiança. A comparação dos desempenhos entre as versões A e B elucidou as melhorias alcançadas pelas modificações, com avaliações de significância estatística fundamentais para validar ou refutar as hipóteses propostas.

## Apresentação dos Dados

Nesta seção está sendo apresentada uma análise detalhada dos dados acumulados durante o teste A/B, visando identificar o impacto na taxa de conversão de leads da landing page. O teste foi conduzido utilizando o Looker Studio, que integra dados do Google Analytics. Segue abaixo, uma visão detalhada do volume e da natureza dos dados coletados.

### Volume dos Dados
Durante o período de duas semanas, o tráfego da landing page foi dividido da seguinte maneira:

- Página A: 73%, equivalente a 10.146 visitas.
- Página B: 27%, equivalente a 3.643 visitas.

A intenção era que o tráfego da Página B fosse dividido uniformemente por grupo, ou seja, 6% para cada equipe. Contudo, a operacionalização pela MarketMedia/Pearson resultou em uma variação nos percentuais. Abaixo, é possível visualizar o tráfego total (Tabela 1) e por grupo (Tabela 2).

| Página | Tráfego (%) | Tráfego (n) |
|--------|-------------| -------------|
| A      | 73%         | 3643 |
| B      | 27%         | 10146 | 

Tabela 1. Tráfego Geral. Fonte: Arquivo Pessoal. 

| Página | Tráfego (%) | Tráfego (n) |
|--------|-------------| -------------|
| 1      | 25,17%         | 917 |
| 2      | 16,93%         | 617 | 
| 3      | 25,47%         | 928 |
| 4      | 17,37%         | 633 | 
| 5      | 15,04%         | 548 |

Tabela 2. Tráfego por Grupo. Fonte: Arquivo Pessoal. 

### Natureza dos Dados

#### Ferramentas Utilizadas

- Google Analytics: Para rastreamento de tráfego, taxas de conversão e comportamento do usuário.
- Looker Studio: Para integração e visualização dos dados, facilitando a análise detalhada e o monitoramento contínuo durante o período do teste.

#### Dados Coletados

Durante o período dos testes, foram obtidos apenas dados quantitativos. Abaixo está a descrição dos mesmos:

- Forms: referem-se às informações coletadas dos usuários quando eles preenchem e submetem o formulário de interesse na landing page.
- Sessions: é o período em que um usuário interage com a landing page. O Google Analytics registra uma sessão sempre que um usuário visita a página e interage com ela de alguma forma.

Através desses dados, obtém-se a taxa de conversão, que é a proporção de visitantes da landing page que submetem o formulário em relação ao número total de visitantes.

### Descrição das Ferramentas e Técnicas Estatística

O sistema utilizado para a coleta e análise dos dados será o Looker Studio (anteriormente Google Data Studio), da Pearson. Esta plataforma permite a integração com diversas fontes de dados, incluindo o Google Analytics, que será a principal fonte de informações para os testes A/B.

#### P-Valor

O p-valor é uma medida estatística utilizada para determinar a significância dos resultados de um teste A/B, quantificando a probabilidade de que as diferenças observadas entre as versões testadas (Proposta A e Proposta B) tenham ocorrido por acaso. Em termos práticos, um p-valor baixo (geralmente inferior a 0,05) indica que existe uma alta confiança de que as alterações implementadas (como mudanças no design ou conteúdo da landing page) têm um impacto real e significativo sobre a métrica de interesse, neste caso, a taxa de conversão de leads. Sua contribuição é crucial, pois permite aos analistas diferenciar entre variações causadas por intervenções efetivas e aquelas que são resultado de flutuações aleatórias nos dados, garantindo decisões baseadas em evidências concretas e não em suposições.

#### Teste t

O teste t de Student é uma técnica estatística fundamental para comparar as médias de duas amostras independentes, como as taxas de conversão das versões A e B da LP em um teste A/B. Ele testa a hipótese nula de que não há diferença significativa entre as médias das duas amostras, utilizando uma estatística t para determinar se a diferença observada é estatisticamente significativa, com um p-valor inferior a 0,05 indicando significância. Complementando essa análise, o intervalo de confiança fornece uma faixa de valores estimados dentro da qual se espera que a verdadeira taxa de conversão populacional se situe com um determinado nível de confiança, geralmente 95%. O intervalo de confiança ajuda a visualizar a precisão das estimativas e a entender a variabilidade dos dados. Juntas, essas técnicas asseguram uma análise robusta e confiável, permitindo a validação ou refutação das hipóteses propostas e fornecendo uma base sólida para a interpretação dos resultados do teste A/B e a tomada de decisões informadas.

#### Condução da Análise 

Para compreender a eficácia das mudanças implementadas na landing page, a análise quantitativa é realizada diariamente ao longo do período de teste, de 5 de junho a 17 de junho. Esta análise envolve a coleta e comparação de dados de conversão das versões A (atual) e B (nova), focando na taxa de conversão de usuários para leads. O processo é detalhado da seguinte forma:

1. **Coleta Diária de Dados**:
    
     Foi utilizado o Looker Studio para integrar dados do Google Analytics. Já o monitoramento da taxa de conversão diária, foi feito a partir número do número de formulários enviados e sessões exploradas pelos usuários.
    
2. **Monitoramento Contínuo**:
    
    Com o passoar dos dias, foi realizado uma comparação contínua das taxas de conversão entre as duas versões para identificar tendências e flutuações.
    
3. **Análise Estatística**:
    
    Em seguida, aplica-se testes estatísticos para comparar as médias das taxas de conversão entre as versões A e B. Além disso, utiliza-se a determinação do p-valor para avaliar a significância das diferenças observadas. 
    
    Alinhado ao visto anteriormente, calcula-se o intervalos de confiança para as taxas de conversão de ambas as versões, fornecendo uma margem de erro para as estimativas e garantindo a precisão dos resultados.
    
4. **Avaliação e Interpretação dos Resultados**:
    
    Observação de padrões diários e sazonais que possam influenciar as taxas de conversão são fundamentais para a etapa de interpretação de resultados. Em concordância, a análise de verificação a fim de compreender se as hipóteses propostas foram confirmadas, utilizando os resultados estatísticos para suportar as conclusões.
    

A metodologia de análise quantitativa por períodos permite uma avaliação detalhada e contínua do impacto das mudanças testadas na taxa de conversão. O uso de estatísticas, como o cálculo do p-valor e intervalos de confiança, assegura a robustez dos resultados, diferenciando entre variações significativas e ruído aleatório. Esse processo não só valida as hipóteses propostas, mas também fornece uma compreensão aprofundada das dinâmicas de conversão ao longo do tempo.

Dessa forma, o Looker Studio permitiu visualizar o impacto das alterações em tempo real, ajudando a ajustar rapidamente a estratégia durante o período de teste. E o uso do p-valor confirmou que as mudanças realizadas eram estatisticamente significativas, assegurando que o aumento observado na taxa de conversão não foi devido ao acaso. Ressalta-se ainda que a comparação entre as versões A e B destacou claramente as melhorias, proporcionando insights valiosos sobre quais elementos do design e conteúdo tiveram maior impacto na conversão.

### Análise Estatística

#### Taxas de Conversão

| Página | Taxa de Conversão | 
|--------|-------------|
| Página B (Grupo 1) | 0.050676  |
| Página A | 0.034877 |

#### Cálculo da Taxa de Conversão

A **taxa de conversão** é calculada como a razão entre o número de formulários preenchidos (Leads) e o número total de sessões. 

#### Teste Qui-Quadrado

- **Chi2**: 5.567191031286078
- **Valor-p**: 0.018300095285156234
- A diferença nas taxas de conversão é estatisticamente significante.

#### Interpretação do Teste Qui-Quadrado

- **Chi2**: É o valor da estatística do teste qui-quadrado. Valores maiores indicam maior divergência entre as proporções observadas.
- **Valor-p**: Representa a probabilidade de se observar um valor tão extremo quanto o valor da estatística de teste, assumindo que a hipótese nula é verdadeira. Um valor-p menor que 0.05 sugere que a diferença nas taxas de conversão é **estatisticamente significante**.

#### Validade e Confiabilidade dos Resultados

Os resultados do teste qui-quadrado indicam que há uma diferença estatisticamente significante nas taxas de conversão entre o Grupo 1 e a Página A (p < 0.05). Isso sugere que as mudanças implementadas na Página A tiveram um impacto real nas taxas de conversão. No entanto, é importante considerar fatores como tamanho da amostra, viés de seleção e outros fatores externos que possam ter influenciado os resultados.

### Impacto no Entendimento do Comportamento do Usuário ou do Produto Testado

Esses resultados sugerem que os usuários podem ter reagido positivamente às mudanças na página. É importante investigar mais a fundo para entender as mudanças que geraram esse efeito e mapeá-las. 

#### Principais Aprendizados

1. A Página A apresentou uma taxa de conversão inferior ao Grupo 1 (Figura 1), indicando que as mudanças feitas podem ter sido eficazes ou que outros fatores externos influenciaram os resultados.
2. A diferença é estatisticamente significante, sugerindo que as mudanças implementadas tiveram um efeito real nas taxas de conversão.

![Taxa de Conversão](https://github.com/Inteli-College/2024-1B-T04-SI10-G01/blob/dev/assets/imagens/TaxaDeConversao.png)

Figura 1. Comparação entre a Página A e a Página do Grupo. Fonte: Arquivo Pessoal. 
