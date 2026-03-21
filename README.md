Aqui está o relatório corrigido, removendo a barra invertida e mantendo a formatação HTML de justificação solicitada:

<p align="justify\><h1\>Detecção de Anomalias em Vibrações Ferroviárias com Transformers\</h1\>\</p\>

<p align="justify"\>A implementação de um sistema de monitoramento para a \<b>Manutenção 4.0\</b\> utiliza o poder dos Transformers para aprender o comportamento dinâmico "saudável" de uma infraestrutura. Ao contrário de métodos estatísticos simples, o modelo de Deep Learning consegue capturar dependências temporais complexas, permitindo distinguir entre o ruído operacional comum e falhas estruturais críticas. Abaixo, detalhamos os blocos fundamentais do código e a interpretação dos resultados.\</p\>

<p align="justify">\<h3>1. Geração de Sinais: O Gêmeo Digital do Trilho\</h3\>\</p\>

<p align="justify">Para validar o modelo, simulamos a física de um ambiente ferroviário. O \<b\>Sinal Normal\</b\> é composto por frequências fundamentais estáveis (representando a rotação das rodas e a ressonância do truque). Já o \<b\>Sinal Anômalo\</b\> introduz transientes não-lineares: impactos súbitos com decaimento exponencial e alta frequência. Esta distinção é crucial, pois em um cenário real, uma fissura no trilho ou um defeito no rolamento não altera apenas a amplitude, mas introduz uma assinatura espectral completamente nova que o modelo deve ser capaz de rejeitar como "desconhecida".\</p\>

<p align="justify\>\<h3>2. A Arquitetura: Transformer para Séries Temporais\</h3\>\</p\>

<p align="justify">O coração do código é a classe \<code\>RailVibrationTransformer\</code\>. Ela utiliza o mecanismo de \<b\>Self-Attention\</b\> para analisar uma janela de 50 milissegundos de dados. O modelo não olha apenas para o valor anterior, mas para a correlação entre todos os pontos da janela simultaneamente. Enquanto em otimizações clássicas buscaríamos parâmetros fixos, aqui os pesos do Transformer se ajustam para minimizar o erro de previsão (MSE) apenas para o padrão saudável, criando um "filtro de normalidade".\</p\>

<p align="justify"\>\<h3\>3. Detecção via Erro de Reconstrução\</h3\>\</p\>

<p align="justify"\>A detecção não ocorre por uma classificação direta, mas através da métrica de \<b\>Resíduo\</b\>. O modelo tenta prever o próximo ponto do sinal. Quando o sinal é normal, a previsão sobrepõe-se quase perfeitamente ao real. Quando a anomalia ocorre, o Transformer tenta "forçar" o padrão que ele conhece (a senoide suave) sobre o impacto caótico. A diferença matemática entre essas duas curvas gera o \<b\>Score de Anomalia\</b\>.\</p\>

<p align="justify"\>\<h3\>4. Conclusão e Análise das Figuras\</h3\>\</p\>

<p align="justify"\>Ao observar os gráficos gerados, a eficácia do método torna-se evidente:\</p\>

<p align="justify"\>\<ul\>
<li\>\<b\>Figura Superior (Sinal de Aceleração):\</b\> Mostra que o sinal de vibração é altamente ruidoso, dificultando a detecção visual imediata. No entanto, as áreas destacadas mostram onde o comportamento transiente rompe a ciclicidade.\</li\>
<li\>\<b\>Figura Inferior (Erro Residual):\</b\> É onde a inteligência do sistema reside. O \<b\>Limiar de Alerta (Threshold)\</b\>, definido estatisticamente, serve como uma barreira de segurança. Note que o erro permanece baixo durante a operação normal e apresenta picos agudos exatamente nos eventos de falha.\</li\>
</ul\>\</p\>

<p align="justify"\>Em suma, a aplicação de Transformers para previsão de vibração transforma dados brutos de sensores em \<b\>informação acionável\</b\>. Este projeto demonstra que é possível automatizar a vigilância de ativos ferroviários, prevenindo acidentes através da identificação precoce de comportamentos anômalos.\</p\>
