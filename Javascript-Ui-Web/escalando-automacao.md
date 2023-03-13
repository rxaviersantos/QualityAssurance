<h1 align="center">
Escalando sua automação de teste
</h1>

Escrever testes automatizados que funcionam perfeitamente em um ambiente é um desafio por si só. Mas e quando você estiver pronto para dimensionar seu conjunto de testes para execução em vários ambientes, navegadores ou dispositivos.

## Vários ambientes

Em algum momento de sua jornada de automação, você pode precisar executar seus scripts automatizados em diferentes ambientes. No entanto, você pode descobrir que ambientes diferentes possuem informações diferentes – como o endereço IP ou URL, as credenciais de login e as informações do banco de dados.

Por esse motivo, é melhor extrair esses tipos de detalhes de seu projeto de automação e usar artefatos como arquivos de propriedades. Mesmo durante suas fases iniciais de automação para um único ambiente. Fazer essas considerações antecipadamente evitará que você precise refatorar mais tarde. Com o uso de arquivos de propriedades, você pode se concentrar no conteúdo do teste em vez de codificar vários caminhos condicionais.

Gerenciar dados de teste e todos os outros artefatos necessários para automação de teste também se torna mais desafiador ao executar em vários ambientes. Felizmente, soluções como a conteinerização ajudam a mitigar parte dessa carga.

## Navegador cruzado

Mesmo se estiver executando no mesmo ambiente, pode ser necessário executar seus testes de interface do usuário em vários navegadores. Esse é um dos benefícios de automatizar testes – para que seus testadores não precisem repetir os mesmos testes indefinidamente em vários navegadores e suas versões.

No entanto, gerenciar esses navegadores se torna uma nova tarefa para sua equipe. Leve isso em consideração e determine se o teste em alguns navegadores selecionados é suficiente. Se o risco for muito alto, considere o uso de soluções em nuvem que tenham uma variedade de navegadores de todas as versões diferentes prontamente disponíveis para execução a qualquer momento.


## Vários dispositivos

No mundo de hoje, os usuários tendem a acessar aplicativos de todos os tipos de dispositivos. Esse é outro fator a ser considerado ao desenvolver seus testes.

Considerações semelhantes ao teste entre navegadores precisam ser feitas para o teste de dispositivo. Você criará e manterá seu próprio farm de dispositivos ou é mais viável usar um serviço baseado em nuvem para isso?

Você também precisará considerar seu código de teste. Seus testes de nível de interface do usuário funcionam quando seu aplicativo está em layout responsivo? Alguns dos elementos foram substituídos por outros compatíveis com dispositivos móveis. Seu código de teste deve ser capaz de lidar com isso.

Que tal para aplicativos móveis nativos? Seu pacote de automação pode ser executado tanto para iOS quanto para Android? Você precisa escrever dois projetos de automação diferentes para dar suporte a cada um deles? Isso coloca um problema interessante. Existem bibliotecas, como Appium, que suportam escrever a automação de teste uma vez e executá-la em diferentes sistemas operacionais móveis. No entanto, se você espera que seus desenvolvedores ajudem na automação de teste, em qual idioma isso deve ser escrito? Se você tiver dois aplicativos nativos exclusivos, em que seus desenvolvedores iOS estão escrevendo em um idioma e os desenvolvedores Android estão escrevendo em outro idioma, não há um denominador comum aqui.

Além disso, se seus aplicativos móveis nativos forem distintamente diferentes – ou seja, diferentes recursos e diferentes caminhos de navegação, como você conquistará isso em seu código de teste?

Essas são decisões críticas que precisam ser tomadas desde o início, para que você não siga o caminho da automação de um desses dispositivos e, posteriormente, seja incapaz de dimensioná-lo para executar contra outros.

### Recursos

[Técnicas avançadas de automação de teste para aplicativos e sites responsivos](https://www.youtube.com/watch?v=20pJpyv5vQE  "Técnicas avançadas de automação de teste para aplicativos e sites responsivos")


## Questionário 

1. Quais são algumas maneiras pelas quais seus testes automatizados podem precisar ser dimensionados além de sua máquina local?
- [ ] Ambientes diferentes
- [ ] Dispositivos diferentes
- [ ] Navegadores diferentes
- [x] Tudo o que precede
 
 2. Ao dimensionar para diferentes ambientes, o gerenciamento de ______ deve ser considerado.
- [x] Dados específicos do ambiente
- [ ] Linguagens de programação
- [ ] Ferramentas de automação de teste
- [ ] APIs

 3. Qual é a melhor abordagem ao escolher em quais navegadores executar?
- [ ] Os testes são automatizados; executado em todos os navegadores!
- [ ] Execute apenas no navegador que é mais fácil de automatizar para
- [x] Considere suas necessidades de negócios e escolha seus navegadores de acordo
- [ ] Execute em todos os navegadores oferecidos pelo seu provedor de nuvem

 4. Quais considerações devem ser feitas para automação de teste móvel?
- [ ] Lidando com layouts responsivos
- [ ] Aplicativos móveis desenvolvidos por sua organização
- [ ] Ferramentas de automação apropriadas
- [x] Tudo o que precede



--------
<p align="center">
 Olá, sinta-se à vontade para mostrar apoio e dar a este repo<img src="https://img.icons8.com/fluency/20/null/star.png"/>estrela! Significa muito, obrigado :) 
</p>
