<h1 align="center">
Desenvolvendo para automação de teste
</h1>

## Pirâmide de Automação de Testes

Um modelo que descreve três níveis nos quais os testes podem ser automatizados: unidade, serviços e interface do usuário.

<p align="center">
  <img alt="Pirâmide de automação" src="https://user-images.githubusercontent.com/85380530/224585554-136e1ebe-f9aa-4d08-8c09-6e180a33c4a1.png" width="80%">
</p>

``Se um dos motivos pelos quais você está automatizando testes é ter um feedback rápido, convém projetar seus testes automatizados para serem executados o mais rápido possível. Uma maneira de fazer isso é automatizar os testes o mais próximo possível do código de produção.`` 

### Unit

O nível da unidade está mais próximo do código de produção. Os testes que são automatizados neste nível são chamados de Testes de Unidade e são rápidos de escrever e também rápidos de executar. Para relembrar, os testes de unidade são pequenos testes modulares que verificam a lógica de funções individuais sem a necessidade de integração de outras funcionalidades, bancos de dados ou interfaces de usuário.
Além de serem rápidos, os testes de unidade também são capazes de identificar a função exata em que existe um bug. Portanto, a maior parte dos testes automatizados deve ser escrita nesse nível. Isso se alinha com o objetivo de feedback rápido.

Esses são os testes mais bem escritos por seus desenvolvedores de produto como parte de seu trabalho de desenvolvimento de recursos. No entanto, se os testes forem posteriormente identificados como bons candidatos para automação, mas não foram incluídos pelos próprios desenvolvedores, esses testes ainda podem ser adicionados nesse nível por qualquer pessoa com conhecimento. Só porque o desenvolvedor não o adicionou ao nível da unidade, não significa que ele deva ser automatizado em um nível superior.


### Services 

O nível de serviços está um pouco mais distante do código em si e se concentra na funcionalidade que o código fornece, mas sem uma interface com o usuário. Os testes automatizados nesse nível podem fazer chamadas para as APIs do produto e/ou lógica de negócios para verificar a integração de várias funções individuais.
Este nível deve conter o segundo maior número de testes automatizados após o nível de unidade.

### Ui

O nível mais distante do código de produção é o nível de interface do usuário. Os testes escritos nesse nível enfrentam desafios únicos, pois demoram mais para serem escritos, demoram mais para serem executados e dependem da consistência da IU. Devido a essa despesa, esse nível deve conter o menor número de testes automatizados.
Ao considerar um teste para automação, determine quais informações o teste precisa verificar e escolha o nível mais baixo da pirâmide possível para escrever o teste. Quanto mais baixo o nível, mais rápido o teste – mantendo assim o objetivo de feedback rápido.

Agora, isso parece prático na teoria, mas quando a equipe está criando recursos no nível da interface do usuário, é tentador acreditar que tudo deve ser automatizado no nível da interface do usuário. Entendo. Você deseja verificar se o aplicativo tem a aparência esperada e se os controles funcionam.

Você certamente deve verificar sua IU, mas todas as etapas necessárias para o caso de teste não precisam ser executadas nesse nível.

### Exemplo 1:

<p align="center">
  <img alt="Página web de produtos" src="https://user-images.githubusercontent.com/85380530/224586582-6da29077-c42e-42ef-a5b6-c0f9b6d597d4.png" width="80%">
</p>

Digamos que sua equipe acabou de criar um novo recurso de pesquisa. Naturalmente, você deseja verificar se, ao pesquisar produtos, os resultados corretos são retornados, se os resultados aparecem como deveriam e se qualquer outra filtragem, classificação, seleção de coluna ou paginação está funcionando.
Se você estiver automatizando um teste de pesquisa, concordo – automatize-o no nível da interface do usuário e execute todas essas verificações no nível da interface do usuário.

No entanto, se você precisar automatizar vários testes de pesquisa, pergunte-se se todos eles precisam ser executados nesse nível caro. Ou você pode automatizar um no nível da interface do usuário e automatizar o restante deles em um nível inferior. Neste ponto, você já verificou os componentes da interface do usuário e agora o que está realmente exercitando é a funcionalidade do algoritmo de pesquisa. Isso pode ser verificado no serviço ou mesmo no nível da unidade.

### Exemplo 2: Em que você deseja adicionar um produto ao carrinho de compras.

<p align="center">
  <img alt="Página web de produtos" src="https://user-images.githubusercontent.com/85380530/224586748-dfe900d9-dbd8-4652-be12-2be125d494a3.png" width="80%">
</p>

As etapas do cenário incluem:

    1. Procurando o produto
    2. Olhando através dos resultados da pesquisa para encontrar o produto que você deseja
    3. Clicando no produto
    4. Clicando no botão Adicionar ao Carrinho
    5. Clicar no ícone do carrinho para acessar o carrinho
    6. Verificando se o item está realmente no carrinho

Automatizar todas essas etapas no nível da interface do usuário é arriscado. Se alguma dessas etapas falhar devido à fragilidade da navegação na interface do usuário, seu teste não chegará à etapa que realmente importa.

Você já adicionou um teste de pesquisa no nível da interface do usuário ao seu pacote, portanto, pode ignorá-lo neste novo cenário. Em vez disso, procure costuras - ou atalhos - em seu aplicativo que facilitem a automação.

Neste exemplo, em vez de pesquisar o produto, você pode ir direto para a URL do produto em seu teste automatizado. Essa é a costura e isso economizará muito tempo e reduzirá alguns dos riscos de usar a interface do usuário, eliminando as etapas possíveis. Além disso, você está eliminando a dependência do recurso de pesquisa que funciona para este teste. O teste de adicionar algo ao carrinho não tem nada a ver com a Pesquisa. No entanto, se você automatizar a pesquisa como parte desse cenário, esse teste falhará e você será impedido de verificar o objetivo desse teste.

