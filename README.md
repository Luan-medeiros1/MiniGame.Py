Jogo de teste de matemática
Descrição
Este é um jogo de perguntas e respostas matemáticas em Python que desafia o jogador com operações matemáticas básicas. O projeto consiste em dois arquivos principais:

game.py: Contém a lógica principal do jogo, incluindo as funções maine play.
calculate.py: Localizado na pasta de modelos, define a Calculateclasse, responsável por gerar operações matemáticas aleatórias com base em uma dificuldade escolhida.
Calcular Classe
A Calculateclasse possui os seguintes atributos:

difficulty: Nível de dificuldade escolhido pelo jogador (1 a 4).
value1e value2: Números gerados aleatoriamente para as operações.
operation: Número inteiro representando a operação a ser realizada (1 = somar, 2 = subtrair, 3 = multiplicar).
result: Resultado da operação gerada.
Métodos
        show_operation():Exibe a operação gerada.
        check_result(response: int) -> bool:Verifica se a resposta do usuário está correta.
    
jogo.py
O game.pyarquivo controla a execução do jogo, interagindo com o jogador e gerenciando os pontos acumulados.

Como correr
        python game.py
    
Características
        main():Função principal que inicia o jogo.
        play(points: int) -> None:Função que implementa a lógica do jogo, permitindo ao jogador realizar operações matemáticas.
    
Exemplo de uso
        from models.calculate import Calculate

        def main() -> None:
            points: int = 0
            play(points)

        def play(points: int) -> None:
            difficulty: int = int(input('Enter the desired difficulty level [1, 2, 3, or 4]: '))

            calc: Calculate = Calculate(difficulty)

            print('Enter the result for the following operation: ')
            calc.show_operation()

            result: int = int(input())

            if calc.check_result(result):
                points += 1
                print(f'You have {points} point(s).')

            continue_game: int = int(input('Do you want to continue playing? [1 - yes, 0 - no] '))

            if continue_game:
                play(points)
            else:
                print(f'You finished with {points} point(s).')
                print('Until next time!')

        if __name__ == '__main__':
            main()
    
calcular.py
O calculate.pyarquivo define a Calculateclasse, que encapsula a lógica para gerar e verificar operações matemáticas.

Uso
        from models.calculate import Calculate

        # Create an instance of the Calculate class with the desired difficulty
        calc = Calculate(difficulty=2)

        # Display the generated operation
        calc.show_operation()

        # Wait for the user's response
        response = int(input('Your response: '))

        # Check if the response is correct
        if calc.check_result(response):
            print('Correct answer!')
        else:
            print('Wrong answer.')
    
Calcular Classe
A Calculateaula gera operações matemáticas aleatórias com base na dificuldade escolhida.

Propriedades
difficulty:Número inteiro representando o nível de dificuldade (1 a 4).
value1e value2:inteiros gerados aleatoriamente.
operation:Representa a operação a ser realizada (1 = somar, 2 = subtrair, 3 = multiplicar).
result:Resultado da operação gerada.
Métodos
        show_operation():Exibe a operação gerada.
        check_result(response: int) -> bool:Verifica se a resposta do usuário está correta.
    
Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir problemas ou enviar solicitações pull.
