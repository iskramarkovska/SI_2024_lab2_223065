Iskra Markovska 223065

![image](https://github.com/iskramarkovska/SI_2024_lab2_223065/assets/120428909/e0bc9ab1-2398-4436-8372-07b95b12093f)

Цикломатската комплексност е 10  
E - N + 2P   
E = 36  
N = 28  
P = 1  
36 - 28 + 2 = 10  
  
Според Every Branch критериумот, јас избројав 8 тест случаи:  
  
1. True - True - True  
Влез: allItems = [new Item(null, "000000001", 100, 0.1)] payment = 100  
Случај кога името на предметот е null, баркодот не е и discount > 0  
  
2. True - True - False  
Влез: allItems = [new Item(null, "000000001", 100, 0)], payment = 100  
Случај кога името е null, баркодот не е и discount = 0  
  
3. True - False - True  
Влез: allItems = [new Item(null, null, 100, 0.1)], payment = 100  
Случај кога името е null, баркодот е null и discount > 0  
  
4. True - False - False   
Влез: allItems = [new Item(null, null, 100, 0.1)], payment = 100  
Случај кога името е null, баркодот е null и discount = 0  
  
5. False - True - True  
Влез: allItems = [new Item("item", "000000001", 100, 0.1)], payment = 100  
Случај кога името не е null, баркодот не е null и discount > 0  
  
6. False - True - False  
Влез: allItems = [new Item("item", "000000001", 100, 0.1)], payment = 100  
Случај кога името не е null, баркодот не е null и discount = 0  
  
7. False - False - True  
Влез: allItems = [new Item("item", null, 100, 0.1)], payment = 100  
Случај кога името не е null, баркодот е null и discount > 0  
  
8. False - False - False  
Влез: allItems = [new Item("item", null, 100, 0.1)], payment = 100  
Случај кога името не е null, баркодот е null и discount = 0
  
  
Целта на Multiple Condition критериумот е да ги покрие сите можни комбинации во  
if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0')  
Услови се:  
item.getPrice() > 300  
item.getDiscount() > 0  
item.getBarcode().charAt(0) == '0',  
секој услов може да биде true/false, значи има 2^3 = 8 тест случаи  
  
1. True - True - True  
item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0'  
  
2. True - True - False  
item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) != '0'  
  
3. True - False - True  
item.getPrice() > 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) == '0'  
  
4. True - False - False  
item.getPrice() > 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) != '0'  
  
5. False - True - True  
item.getPrice() <= 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0'  
  
6. False - True - False  
item.getPrice() <= 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) != '0'  
  
7. False - False - True  
item.getPrice() <= 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) == '0'  
  
8. False - False - False  
item.getPrice() <= 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) != '0'  