### Exemplo 3: Digamos que você tenha um teste que verifica se você pode aumentar a quantidade de um produto no carrinho de compras.

<p align="center">
  <img alt="Página web carrinho de compras" src="https://user-images.githubusercontent.com/85380530/224587583-399d4bd9-9cb7-4ccc-9e78-15b423521bdf.png" width="80%">
</p>

Pensando nesse cenário, as etapas podem incluir:

    1. Procurando o produto
    2. Olhando através dos resultados da pesquisa para encontrar o produto que você deseja
    3. Clicando no produto
    4. Clicando no botão Adicionar ao Carrinho
    5. Clicar no ícone do carrinho para acessar o carrinho
    6. Aumente a quantidade do produto
    7. Verificando o carrinho


Novamente, o processo de pesquisar e até mesmo adicionar o produto ao carrinho não precisa necessariamente ser feito no nível da interface do usuário. Ao fazê-los lá, você está adicionando tempo, dependência, redundância (porque você já tem um teste de nível de interface do usuário para isso) e exposição à fragilidade de seus testes.

Você pode utilizar uma costura, como uma chamada de serviço da Web que adiciona o produto ao carrinho, vá direto para a URL do carrinho e comece seu teste. Isso é muito mais rápido e menos propenso a falhar por uma causa não relacionada

### Costuras

Já falamos um pouco sobre costuras. São atalhos dentro do aplicativo que facilitam muito a automatização dos testes. Algumas costuras são fornecidas no aplicativo por padrão - como URLs exclusivos para várias páginas. Utilize-os sempre que possível em seus testes automatizados, em vez de tentar navegar na interface do usuário por meio de itens de menu e vários fluxos de cliques.

Costuras adicionais podem ser fornecidas por desenvolvedores, como serviços da Web, que permitem que seu código de teste ignore a interface do usuário e envie solicitações HTTP rápidas para o aplicativo. Eles são ótimos para configuração de pré-requisito, verificação de dados e limpeza após a conclusão do teste. Este é um excelente exemplo de como seus desenvolvedores podem contribuir para melhorar a automatização do teste do aplicativo e, portanto, permitir testes mais rápidos e confiáveis.

A exposição a funções de negócios também pode ser útil. Por exemplo, em vez de passar pela interface do usuário e navegar até uma página para clicar em um botão, o código de teste pode chamar diretamente a função que executa a ação. Esse tipo de automação seria considerado automação de nível de serviço. Para automatizar dessa maneira, seu código de teste precisaria ser capaz de acessar a lógica do aplicativo sem uma interface de usuário.

### Localizadores de IU

Para os testes que precisam ser executados no nível da interface do usuário, os testes precisarão interagir com o aplicativo acessando seus elementos HTML. Uma das principais causas de testes inconsistentes é a ausência ou falta de confiabilidade de identificadores para esses elementos HTML.

Quando os desenvolvedores criam novos elementos da Web, é extremamente importante que adicionem identificadores a esses elementos. Isso pode ser na forma de um atributo de ID, atributo de nome ou um atributo personalizado que é exclusivamente para fins de automação de teste.

Isso não é algo que normalmente é ensinado aos desenvolvedores front-end enquanto eles estão aprendendo a codificar, então é necessário fazer disso parte da cultura de sua equipe. Embora informe aos desenvolvedores que isso é necessário, ainda é relativamente fácil esquecer de fazer. Portanto, implemente outros processos para impor esse comportamento.

As opções incluem:

- Adicionando uma regra ao linter de código da equipe que sinaliza quaisquer elementos que não contenham um atributo de ID ou, melhor ainda, o atributo de teste personalizado
- Procurando ativamente por essas omissões durante a revisão do código
- Reunir-se com os desenvolvedores com antecedência e rotular uma maquete dos elementos com os atributos necessários para a automação de teste

[Recursos](https://angiejones.tech/hybrid-tests-automation-pyramid/  "TESTES HÍBRIDOS: CONFUNDINDO AS LINHAS DA PIRÂMIDE DE AUTOMAÇÃO")


## Questionário 

1. Qual das opções a seguir NÃO melhora a automatização do teste?
- [ ] Costuras de código
- [ ] Identificadores de elementos da interface do usuário
- [ ] Atalhos de aplicativos
- [x] Carrinhos de compras
 
 2. Qual das opções a seguir NÃO é um nível da Pirâmide de Automação de Teste?
- [ ] Serviços
- [] UI
- [ ] Unidade
- [x] Javascript

 3. Em que nível você deve automatizar seu teste para que ele seja executado o mais rápido possível?
- [x] O mais próximo possível do código de produção
- [ ] O mais longe possível do código de produção
- [ ] O nível mais fácil de chegar
- [ ] Qualquer nível

 4. A ausência de identificadores de elementos confiáveis ​​afeta que tipo de testes?
- [ ] Unidade
- [ ] Serviçoa
- [ ] API
- [x] UI

 5. Qual NÃO é um exemplo de utilização de uma costura de código?
- [x] Navegar na IU da mesma forma que um usuário faria
- [ ] Chamando uma função de nível de negócios diretamente
- [ ] Chamando uma solicitação HTTP para ignorar a interface do usuário
- [ ] Evitando a navegação iniciando páginas de aplicativos específicos

--------
<p align="center">
 Olá, sinta-se à vontade para mostrar apoio e dar a este repo<img src="https://img.icons8.com/fluency/20/null/star.png"/>estrela! Significa muito, obrigado :) 
</p>


