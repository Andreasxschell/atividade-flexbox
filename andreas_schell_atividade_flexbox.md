# Gabarito de Flexbox

1. O contêiner é a caixa que abraça os elementos e os itens são os 2 filhos que ficam dentro dela, sendo que o display flex se escreve sempre no contêiner.

2. Se o CSS não define o flex-direction, o eixo principal fica na horizontal e corre da 1 direção, da esquerda para a direita.

3. A sobra de espaço é o vazio que fica na faixa quando o tamanho dos itens é menor que o espaço total, e se todo mundo tem flex-grow 0 ninguém distribui essa sobra.

4. O valor padrão de flex-grow é 0, o que significa que o item não cresce para ocupar o espaço sobrando.

5. Na analogia da pizza, a mesa é o contêiner, o prato de cada pessoa é o tamanho inicial do item, a sobra são os 2 pedaços extras na caixa e o peso do flex-grow é a proporção de pedaços que cada um vai ganhar.

6. Para fazer a marca ocupar toda a sobra enquanto os links ficam com o tamanho do texto, você coloca flex-grow 1 diretamente na marca.

7. A soma dos pesos é 2 + 3 + 1 que dá 6 partes, o valor de 1 parte é 600 / 6 que dá 100 pixels, e a largura final fica 200 pixels para o primeiro, 300 para o segundo e 100 para o terceiro.

8. O espaço inicial ocupado é 300 pixels, sobrando 300 pixels, a soma dos pesos é 3 partes, e o valor de 1 parte é 100 pixels, resultando em 100 pixels para o primeiro, 200 para o segundo e 300 para o terceiro.

9. O flex-shrink entra em ação quando falta espaço na faixa, e o seu valor padrão é 1.

10. Como falta 200 pixels e ambos têm o mesmo tamanho e flex-shrink 1, o corte é dividido meio a meio, resultando em 300 pixels para cada 1.

11. Se o primeiro item tem flex-shrink 0 ele mantém seus 400 pixels inteiros, o segundo item absorve todo o excesso de 200 pixels ficando com 200 pixels, e o conjunto cabe perfeitamente na faixa somando 600 pixels.

12. Um exemplo prático é 1 foto de perfil ou avatar fixo, porque a gente não quer que a imagem fique esmagada se a tela diminuir.

13. O flex-basis é o ponto de partida do item, e entre width de 200 pixels e flex-basis de 10rem, o flex-basis é o que vale como medida inicial.

14. Usar flex-basis 0 faz o navegador considerar o tamanho inicial como 0, transformando a faixa inteira em sobra para ser distribuída pelos pesos do flex-grow.

15. Para a tabela de atalhos, flex initial tem grow 0, shrink 1 e basis auto; flex 1 tem grow 1, shrink 1 e basis 0%; flex auto tem grow 1, shrink 1 e basis auto; e flex none tem grow 0, shrink 0 e basis auto.

16. Com flex 1 os 2 partem do 0 e dividem os 600 pixels meio a meio resultando em 300 pixels para cada 1, enquanto com flex auto eles partem de 100 e 300 pixels e dividem a sobra de 200 pixels igualmente resultando em 200 e 400 pixels, porque o primeiro ignora o conteúdo e o segundo respeita o tamanho natural.

17. É verdadeiro porque se os itens têm exatamente o mesmo conteúdo e tamanho base, a distribuição do espaço extra rola de forma simétrica e dá o mesmo resultado em ambos.

18. A propriedade padrão que segura o item é o min-width auto que impede ele de ficar menor que o conteúdo, e o ajuste que solta é definir min-width 0.

19. Esse problema costuma aparecer quando colocamos 1 texto longo ou URL sem espaços ao lado de 1 menu fixo no miolo, fazendo o texto empurrar a caixa para fora da tela.

20. A ordem na tela é C, A e B. A ordem de foco ao apertar a tecla Tab continua sendo A, B e C. E isso importa para leitores de tela porque eles seguem o código HTML e não a ordem visual do Flexbox.

21. O valor padrão de order é 0, e entre order -1 e order 2, o -1 aparece primeiro.

22. Com align-self flex-end o filho vai para o fim do eixo cruzado ignorando o pai, e com align-self auto ele segue o estiramento padrão do align-items do pai.

23. Você usa align-items no pai para alinhar todo mundo de 1 vez, e align-self no filho para mudar o alinhamento de 1 item específico.

24. Os itens da pagina são o header, a div miolo e o footer, e os itens do miolo são o aside e o main.

25. O miolo precisa ter display flex para conseguir organizar os seus próprios filhos lado a lado, já que ser item da página só define a posição dele em relação ao topo e rodapé.

26. A primeira linha organiza a página em coluna ocupando no mínimo 100% da altura da tela, a segunda transforma o miolo em linha e faz ele crescer para ocupar o espaço vertical livre, a terceira fixa o menu lateral em 10rem sem deixar crescer nem encolher, e a quarta faz o texto principal crescer com min-width 0 para não estourar a faixa.

27. O erro foi colocar flex-grow 1 no contêiner sendo que ele pertence aos itens, e a correção é mover a propriedade para os elementos de dentro.

28. As 2 formas são usar min-width 0 para quando o travamento é causado por textos ou conteúdos internos, e usar flex-shrink para quando o item é largo demais e precisa ser esmagado proporcionalmente.

29. O flex-basis define o tamanho inicial do item antes de crescer ou encolher, o flex-grow controla o quanto o item estica para aproveitar o espaço sobrando, o flex-shrink define o quanto o item aceita encolher quando falta espaço, o order muda a ordem visual dos itens na tela, e o align-self permite que 1 item específico fuja do alinhamento geral do pai no eixo cruzado.