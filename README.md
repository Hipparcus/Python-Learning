## Python Learning
 Todos os exercícios e projetos feitos no início da minha graduação em Astronomia, na UFRJ, quando aprendia **Python**.
 Para mais informações: [Veja este tópico que criei com base nesses exercícios.](https://road2tech.forumbrasil.net/t16-materiais-de-computacao-ufrj-python#22)

____________________________________________________________________


  * ***Updates:***
         *Update 06/06/2019*: Lista 2 gabarito número 1-b)
 ```
      def NomeQualquer(valor,dinheiro):
               quant=dinheiro/valor
               total=valor*quant
               troco=dinheiro-total
               print quant, troco
```
Ou pode-se usar input:"string " para o usuário colocar os valores das variáveis valor e dinheiro. Mas esse tipo de manipulação está mais para frente nos slides.

        Update 20/07/2019: Aula teórica 4 exercícios finais

  
def nome():
nome=raw_input("Digite seu nome para receber o numero de letras assim como sua primeira letra: ")
nome2=nome.strip()
nomesemesp=nome2.replace(" ","")
inverter=nome2[::-1]
return str(len(nomesemesp)) + " eh o numero de letras de teu nome e " + nome2[:1] + " eh a primeira letra!" + " Seu nome invertido eh: " + str(inverter) + ". As posicoes impares do nome dado sao: " + nome2[1::2]


*Update 29/07/2019:* Aula prática 6 número 9:
O gabarito mostra um código que parece meio estranho. Acontece que se a média da turma não estiver na lista de notas (ou seja, se a média for 5 mas ninguém da turma tirar esta nota) o list.index não vai funcionar. Para corrigir este problema apliquei list.append. Deste modo adicionamos a média calculada no final da lista e dps damos list.sort para colocar em ordem crescente. Depois usamos o index para recortar a lista a partir da primeira aparição da média e em seguida usamos list.remove (dessa forma se não houver esta média na lista das notas da turma, nós apenas adicionamos esta "nota falsa" na lista para podermos recorta-la então a removemos como se nada tivesse acontecido)

def questao_nove(notas):
    media=sum(notas)/len(notas)
    notas.append(media)
    list.sort(notas)
    aprovados=notas[list.index(notas,float(media)):]
    aprovados.remove(media)
    return aprovados
