# Введение в программирование на Java

1. Нажимаем новый проект.
2. в появившемся окне выбираем Java, даем имя например java-project-1, выбераем Buld system " Maven " в закладке Advanced Settings в Grupid пишем например "ru.otus.java.basic". Проверяем Artefactid должно быть равное имени данное в начале. Нажимаем Create.
3. Заходим в папку src > main > нажимаешь правой кнопкой миши и создаем пакет с названием как в Groupid.
4. Нажимаем правой кнопкой мыши на пакет в папках и создаем new > Java class b даем ему название например App. **(всегда пишеться в UpperCameLCase)**
5. Заходим в папку .gitignor и удаляем все и оставляем только target/ и   .idea/
6. Нажимаем на папку самую верхнюю с названием проекта правой кнопкой мыши git > add.
7. Заходим в MainMenu во вкладку VSC и нажимаем Enable.
   


## Первая программа
- Точка входа можно вызывать коротко **"main" and "psvm"**.   
- Команда которая заставляет Java вывести что то в консоль,можно коротко вызывать "sout"
- Коментарии в коде однострочные : **//это коментарий**
- Коментарии многострочные обозначаются /* код или коментарий */
- **cntr /** делает многострочный коментарий при выделении
![](https://github.com/Extertom/Notebook_my/blob/a1396dd377b979a913de3c30b80667a2d97bf634/images/Hello_World.png)

## Небходимые интрументы 
![](https://github.com/Extertom/Notebook_my/blob/009aa27f7c91deffe8189b0cbfd90b5f1a060ed4/images/%D0%BD%D0%B5%D0%BE%D0%B1%D1%85%D0%BE%D0%B4%D0%B8%D0%BC%D1%8B%D0%B5%20%D0%B8%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B.png)

##Переменные и типы данных
![](https://github.com/Extertom/Notebook_my/blob/435b66d5dc06ecfeb06381e1cf22238c8eef1cd6/images/%D0%9F%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5%20%D0%B8%20%D1%82%D0%B8%D0%BF%D1%8B%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85.png)
![](https://github.com/Extertom/Notebook_my/blob/435b66d5dc06ecfeb06381e1cf22238c8eef1cd6/images/%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%20%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5.png)
![](https://github.com/Extertom/Notebook_my/blob/a51d0d639008ba2b4ebb7c173b2f3076d4ae275e/images/%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%20%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5%202.png)
- Переменные это int(Тип данных) a(Имя переменная) = 20(Значение которое дали переменной);
![](https://github.com/Extertom/Notebook_my/blob/f221d2aa338fcf06bbe4d37362a17b7a2a316d6c/images/%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5%20%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D1%80%203.png)




public class Main{
public static void main(String[] args){
system.out.println("Hello World");
}
}




