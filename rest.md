## 2. REST

В рамках системы Host-to-Host предлагаются следующие ресурсы:

<table>
<thead>
<th>Документ</th><th>Описание метода</th> <th>Метод</th> <th>Ссылка</th> <th>Комментарий</th>
<tbody>
  <tr>
    <td rowspan=3>Валютный перевод <br />Платёжное поручение</td>
<td>Create Payments</td>
<td>POST</td>
<td>/API/v1/ISO20022/Payments</td>
<td>Создание пакета ВП/ПП</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/Payments/&lt;MsgId&gt;</td>
<td>Получение статуса по пакету ВП/ПП</td>
</tr><tr>
<td>Get Payment Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/Payments/Transactions/&lt;InstrId&gt;</td>
<td>Получение статуса по конкретному ВП/ПП</td>
</tr><tr>
<td>Отзыв платежа</td>
<td>Create Recall Payment</td>
<td>PUT</td>
<td>/API/v1/ISO20022/Payments/Recall</td>
<td>Отзыв платежа</td>
</tr><tr>
<td rowspan=2>Выписка</td>
<td>Post Request for Statement</td>
<td>POST</td>
<td>/API/v1/ISO20022/Statements</td>
<td>Запрос выписки</td>
</tr><tr>
<td>Get Statement by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/Statements/&lt;MsgID&gt;</td>
<td>Получение выписки</td>
</tr><tr>
<td rowspan=2>Онлайн остаток</td>
<td>Post Request for Account Balance</td>
<td>POST</td>
<td>/API/v1/ISO20022/Statements/AccountBalance</td>
<td>Запрос базового остатка</td>
</tr><tr>
<td>Post Request for Extended Account Balance</td>
<td>POST</td>
<td>/API/v1/ISO20022/Statements/AccountBalanceExtended</td>
<td>Получение расширенного остатка</td>
</tr><tr>
<td rowspan=3>СПД</td>
<td>Create ConfCertitficate</td>
<td>POST</td>
<td>/API/v1/ISO20022/ConfCertificates</td>
<td>Создание пакета СПД</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/ConfCertificates/&lt;MsgId&gt;</td>
<td>Получение статуса по пакету СПД</td>
</tr><tr>
<td>Get ConfCertitficate Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/ConfCertificates/Transactions/&lt;TxId&gt;</td>
<td>Получение статуса по конкретной СПД</td>
</tr><tr>
<td rowspan=3>Вложения к СПД</td>
<td>Load attaches to Certificate</td>
<td>POST</td>
<td>/API/v1/ISO20022/ConfCertificates/Transactions/Files/&lt;SpprtgDocId&gt;</td>
<td>Отправка вложенных файлов в СПД</td>
</tr><tr>
<td>Get attaches' list to Certificate</td>
<td>GET</td>
<td>/API/v1/ISO20022/ConfCertificates/Transactions/Files/&lt;SpprtgDocId&gt;</td>
<td>Получение списка файлов, приложенных к СПД (Выводится из эксплуатации, используйте: &lt;&lt;FILES_WITH&gt;&gt;)</td>
</tr><tr>
<td>Get attach to Certificate</td>
<td>GET</td>
<td>/API/v1/ISO20022/ConfCertificates/Transactions/Files/&lt;SpprtgDocId&gt;/&lt;FileId&gt;</td>
<td>Получение контента файла, приложенного к СПД</td>
</tr><tr>
<td rowspan=3>СВО</td>
<td>Create COCertificates</td>
<td>POST</td>
<td>/API/v1/ISO20022/COCertificates</td>
<td>Создание пакета СВО</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/COCertificates/&lt;MsgId&gt;</td>
<td>Получение статуса по пакету СВО</td>
</tr><tr>
<td>Get COCertificate Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/COCertificates/Transactions/&lt;TxId&gt;</td>
<td>Получение статуса по конкретным СВО</td>
</tr><tr>
<td rowspan=3>Вложения к СВО</td>
<td>Load attaches to Certificate</td>
<td>POST</td>
<td>/API/v1/ISO20022/COCertificates/Transactions/Files/&lt;TxId&gt;</td>
<td>Отправка вложенных файлов в СВО</td>
</tr><tr>
<td>Get attaches' list to Certificate</td>
<td>GET</td>
<td>/API/v1/ISO20022/COCertificates/Transactions/Files/&lt;TxId&gt;</td>
<td>Получение списка файлов, приложенных к СВО (Выводится из эксплуатации, используйте: &lt;&lt;FILES_WITH&gt;&gt;)</td>
</tr><tr>
<td>Get attach to Certificate</td>
<td>GET</td>
<td>/API/v1/ISO20022/COCertificates/Transactions/Files/&lt;TxId&gt;/&lt;FileId&gt;</td>
<td>Получение контента файла, приложенного к СВО</td>
</tr><tr>
<td rowspan=3>РСТС</td>
<td>Create FCYRLS</td>
<td>POST</td>
<td>/API/v1/ISO20022/FCYRLS</td>
<td>Создание РСТС</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/FCYRLS/&lt;MsgId&gt;</td>
<td>Получение статуса по сообщению, содержащему одно или несколько РСТС</td>
</tr><tr>
<td>Get RLS Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/FCYRLS/Order/&lt;PmtInfId&gt;</td>
<td>Получение статуса по конкретному РСТС</td>
</tr><tr>
<td rowspan=3>Письмо</td>
<td>Create official letter</td>
<td>POST</td>
<td>/API/v1/ISO20022/Letters</td>
<td>Создание письма</td>
</tr><tr>
<td>Get message status</td>
<td>GET</td>
<td>/API/v1/ISO20022/Letters/&lt;MsgId&gt;</td>
<td>Получение статуса по пакету писем</td>
</tr><tr>
<td>Get letter status</td>
<td>GET</td>
<td>/API/v1/ISO20022/Letters/OutLetters/&lt;ReqOrLttrId&gt;</td>
<td>Получение статуса по конкретному письму</td>
</tr><tr>
<td rowspan=2>Вложения к письму</td>
<td>Load attaches to letter</td>
<td>POST</td>
<td>/API/v1/ISO20022/Letters/OutLetters/Files/&lt;ReqOrLttrId&gt;</td>
<td>Отправка вложенных файлов</td>
</tr><tr>
<td>Get attach's content to incoming letter</td>
<td>GET</td>
<td>/API/v1/ISO20022/Letters/InLetters/Files/&lt;ReqOrLttrId&gt;/&lt;DocNb&gt;</td>
<td>Получение контента файла, приложенного к входящему письму (Выводится из эксплуатации, используйте: &lt;&lt;FILES_WITH&gt;&gt;)</td>
</tr><tr>
<td rowspan=2>Список входящих писем</td>
<td>Post request for list of letters</td>
<td>POST</td>
<td>/API/v1/ISO20022/Letters/Lists</td>
<td>Запрос на получение списка писем (входящих+ув-ия о ПВВ)</td>
</tr><tr>
<td>Get list of letters</td>
<td>GET</td>
<td>/API/v1/ISO20022/Letters/Lists/&lt;MsgId&gt;</td>
<td>Получение списка писем (входящих+ув-ия о ПВВ)</td>
</tr><tr>
<td  rowspan=4>Контракт (УНК)</td>
<td>Create Contract</td>
<td>POST</td>
<td>/API/v1/ISO20022/Contracts</td>
<td>Постановка на учет внешнеторгового контракта (УНК)</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/Contracts/&lt;MsgId&gt;</td>
<td>Получение статуса по пакету Контракта (УНК)</td>
</tr><tr>
<td>Get Contract Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/Contracts/Contract/&lt;CtrctRegnOpngId&gt;</td>
<td>Получение статуса по конкретному Контракту (УНК)</td>
</tr><tr>
<td>Get Сonfirmed Сontract by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/Contracts/Confirmations/&lt;CtrctRegnOpngId&gt;</td>
<td>Получение подтвержденного Контракта с номером УНК</td>
</tr><tr>
<td rowspan=3>Вложения к контракту</td>
<td>Load attaches to contract</td>
<td>POST</td>
<td>/API/v1/ISO20022/Contracts/Files/&lt;CtrctRegnOpngId&gt;</td>
<td>Отправка вложенных файлов</td>
</tr><tr>
<td>Get attaches' list to contract</td>
<td>GET</td>
<td>/API/v1/ISO20022/Contracts/Files/&lt;CtrctRegnOpngId&gt;</td>
<td>Получение списка файлов, приложенных к Контракту (Выводится из эксплуатации, используйте: &lt;&lt;FILES_WITH&gt;&gt;)</td>
</tr><tr>
<td>Get attach's content to contract</td>
<td>GET</td>
<td>/API/v1/ISO20022/Contracts/Files/&lt;CtrctRegnOpngId&gt;/&lt;FileId&gt;</td>
<td>Получение контента файла, приложенного к полученному контракту</td>
</tr><tr>
<td rowspan=3>Поручение на конверсионную операцию</td>
<td>Create FX</td>
<td>POST</td>
<td>/API/v1/ISO20022/ForeignExchanges</td>
<td>Создание поручения</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/ForeignExchanges/&lt;MsgId&gt;</td>
<td>Получение статуса по сообщению, содержащему одну или несколько конверсионных операций</td>
</tr><tr>
<td>Get FX Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/ForeignExchanges/Instructions/&lt;InstrId&gt;</td>
<td>Получение статуса по поручению</td>
</tr><tr>
<td rowspan=2> Зарплатная ведомость</td>
<td>Send payroll</td>
<td>POST</td>
<td>/API/v1/ISO20022/Payroll</td>
<td>Отправить ЗП ведомость</td>
</tr><tr>
<td>Get message status</td>
<td>GET</td>
<td>/API/v1/ISO20022/Payroll/&lt;MsgId&gt;</td>
<td>Получить статус сообщения с зарплатной ведомостью</td>
</tr><tr>
<td rowspan=2> Открытие ЛС</td>
<td>Send Employee account application</td>
<td>POST</td>
<td>/API/v1/ISO20022/EmployeeAccount</td>
<td>Отправить заявку на открытие ЛС</td>
</tr><tr>
<td>Get message status</td>
<td>GET</td>
<td>/API/v1/ISO20022/EmployeeAccount/&lt;MsgId&gt;</td>
<td>Получить статус сообщения с заявкой на открытие ЛС</td>
</tr><tr>
<td rowspan=3>Формирование архива со списком ВБК</td>
<td>Create an archive of bank control statements</td>
<td>POST</td>
<td>/API/v1/ISO20022/ContractReports</td>
<td>Создание архива с ВБК по контрактам</td>
</tr><tr>
<td>Get Message Status by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/ContractReports/&lt;MsgId&gt;</td>
<td>Получение статуса по сообщению, содержащему все переданные номера контрактов</td>
</tr><tr>
<td>Download file by Id</td>
<td>GET</td>
<td>/API/v1/ISO20022/ContractReports/Files/&lt;MsgId&gt;</td>
<td>Скачивание архива со списком ВБК</td>
</tr>