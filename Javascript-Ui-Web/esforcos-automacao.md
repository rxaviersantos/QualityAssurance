<h1 align="center">
Preparando seus esforços de automação de teste para o futuro
</h1>

Sem uma estratégia clara em mente, muitas equipes cometem o erro de automatizar seus testes para a situação atual. Talvez você esteja apenas começando e tenha cerca de uma dúzia de testes executados localmente. Você não vê os problemas que seu código de teste mal escrito pode apresentar.

No entanto, quando você chega a 100 testes, de repente, fica muito claro como suas decisões de design foram falhas. Agora você precisa encontrar tempo para refatorar seu projeto de automação de teste.

Neste capítulo, compartilharei com você algumas considerações de design que você pode ter em mente no início de sua jornada de automação. Saber essas coisas com antecedência ajudará você a preparar seu projeto de automação de teste para o futuro e a economizar muito tempo e dor de cabeça.

## Correndo em paralelo

Quando você tem apenas um punhado de testes automatizados, executá-los sequencialmente não parece grande coisa. No entanto, à medida que o número de testes automatizados cresce, mais tempo levará para que todo o seu conjunto de testes seja concluído. Uma solução para isso é executar os testes em paralelo. No entanto, isso não é tão simples quanto apertar um botão. Seus testes devem ser projetados para serem executados dessa maneira.

Para começar, você não deve ter nenhum dos seus testes dependentes uns dos outros. Se você confiar que o Teste 1 será executado antes do Teste 2, esses dois testes não poderão ser executados em paralelo. Portanto, certifique-se de projetar todos os seus testes para serem independentes. Qualquer configuração ou limpeza deve ser isolada dentro do teste.

Você também deve evitar modificar os dados de teste dos quais outros testes podem depender. Se o Teste 1 altera o valor de um registro e o altera de volta ao seu valor original depois de concluído, ainda existe o risco do Teste 2 ser executado no momento em que o valor foi alterado. Portanto, o teste 2 falha. Para mitigar isso, qualquer teste que precise alterar dados de teste deve ser o único teste usando esses dados.

Em terceiro lugar, objetos e variáveis ​​usados ​​por vários testes devem ser declarados de maneira thread-safe, o que significa que não devem ser globais ou estáticos – pois seus valores podem mudar.

## Codificação limpa

Embora seu projeto de automação consista em código de teste, isso não significa que você pode jogar a cautela ao vento e ignorar as práticas de codificação limpa. Lembre-se, automação de teste é desenvolvimento de software. Tem que ser ampliado e mantido, por isso é melhor desenvolvê-lo em um assunto que suporte ambos.

Evite a duplicação excessiva de código, classes e métodos longos, espera ineficiente nos testes e outras más práticas conhecidas como code smells. Em vez disso, adote abordagens que permitam a reutilização e manutenção do código.

## Padrões de design

Familiarize-se com os padrões de design que são especialmente benéficos para projetos de automação de teste, como:

    - Modelo de objeto de página
    - Roteiro
    - Fluente
    - Construtor
    - solteiro
    - Fábrica
    - Fachada


Você não precisa usar todos eles, na verdade, alguns são alternativas entre si, mas ter conhecimento sobre eles ajuda a saber quais são os melhores para o seu projeto de automação de teste.

## Questionário 

1. Qual das opções a seguir NÃO é uma consideração necessária para testes automatizados preparados para o futuro?
- [ ] Utilizando padrões de design
- [ ] Práticas de codificação limpa
- [ ] Ativando a execução paralela de testes
- [x] Mantendo o código-fonte em sua máquina
 
 2. Para executar testes em paralelo, seus testes devem:
- [x] Seja thread-safe
- [ ] Confie em outros testes
- [ ] Modifique os dados de teste compartilhados quando necessário
- [ ] Definir objetos/variáveis ​​compartilhados como estáticos

 3. Qual das opções a seguir é uma violação das práticas de codificação limpa?
- [ ] Testes curtos
- [x] Duplicação excessiva de código
- [ ] Métodos curtos
- [ ] Técnicas de espera eficientes

 4. Para preparar seus testes para o futuro, quais padrões de projeto você deve usar?
- [ ] Todos eles
- [ ] Nenhum deles
- [x] As que fazem sentido para o seu projeto
- [ ] Apenas um


--------
<p align="center">
 Olá, sinta-se à vontade para mostrar apoio e dar a este repo<img src="https://img.icons8.com/fluency/20/null/star.png"/>estrela! Significa muito, obrigado :) 
</p>