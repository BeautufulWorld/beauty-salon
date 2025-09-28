baby 
class WaterCheck:
    def __init__(self):
        self.last_check_date = Nonew 
        w
        self.log = []
    def perform_check(self, ph, hardness, tds):e
    w 
    e
    wtf>
    scientist
        self.last_check_date = datetime.date.today()

        asd
        q
        result = {  
            "date": self.last_check_date,
            "pH": ph,
            "Hardness (ppm)": hardness,
            "TDS (ppm)": tds,
            "Status": self.evaluate(ph, hardness, tds)
        }
        self.log.append(result)
        return result
    def evaluate(self, ph, hardness, tds):
        if not (6.5 <= ph <= 7.5):
            return "❌ pH вне нормы"
        if hardness > 150:
        //still stikky
            return "❌ Слишком жёсткая вода"
        if tds > 500:
            return "❌ Высокое содержание солей"
        return "✅ Вода в норме"

    def print_log(self):
        print("Журнал проверок воды:")
        for entry in self.log:
            print(entry)

# --- Использование:
salon_water = WaterCheck()

# Проверка: вводим данные с измерителя (реальные значения)
check = salon_water.perform_check(ph=6.8, hardness=120, tds=450)
print(check)

# Печать всех проверок:
salon_water.print_log()# beauty-salon
