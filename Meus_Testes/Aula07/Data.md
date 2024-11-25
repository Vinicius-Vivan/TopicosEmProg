from datetime import datetime

def get_day_of_week_in_portuguese(weekday: int) -> str:
    """
    Retorna o nome do dia da semana em português baseado no índice.
    """
    days_of_week = {
        0: "Segunda-feira",
        1: "Terça-feira",
        2: "Quarta-feira",
        3: "Quinta-feira",
        4: "Sexta-feira",
        5: "Sábado",
        6: "Domingo"
    }
    return days_of_week.get(weekday, "Dia inválido")

def main() -> dict:
    """
    Retorna a data atual e o dia da semana em português.
    """
    # Obtém a data atual
    current_date = datetime.now()

    # Formata a data no formato dd/mm/aaaa
    formatted_date = current_date.strftime("%d/%m/%Y")

    # Obtém o dia da semana em português
    day_of_week = get_day_of_week_in_portuguese(current_date.weekday())

    # Retorna a data e o dia da semana
    return {
        "data_atual": formatted_date,
        "dia_da_semana": day_of_week
    }
