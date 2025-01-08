# bit_map_message
В этой программе битовая карта (bitmap) — двумерное изображение, каждый пиксел которого может быть одного из двух цветов, представлена в виде многострочного строкового значения и служит для определения способа отображения пользовательского сообщения. В нашей битовой карте пробелы соответствуют пустому пространству, а все прочие символы заменяются символами из пользовательского сообщения. Представленная битовая карта напоминает карту мира, но вы можете заменить ее на любую другую, какую пожелаете. Простота системы двоичного представления «пустое пространство или символы сообщения» делает ее идеально подходящей для начинающих. Попробуйте поэкспериментировать с различными сообщениями и посмотрите, что получится.

# Результат работы должен выглядеть так:

....................................................................
    **********   *  *** **  *      ******************************
    ********************* ** ** *  * ****************************** *
         *****************       ******************************
          *************          **  * **** ** ************** *
           *********            *******   **************** * *
            ********           ***************************  *
            * **** ***         *************** ******  ** *
               ****  *         ***************   *** ***  *
                 ******         *************    **   **  *
                 ********        *************    *  ** ***
                   ********         ********          * *** ****
                   *********         ******  *        **** ** * **
                   *********         ****** * *           *** *   *
                     ******          ***** **             *****   *
                     *****            **** *            ********
                    *****             ****              *********
                    ****              **                 *******   *
                    ***                                       *    *
                    **     *                    *
....................................................................

# Описание работы
Вместо того чтобы по отдельности вводить все символы шаблона карты мира, вы можете скопировать его целиком из https://inventwithpython.com/bitmapworld.txt и вставить. Строки из 68 точек вверху и внизу шаблона служат «линейками» для упрощения правильного выравнивания. Однако программа будет работать и при наличии каких-либо опечаток в этом шаблоне.
Вызываемый в строке 43 метод bitmap.splitlines() возвращает список отдельных строк из многострочного строкового значения bitmap. Благодаря использованию многострочного строкового значения можно легко заменить нашу битовую карту любым другим шаблоном. Программа заполнит все непробельные символы в шаблоне, так что нет разницы, какие это символы: звездочки, точки или любые другие символы.
Код message[i % len(message)] повторяет текст в message. Когда i, увеличиваясь с 0, доходит до числа len(message), выражение i % len(message) снова становится
Описание работы 37
равно 0. В результате этого выражение message[i % len(message)] повторяет символы в message при росте i.

