# Final_test
1. Создать репозиторий на GitHub
2. Нарисовать блок-схему алгоритма (можно обойтись блок-схемой основной содержательной части, если вы выделяете её в отдельный метод)
3. Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)
4. Написать программу, решающую поставленную задачу
5. Использовать контроль версий в работе над этим небольшим проектом (не должно быть так, что всё залито одним коммитом, как минимум этапы 2, 3, и 4 должны быть расположены в разных коммитах)

Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

Примеры:
[“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]
[“1234”, “1567”, “-2”, “computer science”] → [“-2”]
[“Russia”, “Denmark”, “Kazan”] → []

решение: 

//задаем переменные
      string[] mass;
      int count; 
      string s;
      string[] mass2;
      string[] mass3;
      
      Console.WriteLine("Введите строки массива");
      count = 0;
      mass = new string[count];

//заполняем массив строками (кол-во определяется пользователем)
      do
      {
        s = Console.ReadLine();
        if (s!="")
        {
          count++;
          mass2 = new string[count];
          for (int i = 0; i < mass2.Length - 1; i++)
            mass2[i] = mass[i];
          mass2[count - 1] = s;
          mass = mass2;
        }
      } while (s != "");
      
//Переносим строки с длиной не более 3х символов в новый массив
      count = 0;
      mass3 = new string[count];
      for (int i = 0; i < mass.Length; i++) {
      if (mass[i].Length <= 3) {
            count++;
            mass2 = new string[count];
            for (int j = 0; j < mass2.Length - 1; j++)
                mass2[j] = mass3[j];
            mass2[count - 1] = mass[i];
            mass3 = mass2;

      }
      }
// Выводим итоговый массив на печать
    for (int i = 0; i < mass3.Length; i++)
    Console.WriteLine("mass3[{0}] = {1}", i, mass3[i]);
    Console.ReadKey();
  }
}


Спасибо за внимание! :)
