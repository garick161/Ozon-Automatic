
![logo](https://github.com/garick161/Ozon-Automatic/assets/114688542/e969e901-c106-41c6-9698-f07972b28ec7)

# Предпосылки

2020 год изменил привычки и предпочтения многих людей. Каждый из нас столкнулся с ограничениями, с которыми пришлось мириться. Одним из таких ограничений - запрет на пользованием каршерингом. По специфике работы я часто им пользовался. Причины были понятны - есть риск передачи вируса при использовании различными людьми.
Тогда и возникла идея, как бы дезинфицировать автомобили после завершения аренды. Более того, я бы предпочёл, чтобы это происходило и не в условиях эпидемии.
Выполнить дезинфекцию вручную на таком количестве автомобилей - не реалистично. Нужно чтобы это было автономно и автоматически. И что тоже важно - безопасно! 
Выбор средств для дезинфекции в такой задаче невелик, если не сказать единственный.

# Дезинфекция озоном / Теория / Постановка задачи

Cуществуют множество статей и исследований об эффективности и безопасности озона. Это не является мировым открытием сейчас, давно применяется в разных сферах, в том числе и в медицине. Существуют готовые решения для помещений, но все они требуют присутствие персонала.
Устройства для автоматической дезинфекции автомобилей не существовало.\
При решении такой задачи как минимум возникают следующие сложности:
- Как установить устройство в автомобиль и не сломать его? Чтобы не было конфликтов с системами автомобиля
- Устройство должно энергосберегающее. Заряд аккумуляторной батареи автомобиле не безграничен
- Безопасность. Дезинфекция должна проводится строго в отсутствии людей
- Пожаробезопасность
- Универсальность. Автомобили все разные, а подключение должно быть единообразно

Озон можно получить из кислорода входе следующей химической реакции:
## <p style="text-align: center;"> 3 O<sub>2</sub> &harr;  2 O<sub>3</sub></p>

Реакция обратима и равновесие смещено влево(в сторону кислорода). При обычных условиях не идет, а только при выполнеии условий:
- Под действием электрического разряда. Это мы можем наблюдать во время грозы. Характерный запах после такого дождя этому свидетель\
или
- Под действием жесткого УФ-излучения (длина волны $\lambda$ = 185 Нм). Это явление тоже встречается в природе - образование озонового слоя в стратосфере. Удивительно, но именно озон потом и защищает Землю от дальнейшего проникновения УФ-излучения. В нашей задаче это скорее негативный побочный эффект.

1-й способ под действием электрического разряда более продуктивный, но очень энергозатратный. К тому же пластины сильно нагреваются при работе, поэтому возникает вопрос пожаробезопасности. Нам этот способ не подходит.

2-й способ возможен при использовании так называемых кварцевых ламп. Многие из нас видели такие лампы в палатах в медицинских учереждениях. Только там эффект основан на обеззараживании за счет УФ-излучения, озон лишь побочный продукт.

Использовать кварцевую лампу в салоне атомобиля мы не можем, так как после нескольких использований пластик и отделка салона прийдет в негодность. Значит остается вариант установить лампу в закрытый корпус и протягивать воздух через него. Тем самым мы получим сразу 2 эффекта:
- Проходящий воздух обеззараживается УФ-излучением
- Образуется озон, который потом оседает на поверхностях салона автомобиля, дезинфицируя их

# Концепция применения в каршеринге

Яндекс драйв: ссылка

Делимобиль: ссылка

# Первое устройство

Первое устройство было изготовлено в минималистичном варианте размером 200х100х50 мм и лампой мощностью всего лишь 4 Вт. Без всяких систем безопасности и наворотов. Естественно лампа с такой мощностью не могла в полной мере работать с объемом салона автомобиля. Проблема в том, что как мы говорили раньше, реакция получения озона обратимая и с течением времени возвращается к кислороду. Таким образом с лампой маленькой мощности мы так не сможем добиться нужной концентрации озона для дезинфекции, сколько бы она не работала. Да запах озона будет присутствовать, но клинического эффекта не будет.
Для эффективной борьбы с вирусами нужно около 0.4 - 0.5 мг/л.\
Статья о воздействии озона на микроорганизмы и необходимые концентрации.\
https://airlife.ru/articles/issledovaniya-po-unichtozheniyu-mikroorganizmov-ozonom

Итак, наша цель - 0.4 - 0.5 мг/л.\
В ходе долгих поисков подходящей лампы (нужно чтобы она была максимально мощная, в тоже время максимально компактная) была найдена мощностью 25 Вт и размером 25 см. Аналогичные лампы однотрубчатые такой же мощности будут около 70 - 80 см.\
Из расчета такая лампа производит 1г озона, что в пересчете на наш объем салона авто(2-3 $м^2$) где-то и получается 0.4 - 0.5 мг/л.\
Все зависит от длительности обработки. Так же на производительность сильно влияет температура окружающей среды: чем &darr; температура окружающей среды, тем &uarr; концентрация озона.\
Вооружившись знаниями приступил в сборке полнофункционального устройства.

# Краткий обзор компонентов
Ниже на схеме упрощенно приведены основные компоненты и их взаимодействие

![components3](https://github.com/garick161/Ozon-Automatic/assets/114688542/fc0d6d9d-cd2c-489b-880c-d5f0480908e5)

- В качестве основного контроллера был выбран Arduino Nano
- Запуск осуществляется с пульта ДУ и выбором различных программ
- Питание от бортовой сети автомобиля 12V
- Для питания датчиков и контроллера используется напряжение 5V от сцециальных преобразовалей
- Для запуска лампы используется инвертор 12/220V
- Для управлнения скоростью вентилятора используется ШИМ сигнал(Широко-импульсная модуляция)
- В состоянии покоя впусные/выпускные заслонки закрыты
- Для отрытия/закрытия заслонок используется сервоприводы с шаговыми двигателями
- При выполнении условий безопасности(мониторинг датчиков) система может быть запущена 
