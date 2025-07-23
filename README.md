import os
from datetime import datetime

def obter_resposta(texto: str) -> str:
    comando: str = texto.lower()

    # Se o comando for exatamente "olá", "boa tarde" ou "bom dia"
if comando in ('olá', 'boa tarde', 'bom dia'):
        return 'Olá tudo bem!'  # Responde com uma saudação padrão

    # Se o comando for exatamente "como estás"
if comando == 'como estás':
        return 'Estou bem, obrigado!'  # Resposta sobre como está o bot

    # Se o comando for exatamente "como te chamas?"
 if comando == 'como te chamas?':
        return 'O meu nome é: Bot :)'  # O bot diz o seu nome

    # Se o comando for exatamente "tempo"
 if comando == 'tempo':
        return 'Está um dia de sol!'  # Dá uma resposta fixa sobre o tempo

    # Se o comando for "bye", "adeus" ou "tchau"
 if comando in ('bye', 'adeus', 'tchau'):
        return 'Gostei de falar contigo! Até breve...'  # Mensagem de despedida

    # Se a palavra "horas" estiver no comando
 if 'horas' in comando:
        return f'São: {datetime.now():%H:%M} horas'  # Mostra a hora atual

    # Se a palavra "data" estiver no comando
if 'data' in comando:
        return f'Hoje é dia: {datetime.now():%d-%m-%Y}'  # Mostra a data atual

    # Novas interações
if 'python' in comando:
        return 'Python é uma linguagem de programação incrível!'
 if 'ajuda' in comando:
        return 'Claro! Em que posso ajudar?'
 if 'piada' in comando:
        return 'Por que o computador foi ao médico? Porque estava com um vírus!'
if 'música' in comando:
        return 'Gosto de ouvir música clássica. E tu?'
if 'filme' in comando:
        return 'Adoro filmes de ficção científica!'
if 'desporto' in comando:
        return 'Gosto muito de futebol. Qual é o teu time favorito?'
if 'clima' in comando:
        return 'Hoje está ensolarado, ótimo para sair!'
if 'notícias' in comando:
        return 'Desculpa, não tenho acesso a notícias em tempo real.'
 if 'programar' in comando:
        return 'Programar é uma habilidade valiosa e divertida!'
 if 'livro' in comando:
        return 'Estou a ler um livro sobre inteligência artificial.'

    # Se nenhum dos casos acima for atendido
    return f'Desculpa, não entendi a questão! {texto}'  # Mensagem padrão de erro


def chat() -> None:
    print('Bem-vindo ao ChatBot!')
    print('Escreva "bye" para sair do chat')
    name: str = input('Bot: Como te chamas? ')
    print(f'Bot: Olá, {name}! \nComo te posso ajudar?')

while True:
        user_input: str = input('Tu: ')
        resposta = obter_resposta(user_input)
        print(f'Bot: {resposta}')

 if resposta == 'Gostei de falar contigo! Até breve...':
            break

 print('Chat acabou')
print()


def main() -> None:
    os.system('cls' if os.name == 'nt' else 'clear')
    chat()


if __name__ == '__main__':
    main()
