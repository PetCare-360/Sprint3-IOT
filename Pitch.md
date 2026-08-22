# Pitch.md — Roteiro do Vídeo Pitch (~5 minutos)
### PetCare 360 × CLYVO VET — Componente de Inteligência Artificial

Este documento contém tudo o que é necessário para gravar o vídeo pitch: roteiro de fala segmentado por tempo, o que mostrar na tela em cada bloco, e um checklist de gravação. Duração alvo: **5 minutos** (o roteiro tem ~700 palavras, ritmo de fala confortável).

---

## Checklist antes de gravar

- [ ] Tela com o diagrama de arquitetura aberto (`docs/diagrams/arquitetura-ia.mermaid` renderizado, ou o print da seção 7.1 do `README.md`)
- [ ] Dashboard da Sprint 1 aberto (ou print dele) para mostrar os dados reais da coleira
- [ ] Se possível, um mockup/print de como ficaria a notificação gerada pela IA para o tutor
- [ ] Definir quem fala cada bloco (pode ser 1 pessoa ou revezar entre a equipe)
- [ ] Cronometrar um ensaio antes da gravação final

---

## Roteiro por blocos

### Bloco 1 — Abertura / Gancho (0:00 – 0:30)
**Tela:** logo do projeto / integrante falando para a câmera.

> "Um pet não avisa quando está com dor. Ele não liga para a clínica quando a frequência cardíaca sobe, nem manda mensagem quando para de comer direito. E é exatamente nesse intervalo, entre uma consulta e outra, que os problemas mais sérios começam — silenciosamente. Nosso projeto, o PetCare 360, feito para a CLYVO VET, existe para fechar esse vão."

### Bloco 2 — O Problema (0:30 – 1:15)
**Tela:** slide simples com os 3 pontos de dor (tutor / clínica / pet), ou apenas o apresentador.

> "Hoje o cuidado com o pet é reativo: o tutor só percebe que algo mudou quando já é visível, e a clínica só age quando o tutor entra em contato. Não existe monitoramento contínuo, não existe priorização de quem precisa de atenção primeiro, e as recomendações — quando existem — são genéricas, iguais para qualquer pet. O resultado: diagnósticos tardios, vacinas esquecidas e tratamentos abandonados no meio do caminho."

### Bloco 3 — A Solução e o Papel da IA (1:15 – 2:15)
**Tela:** mostrar o dashboard da Sprint 1 recebendo dados da coleira em tempo real.

> "Na Sprint anterior, construímos a coleira inteligente: um ESP32 com sensores que coleta temperatura, frequência cardíaca, nível de atividade e bateria do pet, e envia isso em tempo real para nosso sistema. Isso já prova que conseguimos captar o dado. O desafio agora era: o que fazer com ele?
>
> É aí que entra o **Vitalis Core**, o motor de inteligência artificial do PetCare 360. Ele tem três camadas trabalhando juntas: o **Vitalis Sense**, que aprende o padrão normal de cada pet individualmente e detecta quando algo foge disso; o **Vitalis Rules**, que cruza essa detecção com o histórico clínico do pet e decide o nível de prioridade; e o **Vitalis Voice**, que transforma tudo isso em uma mensagem humana e personalizada — para o tutor e para a equipe da clínica."

### Bloco 4 — Arquitetura e Fluxo de Dados (2:15 – 3:15)
**Tela:** diagrama de arquitetura (seção 7.1 do README) em tela cheia, apontando os blocos enquanto fala.

> "O fluxo funciona assim: a coleira envia os dados para nossa API, que grava tanto no banco de dados cadastral — perfil, vacinas, consultas, medicamentos — quanto em um banco de séries temporais com o histórico de sinais vitais. O Vitalis Sense lê essa série temporal e calcula um score de anomalia comparando com o baseline daquele pet específico. Esse score vai para o Vitalis Rules, que cruza com raça, idade e tempo desde a última consulta para calcular a prioridade. E por fim, o Vitalis Voice usa um modelo de linguagem para gerar a mensagem final — sempre com base nos dados reais, nunca inventando informação — que chega ao tutor como notificação, e à clínica como um resumo no painel de priorização."

### Bloco 5 — Benefícios (3:15 – 4:15)
**Tela:** dividir a tela ou alternar entre "visão do tutor" e "visão da clínica" — pode ser um mockup simples de notificação de um lado e o painel de priorização do outro.

> "Para o tutor, isso significa tranquilidade: em vez de um número sem contexto, ele recebe uma mensagem clara — 'a frequência cardíaca do Thor está acima do normal dele, considere agendar uma avaliação' — no momento certo, no tom certo.
>
> Para a clínica CLYVO VET, isso significa conseguir monitorar centenas de pets com a equipe que já tem, porque o sistema já entrega uma fila priorizada de quem precisa de contato primeiro, e um resumo pronto antes de cada consulta — economizando tempo de triagem e permitindo contato proativo com o tutor, antes que a situação vire uma emergência."

### Bloco 6 — Responsabilidade e Diferencial Técnico (4:15 – 4:45)
**Tela:** apresentador falando direto para a câmera (reforça credibilidade).

> "E um ponto importante: em nenhum momento a IA substitui o veterinário. Ela nunca dá um diagnóstico — ela prioriza, contextualiza e comunica, sempre recomendando avaliação profissional quando necessário. É inteligência artificial aplicada com responsabilidade, unindo modelo preditivo, motor de regras e IA generativa, cada um fazendo exatamente a parte que faz melhor."

### Bloco 7 — Encerramento (4:45 – 5:00)
**Tela:** logo / créditos da equipe.

> "Esse é o PetCare 360: da coleira ao cuidado contínuo, com a CLYVO VET presente em cada etapa da jornada do pet. Obrigado!"

---

## Observações finais

- O roteiro está redigido como um **guia de fala**, não uma leitura obrigatória palavra por palavra — a equipe pode adaptar o tom para soar natural na gravação.
- Se a equipe preferir dividir as falas, uma sugestão é: Bloco 1–2 (problema) com um integrante, Bloco 3–4 (solução/arquitetura, o trecho mais técnico) com quem mais entende da IA, e Bloco 5–7 (benefícios/encerramento) com outro integrante — assim o vídeo mostra múltiplas vozes do time.
- Vale gravar a tela do diagrama e do dashboard **separadamente** e editar por cima da narração, em vez de tentar narrar e navegar ao mesmo tempo.
