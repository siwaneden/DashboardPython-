

## Índice

1. [convert_date_abreviated](#convert_date_abreviated)
2. [is_valid_date_adjusted](#is_valid_date_adjusted)

---

### convert_date_abreviated

```python
def convert_date_abreviated(date):
    date_str = str(date)
    day = date_str[:2]
    month = date_str[2:4]
    year = date_str[4:]
    return f"{day}/{month}/{year}"
Esta função converte datas no formato abreviado para o formato padrão DD/MM/AAAA. Ela recebe uma data no formato abreviado como uma string e retorna a data no formato padrão.

def is_valid_date_adjusted(date_str):
    date_str = date_str.split()[0]
    date_str = date_str.replace("-", "/")
    try:
        date_obj = datetime.strptime(date_str, '%d/%m/%Y')
        if 1923 <= date_obj.year <= 2023:
            return True
        return False
    except:
        return False
Esta função valida se uma data está em um formato aceitável e se o ano está dentro de um intervalo permitido (1923-2023). Ela retorna um valor booleano indicando a validade da data.
