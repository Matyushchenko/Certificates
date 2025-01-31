**Оформление заказа в Яндекс Такси**</br>
***Задача:***</br>
Пользователь мобильного приложения Яндекс Такси хочет заказать поездку и оплатить её через банковскую карту. При этом у пользователя есть возможность применить промокод для скидки на поездку. Промокод действует только на определённые типы поездок и ограничен по времени. Данные о промокодах хранятся в системе Яндекс Такси, включая информацию о самом промокоде, на какие поездки он распространяется, размер скидки, срок действия и статус (активен, использован, истёк). Процесс оплаты выполняется через платёжный шлюз, который списывает средства с карты клиента.</br>


***Последовательность шагов:***</br>
1.	Пользователь выбирает начальный и конечный пункты поездки.
2.	Приложение рассчитывает стоимость поездки и отображает её пользователю.
3.	Пользователь видит поле для ввода промокода и вводит промокод, если он доступен.
4.	Пользователь проверяет валидность промокода, нажав кнопку «Применить промокод».
5.	Если промокод действителен для выбранного маршрута и находится в состоянии «активен», стоимость пересчитывается с учётом скидки. В противном случае отображается ошибка с возможной причиной (промокод недействителен, истёк или не применяется к данному маршруту).
6.	Пользователь соглашается с пересчитанной или исходной стоимостью и нажимает кнопку «Заказать такси».
7.	В систему Яндекс Такси отправляется запрос с данными заказа и итоговой стоимостью. Если применён промокод, его статус меняется на «использован».
8.	Система отправляет запрос в платёжный шлюз с деталями заказа и суммой списания.
9.	Платёжный шлюз проводит проверку данных карты в системе «Антифрод».
10.	В случае успешной проверки шлюз списывает средства с карты, а статус оплаты передаётся в систему Яндекс Такси.
11.	Пользователь получает уведомление в приложении о статусе заказа и оплате (успешно или неуспешно).
12.	В случае успешной оплаты автомобиль приезжает в назначенное место для начала поездки.</br>


***Решение:***</br>
Постройте диаграмму последовательности с учётом всех вышеперечисленных конструкций. Отразите основные шаги оформления заказа, проверки промокода и оплаты, применяя UML-конструкции для альтернативных сценариев, асинхронных вызовов и группировки участников.

![UML Sequence диаграмма ](https://github.com/anastassaa/SA_portfolio/blob/master/UML%20Sequence%20Diagram.png)</br>
**UML Sequence** </br>

//www.plantuml.com/plantuml/png/hLRDJXDH6DtVfxXXBMpSkJ2uyWNa0IPOaoO818QeEw36DYaHuqPN2Bw0jxM52-MML_Zk6tc-SvrSPZgHnf-cqkbyvvplEz-P2-lxPR5N7hpUCiLckRDdvPlCPHPFv0e_n-BYiKprsXRxTiEONHHtDxkxnNPfL-I719dW_aqyil9Td7uGlwArBugttKOvg6U_2IybnA5SspW0zqUv8kHvKNRU5E-Qg4yIWF7nVJn4IvDLbOX7fBaLH-IpxRBxQgyuU6cCDMR3hZwb_XChdo4p4W-easayjXBGGLySHqmzYBTo0-Q0WdxrtLtiIS0unt682zoTmf09whnHvYnm3huZlFgaPrzpyUXipi--YLvRMxFoHPpwXgukyQMpZm6aZIewWIIgAfqDY9oHTSGfBb4Oe32rkAoqFGgS11HTBz63sTajRSqc5RZb_DaccO6shqh0qtiGqgc9ECFsREuFpH_2kd4YWEvfKfqfV8mNOQrCjNsbIXreePQR2ce1XwEGfWfLUarR87so05mnZQK1mdHZ0_GV7pakX4CsRR7LpZOILcoLO6YsbXdG1sA8VmrDgkdRBHyNLDZOIzMgr-eVjV8sc7cwQ54BgjZJj6j2z4sAFBrAKfNTrSAqR9pOmFqbNk3sJpxhWnm7Zl81CDAsxv8F1XO2QiTDGguwLDey_Of2BZu_4-YGs1v0RN6ZAfGyxj_LZpe9DP7gF4hv9fEJCG2dR5PxJFGOZAGo1-CigPEeOe0r-OXgYzzL7ZjHqUm1fy9SkdyEXgsIEBFPMf_dpNN7uSAw5phBy0kveoykcwa1cYHjNQ1s6G-LDz7mMJYhnaRZz5t3D91GPREcbqEI5rL7CHtPoc4coIVY_Lyb6Kt36kNt7y0vfxknkaTWKov6udMd6VRmkTl-L5NquluWqDdQxzGTq_3-bMj4_fDpP6XpZ-USDORTDiyweXuwxzfHAOm-FxEFB8ogJYj6tik8AVqlfrgDK8TQnt_uM-SN
