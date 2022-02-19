### XML

1. Создать внешний репозиторий c названием XML:

    + войти <https://github.com/nazarrow?tab=repositories>

    + нажать `"New"`

    + ввести `"XML"` в поле `"Repository name"` --> выбрать `"Public"` и `"Add a README file"`

    + нажать `"Create repository"`

2. Клонировать репозиторий XML на локальный компьютер:

    + нажать `"Code"` --> выбрать `"HTTPS"` --> `скопировать ссылку на репозиторий`

    + в gitbash зайти в папку(в которой будет размещен репозиторий)

    + клонировать репозиторий на локальный компьютер --> `git clone` <https://github.com/nazarrow/XML.git>

    + войти в папку "XML" --> `cd XML` (в конце адреса расположения отображается "main")

3. Внутри локальной папки XML создать файл “new.xml”:

    + `touch new.xml`

    + `git status` - "new.xml" отображается красным (изменения в файле не отслеживаются)

4. Добавить файл под гит:

    + `git add new.xml`

    + `git status` - "new.xml" отображается зеленым (изменения в файле отслеживаются)

5. Закоммитить файл:

    + `git commit -m "add new.xml"` - создает снимок текущего состояния файла с комментарием add new.xml

6. Отправить файл на внешний GitHub репозиторий:

    + `git push`

7. Отредактировать содержимое файла “new.xml” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате XML:

    + `vim new.xml`

    + `"i"`

````xml
<?xml version="1.0" encoding="UTF-8"?>
<aboutMe>
 <fullName>Nazarov Aleksei Olegovich</fullName>
 <age>28</age>
 <pets>I don`t have any pets</pets>
 <desiredSalary>500$</desiredSalary>
</aboutMe>
````

+ `"Esc"`  

+ `":wq"`

8. Отправить изменения на внешний репозиторий:

    + `git add new.xml`

    + `git commit -m "modified new.xml"`

    + `git push`

9. Создать файл preferences.xml:

    + `cat > preferences.xml`

10. В файл preferences.xml добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате XML:

````xml
<?xml version="1.0" encoding="UTF-8"?>
<myPreferences>
 <movie>The Social Network</movie>
 <series>Silicon Valley</series>
 <food>Meat</food>
 <season>Summer</season>
 <country>Switzerland</country>
</myPreferences>
````

+ `"Enter"`

+ `"Ctrl + D"`

11. Создать файл skills.xml добавить информацию о скиллах которые будут изучены на курсе в формате XML:

    + `cat > skills.xml`

````xml
<?xml version="1.0" encoding="UTF-8"?>
<skills>
 <one>software testing theory</one>
 <two>client-server architecture</two>
 <three>HTTP Server Request Methods</three>
 <four>HTTP server Response codes</four>
 <five>Structures of HTTP requests and responses</five>
 <six>What is JSON, XML. Their structure</six>
 <seven>API testing via Postman JS, API autotests</seven>
 <eight>Removing and reading logs from an external server</eight>
 <nine>Sniffing http web traffic through Charles and Fiddler</nine>
 <ten>Dev Tools of web browsers Google Chrome, FireFox</ten>
 <eleven>VPN. How it works, why you need it, how to use it, tool options</eleven>
 <twelve>Mobile testing</twelve>
 <thirteen>Feature of iOS, Android, guidelines</thirteen>
 <fourteen>Build iOS applications on Xcode</fourteen>
 <fifteen>Build Android applications on Android Studio</fifteen>
 <sixteen>ADB management of android devices</sixteen>
 <seventeen>Setting up proxy and vpn on iOS and Android</seventeen>
 <eighteen>Interception (sniffing) of mobile traffic through Charles and Fiddler on iOS and Android</eighteen>
 <nineteen>Command line (terminal) Linux copy, create, view, move files on servers without a graphical interface</nineteen>
 <twenty>Basics of bash scripting, automation of routine tasks on the server</twenty>
 <twentyOne>Access to remote servers</twentyOne>
 <twentyTwo>Basics of SQL Create, Delete, Drop, Insert Into, Select, From, Where, Join</twentyTwo>
 <twentyThree>Postgres database installation, configuration and use</twentyThree>
 <twentyFour>Non-relational database Redis installation, configuration and use</twentyFour>
 <twentyFive>Load testing in Jmeter</twentyFive>
 <twentySix>Scrum development methodology</twentySix>
 <twentySeven>Python. Learning the basics. Building a client-server application</twentySeven>
</skills>
````

+ `"Enter"`

+ `"Ctrl + D"`

12. Отправить сразу 2 файла на внешний репозиторий:

    + `git add ._`

    + `git commit -m "add preferences.xml and skills.xml"`

    + `git push`

13. На веб интерфейсе создать файл bug_report.xml:

    + войти в `репозиторий "XML"`

    + нажать кнопку `"Add file"`

    + выбрать `"Create new file"`

    + в поле `"Name your file"` ввести `"bug_report.xml"`

14. Сделать "Commit changes" (сохранить) изменения на веб интерфейсе:

    + нажать кнопку `"Commit new file"`

15. На веб интерфейсе модифицировать файл bug_report.xml, добавить баг репорт в формате XML:

    + открыть файл `"bug_report.xml"`

    + выбрать редактирование и ввести текст

````xml
<?xml version="1.0" encoding="UTF-8"?>
<bugReport>
   <summary>Information dosn't provide if have more than 7 characters from WS</summary> 
   <descriprion>WS dosen't provide information if response containes more than 8 characters.</descriprion>
   <actualResult>information gets</actualResult>
   <expectedResult>information doesen't get</expectedResult>
   <requirementId>requirement</requirementId>
   <reproducedOn>Win 10</reproducedOn>
   <reproducibility>always</reproducibility>
   <workaround>no</workaround>
   <stepsTOreproduce>
        <one>1. Open FireFox browser</one>
        <two>2. Click [RESTClient] icon</two>
        <three>3. Request method: POST</three>
        <four>4. URL: http://178.124.206.52/app/ws/</four>
        <five>5. type in Body: {"user":"rangarad", "strict":false}</five>
   </stepsTOreproduce>
   <severity>minor</severity>
   <priority>low</priority>
</bugReport>
````

16. Сделать "Commit changes" (сохранить) изменения на веб интерфейсе:

    + нажать кнопку `"Commit changes"`

17. Синхронизировать внешний и локальный репозиторий XML:

    + `git pull`
