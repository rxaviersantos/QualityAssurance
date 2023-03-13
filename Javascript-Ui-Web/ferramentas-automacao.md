<h1 align="center">
Ferramenta para automação de teste
</h1>

Você definiu sua estratégia para automação de teste, implementou práticas para criar uma cultura que suporte sua estratégia, revisou os principais conceitos sobre a criação de testes confiáveis, além de garantir que seu aplicativo possa ser automatizado. Agora é um bom momento para considerar as ferramentas para seu projeto de automação de teste.

Antes de escolher suas ferramentas, é importante considerar quem as usará.

Se você não tiver programadores que contribuam ativamente para a automação de teste, criar sua própria estrutura de automação de teste pode não ser uma opção viável. Lembre-se, automação de teste é desenvolvimento de software. Se a sua ideia é fazer com que seus testadores aprendam a codificar e, em seguida, criem um novo projeto de desenvolvimento de software, perceba que isso exige um pouco de investimento em educação para eles. Sua organização deve fornecer uma grande quantidade de suporte para isso.

Se isso parecer irrealista, existem ferramentas sem código no mercado que permitem que seus testadores registrem seus cenários e os executem como parte do teste de regressão. Embora o conhecimento de programação não seja necessário, observe que você também precisará planejar a triagem e a manutenção.

Se você quiser que seus desenvolvedores ou engenheiros de automação façam a automação, uma solução codificada é de longe uma opção melhor. Permite maior controle e flexibilidade.

O mínimo que você precisa para seu projeto de automação de teste é uma ferramenta de interação e uma ferramenta de validação.

Lembre-se, temos três níveis: testes de unidade, testes de serviço e testes de interface do usuário. Vamos falar sobre a interação para cada um desses níveis.

## Interação

Para testes de unidade e testes de serviço que chamam funções de produção, eles devem ser escritos na mesma linguagem de programação e residir no mesmo projeto que o código de produção. A interação é simplesmente a chamada para essas funções.

Para seus outros testes, você tem mais opções. Os testes de nível de serviço que chamam APIs precisarão ser capazes de executar as solicitações HTTP e ler as respostas. Portanto, você deve procurar uma linguagem de programação que facilite isso ou bibliotecas que cuidem do trabalho da placa da caldeira para você.

Para testes de interface do usuário, você precisará de uma biblioteca de navegação que forneça a capacidade de interagir com os elementos HTML de seu aplicativo. Usar uma ferramenta que suporte a linguagem de programação em que seu aplicativo foi escrito é uma ideia razoável. No entanto, você também deve considerar como é fácil contratar essa linguagem de programação, caso queira contratar mais engenheiros de automação; e também considere o quão amplamente suportada essa linguagem de programação é por ferramentas de automação de teste. É realmente benéfico usar ferramentas que tenham uma abundância de suporte e recursos educacionais. Portanto, se sua equipe estiver usando uma linguagem de programação obscura com suporte e recursos limitados, essa pode não ser a melhor escolha para seu projeto de automação. Outro fator a considerar são os navegadores e dispositivos nos quais você precisa executar sua automação de teste.

## Validação

Você também precisará incluir bibliotecas de validação. Estas são ferramentas que permitirão que você transforme seu código em um teste que pode ser aprovado ou reprovado. Existem várias opções para a variedade de coisas que você precisa verificar, incluindo funcional, visual, acessibilidade, segurança, etc.

Este é o mínimo necessário para o seu projeto de automação: uma forma de executar os testes e uma forma de verificá-los.

No entanto, você certamente pode tornar seu projeto mais sofisticado adicionando uma biblioteca de relatórios que mostra capturas de tela e possivelmente até vídeos de falhas de teste ou a integração de arquivos de cenário Gherkin se sua equipe já estiver praticando o Behavior Driven Development. E se o seu objetivo final é executar os testes como parte do CI, convém escolher ferramentas que permitam essa integração.

## Questionário 

1. Qual destas é uma consideração importante para escolher uma ferramenta para automação de teste?
- [ ] Quem vai usá-los
- [ ] Suporte e recursos disponíveis
- [ ] Compatibilidade com linguagens de programação, dispositivos e navegadores necessários
- [x] Tudo o que precede
 
 2. Ao considerar uma linguagem de programação para automação de teste, qual fator pode ser um impedimento?
- [ ] Os desenvolvedores usam a mesma linguagem
- [ ] Fácil de aprender
- [x] Não suportado pela maioria das ferramentas de automação de teste
- [ ] Ótima documentação

 3. Qual das opções a seguir NÃO é um exemplo de testes automatizados interagindo com o aplicativo?
- [ ] Chamando funções de nível de produto
- [ ] Fazendo solicitações HTTP aos serviços do produto
- [ ] Navegando na IU do produto
- [x] Relatando os resultados do teste

 4. O objetivo das bibliotecas de validação é:
- [x] Ativar um teste para passar ou falhar
- [ ] Adicionar testes à integração contínua
- [ ] Fazer chamadas de API
- [ ] Navegar na IU




--------
<p align="center">
 Olá, sinta-se à vontade para mostrar apoio e dar a este repo<img src="https://img.icons8.com/fluency/20/null/star.png"/>estrela! Significa muito, obrigado :) 
</p>
