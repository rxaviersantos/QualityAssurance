<h1 align="center">
Projetando uma estratégia de automação de teste
</h1>

## O que
      - Qual é o seu objetivo ao iniciar uma iniciativa de automação de teste e o que você deseja realizar?
      - Quem você imagina participando de sua iniciativa de automação de teste e em que capacidade?
      - Como você planeja a execução dessa estratégia
      

### Passo a passo 

```mermaid 
graph LR;
A[("Passo a passo de como automatizar 
seus testes sem ser um bicho de sete cabeças  fa:fa-cubes")] 
B["Conheça seu cenário fa:fa-globe"] 
C["Saiba quais testes automatizar fa:fa-globe"]
D["Escolha as ferrmentas fa:fa-globe"]
E["Coloque no papel fa:fa-globe"]
F["Mão na massa fa:fa-globe"]
G["Rode os tesetes automaticamente fa:fa-globe"]
H["Compartilhe com o time fa:fa-globe"]

A --> B 
A --> C
A --> D
A --> E
A --> F
A --> G
A --> H
```` 

[Disponível](https://www.programmers.com.br/blog/automacao-zero-to-hero-comece-automatizar-seus-testes/#:~:text=Saiba%20os%20cen%C3%A1rios%20de%20testes%20primeiro&text=Comece%20criando%20os%20cen%C3%A1rios%20que,o%20teste%20deve%20ser%20codificado.  "Projetando uma estratégia de automação de teste")


## Qual é o objetivo para automação de teste? 

É para reduzir o tempo que leva para executar o teste de regressão? Talvez sua equipe precise lançar recursos mais rapidamente. Portanto, você deseja reduzir o esforço manual necessário para executar os testes de regressão e permitir que seus testadores se concentrem em testar os novos recursos.

Ou talvez seu objetivo seja reduzir a dívida técnica fechando seus sprints com automação de teste para os novos recursos? Como seus desenvolvedores estão criando novos recursos e seus testadores estão verificando-os, não há muito tempo para testes de regressão completos. E fechar o sprint sem automatizar os testes recém-identificados só aumenta esse problema. Então talvez você queira cuidar disso desde o início.

Ou talvez seu objetivo seja permitir testes contínuos como parte de seu processo de construção? Depois de verificar novos recursos, seus desenvolvedores podem querer a confiança de que o que eles adicionaram não está comprometendo a qualidade geral do aplicativo. Adicionar testes automatizados ao seu pipeline de integração contínua certamente pode ajudar nisso.

A chave aqui é entender o que você está tentando realizar. Antes de iniciar qualquer planejamento, reserve um momento para decidir por que você precisa da automação de teste.

Certifique-se de que esse objetivo esteja na vanguarda de todas as suas decisões, porque suas ações subsequentes em relação à automação de teste devem ser voltadas para esse objetivo. Quem você envolve, as ferramentas que usa, quais testes você automatiza, a estratégia de execução… tudo isso deve estar alinhado com o seu objetivo.

Comunique o objetivo a toda a equipe. Certifique-se de que todos estejam cientes do motivo pelo qual a equipe está fazendo automação de teste e o que todos desejam realizar com isso.

## Quem 
     - Quem você imagina participando de sua iniciativa de automação de teste e em que capacidade?
Tarefas para automatizar testes de regressão; 

- Escrever os scripts de automação de teste
- Monitorar os resultados toda vez que os testes são executados
- Atualize os testes quando o comportamento do aplicativo mudar

Essas tarefas podem ser realizadas pela mesma pessoa ou compartilhadas entre a equipe.

Digamos que você escolha os desenvolvedores. Porque, ei, eles já sabem codificar. Bem, seus desenvolvedores estão trabalhando em novos recursos. Eles realmente terão tempo para trabalhar em scripts de testes de regressão?

Ok, digamos que você escolha os testadores manuais para escrever os scripts de teste, porque, ei, eles são melhores em testes de qualquer maneira. Vamos nos lembrar do problema que estamos resolvendo. Você está investindo na automação de teste como forma de reduzir o tempo e o esforço necessários para o teste de regressão. Agora você pode dispensar os testadores não apenas para testar novos recursos, mas também para gastar tempo automatizando testes antigos?

Aqui está a dura verdade: a menos que você consiga tirar seus desenvolvedores ou testadores de suas tarefas atuais de trabalhar em novos recursos, ou você seja capaz de fornecer a eles o tempo e os recursos necessários para realizar essas tarefas, essas podem não ser suas melhores opções.

Não se engane, a automação de teste é um projeto de desenvolvimento de software por si só. Leva uma quantidade considerável de tempo e habilidade para fazê-lo. Se você tratá-lo como uma tarefa secundária para a qual as pessoas só contribuem quando têm tempo, ele falhará.

Mesmo que você consiga encontrar tempo para permitir que seu desenvolvedor ou testador escreva os scripts automatizados, ainda há as tarefas de monitorá-los e atualizá-los conforme necessário.

```Então, o que você faz? Bem, você tem algumas opções.```

Algumas empresas designam alguém para trabalhar temporariamente na automação de sua lista de pendências de regressão. No entanto, isso só funciona se você tiver outro plano e estratégia para testes futuros. Caso contrário, o backlog de regressão crescerá continuamente à medida que novos recursos forem desenvolvidos e você se encontrará de volta ao quadrado 1.

Outra opção é designar alguém para trabalhar permanentemente em sua automação de teste. Isso se torna seu trabalho em tempo integral. E sim, na maioria dos casos, é de fato um trabalho em tempo integral. Você pode designar um desenvolvedor ou testador para essa função ou fazer com que trabalhem juntos como um par, mas certifique-se de levar em consideração o fato de que qualquer um deles teria que investir no aprendizado da automação de teste. Sim, seu desenvolvedor sabe codificar, mas quão familiarizado ele está com testes e automação de testes? Seu testador entende de teste, mas quão familiarizado ele está com desenvolvimento e automação de teste? Não me interpretem mal, esta estratégia certamente pode funcionar, mas você deve ser realista sobre a curva de aprendizado e o investimento de tempo. E também ajuda muito se a pessoa realmente quiser fazer esse trabalho.

Outra ótima alternativa é contratar um engenheiro de automação de teste. Essa pessoa é idealmente qualificada em testes, bem como no desenvolvimento de automação. Eles podem liderar seus esforços de automação de teste e incluir os desenvolvedores e testadores em uma capacidade mais viável. Se você seguir esse caminho, é fundamental que faça dessa pessoa uma parte padrão de sua equipe. Tê-los interagindo e colaborando com o restante dos membros da equipe fortalecerá sua iniciativa de automação de teste.

## Como 
    - Como você planeja a execução dessa estratégia?
    
Digamos que você tenha definido sua estratégia e tenha uma ideia de quem liderará o esforço e também de como os outros contribuirão.

```Quais testes devemos automatizar?```

Deixe-me oferecer uma pergunta para ponderar. Quando sua equipe estava executando esses testes manualmente, eles executavam todos eles todas as vezes? Ou eles tomaram uma decisão estratégica com base em outros fatores, como risco e valor?

Você pode pensar que, como está automatizando esses testes, é melhor automatizar todos eles, mas há um custo que vem com a automação. O tempo e a manutenção necessários não são algo a ser menosprezado.

`` Qual é o cenário?`` 

Para automatizar os testes, você precisa de um entendimento claro dos cenários. As ações e os resultados esperados estão claramente definidos?

Isso pode ser coberto por meio de testes de aceitação, cenários Gherkin ou casos de teste. Embora a comunicação verbal seja maravilhosa, um resumo escrito das expectativas, mesmo que leve, é extremamente útil ao escrever automação de teste. A mente do autor do script de teste está trocando do modo de criação para o modo de verificação enquanto eles escrevem o código de teste. Ter um guia para consultar para garantir que nada seja perdido é fundamental.

`` E a implementação?`` 

Você precisará escolher ferramentas para seu projeto de automação, como uma linguagem de programação ou oferta sem código. Assim como em seus projetos de desenvolvimento, você também desejará desenvolver padrões e convenções, especialmente se imaginar várias pessoas contribuindo para o projeto de automação.
 
`` Como os testes serão executados?``

Explore seus pensamentos sobre quando e como esses testes serão executados:

- Não há problema em ter alguém para iniciá-los quando necessário e relatar os resultados?
- Ou você deseja que eles sejam executados várias vezes ao dia em seu próprio trabalho de CI, onde todos têm visibilidade dos resultados?
- Ou você deseja que eles sejam integrados ao trabalho de CI do seu desenvolvimento, onde são executados sempre que alguém faz check-in de um novo código?

Cada um deles requer um certo nível de confiança e atenção concentrada.

Executar os testes automatizados localmente e relatar os resultados à equipe requer intervenção manual e, portanto, será realmente mais lento, mas o resultado relatado à equipe já foi triado e pode ser considerado preciso.

Executar os testes várias vezes ao dia em um trabalho de CI separado do desenvolvimento fornece feedback mais rápido, mas os resultados relatados não foram triados. Assim, os próprios testes devem ser escritos com um maior nível de proficiência e cuidado para garantir que não sejam inconsistentes e possam ser confiáveis.

E executar os testes como parte do processo de CI do desenvolvimento requer testes rápidos e confiáveis ​​que só falham quando o aplicativo em teste o provoca.

Eu recomendo passar gradualmente para essas fases. Começando com a execução local ou como parte de uma compilação de CI privada que não é exposta a outras pessoas. Isso permitirá que você aprenda mais sobre o que faz com que seus testes sejam esquisitos, incluindo peculiaridades sobre seu aplicativo.

Depois de descobrir que você mesmo pode confiar em seus testes, mude para um trabalho de CI separado que seja visível para todos, mas não afete os check-ins do desenvolvedor. Isso fortalece sua confiança no que você escreveu e também permite que outras pessoas comecem a confiar também.

`` Uma vez que você esteja muito confiante nos testes, só então você deve bloquear seus check-ins com eles, adicionando-os ao processo de CI de desenvolvimento.`` 

## Triagem e manutenção de testes automatizados

É melhor perceber desde o início que suas falhas de teste precisarão ser triadas e mantidas e planejar isso em sua estratégia. Novamente, um projeto de automação é um projeto de desenvolvimento de software e, à medida que o desenvolvimento de seu produto muda, seu código de automação também deve mudar. Eu não posso enfatizar isso o suficiente. Não é uma tarefa opcional. Seus testes automatizados precisarão ser triados e mantidos. Planeje adequadamente.

A boa notícia é que esta é uma grande oportunidade para outras pessoas da equipe ajudarem. À medida que seus desenvolvedores executam testes para verificar se seus novos recursos não quebraram nenhum dos existentes, eles podem ser responsáveis ​​pela triagem de quaisquer falhas. Idealmente, qualquer teste que falhar será devido a suas alterações e, portanto, eles podem corrigir seu código ou atualizar o teste para refletir as novas expectativas do aplicativo. No entanto, também esteja preparado para que testes não relacionados também falhem. Isso fornecerá aos desenvolvedores insights sobre coisas que causam testes inconsistentes e maneiras de melhorar a automatização do teste do aplicativo.

Os testadores manuais também são uma opção viável para triagem de falhas de automação. Especialmente aqueles que têm interesse em contribuir com a base de código de automação. Revisar falhas de teste, depurar o código de automação e atualizar o código quando necessário são ótimas oportunidades introdutórias à automação de teste.

Embora todos os desenvolvedores e testadores certamente possam ajudar na triagem e atualização de scripts de automação de teste, porque não é sua responsabilidade principal, ainda é necessário alguém para monitorar isso de forma consistente. Testes não monitorados são testes não confiáveis. Como sua equipe continua perdendo a confiança nos testes automatizados, eles tendem a confiar menos neles e o projeto de automação acaba morrendo.


## Questionário 

1. Qual NÃO é uma meta razoável para automação de teste?
- [ ] Libere recursos mais rapidamente
- [ ] Ativar teste contínuo
- [ ] Reduza o tempo de teste de regressão
- [x] Resolva todos os problemas de qualidade
 
 2. Qual é a primeira coisa que deve ser decidida antes de iniciar uma nova iniciativa de automação de teste?
- [ ] Qual linguagem de programação usar
- [x] Qual é o objetivo da automação
- [ ] Quantas pessoas são necessárias
- [ ] Qual estrutura usar

 3. Quais dessas tarefas estão associadas a um projeto de automação de teste?
- [ ] Autoria de testes automatizados
- [ ] Resultados do teste de monitoramento
- [ ] Manutenção de testes automatizados
- [x] Todos acima

 4. O que NÃO é uma consideração ao determinar quem escreverá os testes automatizados?
- [ ] Capacidade da pessoa
- [ ] Conjunto de habilidades da pessoa
- [x] Antiguidade da pessoa
- [ ] Desejo da pessoa

 5. É recomendável que seu primeiro teste automatizado seja imediatamente adicionado à integração contínua para começar a bloquear os check-ins do desenvolvedor:
- [ ] Verdadeiro
- [x] Falso


--------
<p align="center">
 Olá, sinta-se à vontade para mostrar apoio e dar a este repo<img src="https://img.icons8.com/fluency/20/null/star.png"/>estrela! Significa muito, obrigado :) 
</p>