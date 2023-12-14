# Анализ данных в разработке игр [in GameDev]
Отчет по лабораторной работе #4 выполнил(а):
- Колчин Андрей Алексеевич
- РИ220950
  
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
- Реализовать персептрон в Unity
- Сделать выводы о корректности его работы

## Задание 1
### В проекте Unity реализовать перцептрон, который умеет производить вычисления:
### - OR | дать комментарии о корректности работы
### - AND | дать комментарии о корректности работы
### - NAND | дать комментарии о корректности работы
### - XOR | дать комментарии о корректности работы
  
Ход работы:
- Создадим пустой 3D проект на Unity и добавим туда пустой объект
- Добавим к пустому объекту предложенный файл Perceptron.cs
- Запустим проект на разных тренировочных данных,используя 8 эпох обучения, и сделаем выводы    
![Image alt](https://github.com/prepref/UrFU-GameAnalysis/raw/main/github-screenshots/workshop4/empty_object.png)

Вывод OR:  
  - Поэкспериментировав я выяснил 1,2,3 эпох для обучения точно недостаточно. Начиная с 4 эпохи модель начинает +- обучаться. Но для того чтобы модель полностью и правильно обучилась достаточно 5 эпох. Работа корректна модели для OR.   
    5 эпох:  
    ![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/step1.png)    
  
Вывод AND:  
  - Поэкспериментировав я выяснил 1,2,3,5,7 эпох для обучения точно недостаточно. C 8 эпохи модель более менее начинает обучаться и начиная с 9 эпохи обучается правильно. Работа корректна модели для AND.         
    9 эпох:  
    ![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/step2.png)    
  
Вывод NAND:  
  - Поэкспериментировав я выяснил, что начиная с 9 эпохи модель начинает +- обучаться. 10 эпох достаточно, чтобы модель обучилась правильно. Работа корректна модели для NAND.      
    ![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/step3.png)    
  
Вывод XOR:  
 - Во-первых XOR - не линейная функция, а значит сколько бы эпох мы не поставили, модель не сможет обучиться. Работа некорректна модели для XOR.    
    20 эпох:    
    ![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/step4.png)  
  
## Задание 2
### Построить графики зависимости количества эпох от ошибки  обучения. Указать от чего зависит необходимое количество эпох обучения.
Требуемое количество периодов обучения зависит от веса и смещения. То есть вы должны выбрать такое количество тренировок, чтобы ошибки были максимально сведены к минимуму,
Затем персептрон завершает свое обучение. 
  
Ссылка на таблицу:  
https://docs.google.com/spreadsheets/d/1pGDUL2lGgpKdy2XsjhIDDtVGRwXRlacd7dkszPThEGo/edit?hl=ru#gid=0  
![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/tab-OR.png)   
Вывод:  
![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/tab-AND.png)   
Вывод:  
![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/tab-NAND.png)    
Вывод:  
![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/tab-XOR.png)        
Вывод:  

## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity.  
  При успешном обучении модели и при прохождение тестов сфера и пол становятся зеленым цветом, соответсвенно если обучение не успешно, сфера и пол становятся красным цветом.
  Как мы и говорил раньше модель успешно обучается для OR, AND, NAND, требуется лишь разное число эпох, но результат один для всех.  
  ![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/other.gif)      
  Так как модель не может обучиться на XOR, то мы видим на гиф один  из результатов тестов.   
  ![Image alt](https://github.com/tox3k/DA-in-GameDev-lab4/blob/main/scrinshots/XOR.gif)      
  Также в скрипт Perceptron.cs  я добавил такой код.  
  ```cs
  private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "Floor")
        {
            if (CalcOutput(0, 0) == 0)
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.green;
                gameObject.GetComponent<Renderer>().material.color = Color.green;
            }
            else
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.red;
                gameObject.GetComponent<Renderer>().material.color = Color.red;
            }
        }

        if (collision.gameObject.tag == "Floor1")
        {
            if (CalcOutput(0, 1) == 1)
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.green;
                gameObject.GetComponent<Renderer>().material.color = Color.green;
            }
            else
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.red;
                gameObject.GetComponent<Renderer>().material.color = Color.red;
            }
        }

        if (collision.gameObject.tag == "Floor2")
        {
            if (CalcOutput(1, 0) == 1)
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.green;
                gameObject.GetComponent<Renderer>().material.color = Color.green;
            }
            else
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.red;
                gameObject.GetComponent<Renderer>().material.color = Color.red;
            }
        }

        if (collision.gameObject.tag == "Floor3")
        {
            if (CalcOutput(1, 1) == 1)
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.green;
                gameObject.GetComponent<Renderer>().material.color = Color.green;
            }
            else
            {
                collision.gameObject.GetComponent<Renderer>().material.color = Color.red;
                gameObject.GetComponent<Renderer>().material.color = Color.red;
            }
        }
    }
  ```

## Выводы

- Реализовал и визуализировал персептрон в Unity
- Сделал выводы о корректности его работы на примере функций OR, AND, NAND, XOR

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
