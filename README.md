
 # Controle-de-N-veis-de-gua
 # Atividade Etec 

from colorama import init, Fore, Style
init(autoreset=True)
niveis = [
    "nivel 1 - Muito baixo (CRÍTICO)",
    "nivel 2 - Baixo",
    "nivel 3 - Moderado",
    "nivel 4 - Alto",
    "nivel 5 - Muito alto (AlERTA)"
]
def definir_cor(nivel):
    if nivel == 1:
        return Fore.RED
    elif nivel == 2:
        return Fore.YELLOW
    elif nivel == 3:
        return Fore.GREEN
    elif nivel == 4:
        return Fore.CYAN
    elif nivel == 5:
        return Fore.BLUE
    else:
        return Fore.WHITE
    
nivel_atual = int(input("Digite o nível de risco (1 a 5): "))
if 1 <= nivel_atual <= 5:
    cor = definir_cor(nivel_atual)
    print(cor + niveis[nivel_atual - 1])
else:
    print(Fore.WHITE + "Nível inválido. Por favor, digite um número entre 1 e 5.")
       
print(Style.RESET_ALL)
