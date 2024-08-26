Primer Contacte amb Spring i Maven

NIVELL 1

Aquest exercici és un primer contacte amb Spring Boot i Maven. El projecte genera una API REST simple amb dues rutes que responen a peticions GET.
Creació del Projecte

Per començar, accedeix a la pàgina Spring Initializr i genera un projecte Spring Boot amb les següents característiques:

    Tipus de Projecte: Maven
    Llenguatge: Java
    Versió de Spring Boot: La darrera versió estable

Metadades del Projecte

    Group: cat.itacademy.s04.t01.n01
    Artifact: S04T01N01
    Nom: S04T01N01
    Descripció: S04T01N01
    Package Name: cat.itacademy.s04.t01.n01
    Packaging: Jar
    Versió de Java: Mínim versió 11

Dependències Incloses

    Spring Boot DevTools
    Spring Web

Importació a l'IDE

Després de generar el projecte, importa'l a Eclipse amb l'opció: File > Import > Existing Maven Project.
Configuració

Edita l'arxiu application.properties i configura la variable server.port amb el valor 9000.
Creació del Controller

Dins del package principal, crea un subpackage anomenat controller. En aquest subpackage, afegeix una classe anomenada HelloWorldController amb dos mètodes:

    String saluda: Aquest mètode respondrà a una petició GET i haurà de ser configurat per a rebre el paràmetre nom com un RequestParam. Si no es proporciona cap nom, es retornarà "Hola, UNKNOWN. Estàs executant un projecte Maven". Respondrà a les següents URL:
        http://localhost:9000/HelloWorld
        http://localhost:9000/HelloWorld?nom=El meu nom

    String saluda2: Aquest mètode també respondrà a una petició GET, però el paràmetre nom serà una PathVariable opcional. Respondrà a les següents URL:
        http://localhost:9000/HelloWorld2
        http://localhost:9000/HelloWorld2/elmeunom


NIVELL 2

Aquest exercici és un primer contacte amb Spring Boot i Gradle com a gestor de dependències. El projecte genera una API REST simple amb dues rutes que responen a peticions GET.
Creació del Projecte

Per començar, accedeix a la pàgina Spring Initializr i genera un projecte Spring Boot amb les següents característiques:

    Tipus de Projecte: Gradle
    Llenguatge: Java
    Versió de Spring Boot: La darrera versió estable

Metadades del Projecte

    Group: cat.itacademy.s04.t01.n02
    Artifact: S04T01N02
    Nom: S04T01N02
    Descripció: S04T01N02
    Package Name: cat.itacademy.s04.t01.n02
    Packaging: Jar
    Versió de Java: Mínim versió 11

Dependències Incloses

    Spring Boot DevTools
    Spring Web

Importació a l'IDE

Després de generar el projecte, importa'l a Eclipse amb l'opció: File > Import > Existing Gradle Project.
Configuració

Edita l'arxiu application.properties i configura la variable server.port amb el valor 9001.
Creació del Controller

Dins del package principal, crea un subpackage anomenat controller. En aquest subpackage, afegeix una classe anomenada HelloWorldController amb dos mètodes:

    String saluda: Aquest mètode respondrà a una petició GET i haurà de ser configurat per a rebre el paràmetre nom com un RequestParam. Si no es proporciona cap nom, es retornarà "Hola, UNKNOWN. Estàs executant un projecte Gradle". Respondrà a les següents URL:
        http://localhost:9001/HelloWorld
        http://localhost:9001/HelloWorld?nom=El meu nom

    String saluda2: Aquest mètode també respondrà a una petició GET, però el paràmetre nom serà una PathVariable opcional. Respondrà a les següents URL:
        http://localhost:9001/HelloWorld2
        http://localhost:9001/HelloWorld2/el meu nom

NIVELL 3

Prova dels Projectes Maven i Gradle amb Postman

Aquest exercici consisteix a provar els projectes creats en els nivells anteriors mitjançant Postman. A continuació, es detallen els passos per configurar els entorns necessaris i provar els projectes.
Configuració d'Entorns a Postman
Entorns a Crear:

    Projecte Maven
    Projecte Gradle

Variables dels Entorns:

Ambdós entorns tindran dues variables:

    Servidor:
        Valor: http://localhost (per ambdós entorns)
    Port:
        Valor per al Projecte Maven: 9000
        Valor per al Projecte Gradle: 9001

Proves a Realitzar

Executa els projectes Maven i Gradle des d’Eclipse. Assegura’t que els dos projectes estan en execució abans de realitzar les proves amb Postman.
URLs per Provar:

Pots provar l’URL:

    http://localhost:xxxx/HelloWorld/elmeunom
    O qualsevol altra URL que els dos projectes admeten.

Substitueix xxxx pel valor de la variable Port en cada entorn respectiu.
Entrega:

Has de lliurar els següents arxius:

    Entorns Exportats (2 arxius JSON):
        Un per al Projecte Maven.
        Un per al Projecte Gradle.

    Captures de Pantalla (2 imatges):
        Una captura per a cada entorn, on es mostri l’execució de les peticions des de Postman utilitzant l’entorn i les variables definides.

Com Provar

    Executa els Projectes:
        Executa els projectes Maven i Gradle creats en els nivells anteriors des d’Eclipse.

    Prova les Peticions:
        Realitza les peticions a les URLs configurades utilitzant els entorns i variables creades en Postman.
        Verifica el retorn obtingut en cada projecte.

    Captura de Pantalla:
        Fes una captura de pantalla per a cada entorn que mostri l'execució correcte de les peticions.
