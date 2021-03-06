# Technologie-Aplikacji-Serwerowych

## API

Główna strona: **http://bamfs.grzegorz-pietrzak.pl/index.php**

##### GET

/user/{id}				                ---     wszystkie informacje usera o podanym id <br>
/user/{id}/koszyk    		        	---     produkty z tabeli koszyk przypisane do usera o podanym id, które mają status **koszyk** <br>
/user/{id}/historia   			        ---     produkty z tabeli koszyk przypisane do usera o podanym id, które mają status **kupiony** <br><br>

/produkty             			        ---     wyświetla wszystkie elementy tabeli produkty <br>
/produkty/{kategoria} 			        ---     wyświetla wszystkie elementy tabeli produkty WHERE 'kategoria' = {kategoria} <br>
/produkty/{kategoria}/{podkategoria}  	---	wyświetla wszystkie elementy tabeli produkty WHERE 'kategoria' = {kategoria} AND 'podkategoria' = {podkategoria} <br><br>

/szukaj/user/{klucz}			    	---	wyświetla usera posiadającego w loginie {klucz} <br>
/szukaj/produkty/{klucz}                --- wyświetla produkty posiadające w opisie (nazwie?) {klucz} - *może wyszukać klucz o nazwie równej którejś z kategorii* <br>
/szukaj/produkty/{kategoria}/{klucz}    --- wyświetla produkty w kategorii {kategoria} posiadające w opisie {klucz} - *może wyszukać klucz o nazwie równej którejś z podkategorii* <br>
/szukaj/produkty/{kategoria}/{podkategoria}/{klucz} --- wyświetla produkty w kategorii {kategoria} w podkategorii {podkategoria} posiadające w opisie {klucz} <br><br>

/zaloguj/user/{login}/{haslo}           --- *jeżeli* jest w bazie użytkownik o zgadzającym się loginie i haśle, wyświetla wszystkie dane tego użytkownika - **! {login} może być zarówno loginem jak i e-mailem!** <br><br>

#### POST 
**UWAGA!!! Żeby POST zadziałał, oprócz wejścia w link należy wysłać do strony odpowiednie Parametry!!**<br>
/user/{id}/koszyk/dodaj     -- **parametr: "idP" jest id Produktu** - dodaje podany produkt do koszyka usera o id = {id}<br>
/dodaj/user       -- **parametry: "login", "password", "firstname", "lastname", "email". UWAGA API sprawdza czy podany login/email są już zajęte, nie musicie tego robić** - dodaje użytkownika o podanych danych do bazy<br>

#### PUT
**UWAGA!!! Żeby PUT zadziałał, oprócz wejścia w link należy wysłać do strony odpowiednie Parametry!!**<br>
/user/{id}/koszyk/kup       -- **brak parametrów** - zmienia status wszystkich przedmiotów ze statusem 'koszyk' na 'kupiony' i ustawia 'data' na aktualną datę (UWAGA, data ustawia się od strony API, nie wysyłajcie dat od siebie)<br><br>
/update/user/{id}       -- **parametry: "login", "password", "firstname", "lastname", "email". UWAGA nie zostawiajcie pól pustych bo wtedy w bazie nadpisze dane pustym stringiem!!** - aktualizuje dane użytkownika<br><br>

#### DELETE
**UWAGA!!! Żeby DELETE zadziałał, oprócz wejścia w link należy wysłać do strony odpowiednie Parametry!!**<br>
/user/{id}/koszyk/usun    -- **parametr: "idP" jest id Produktu** - usuwa produkt o podanym id z koszyka (UWAGA, usuwa JEDEN produkt, nie wszystkie o podanym id które są w koszyku; UWAGA2 usuwa TYLKO produktu ze statusem 'koszyk')<br><br><br><br>




####  work in progress 
GET<br>
-<br><br>

POST<br>
-<br><br>

PUT<br>
-<br><br>

DELETE<br>
-<br><br>

**ADRES** - nowa tabela, foreign key userID, GET adress, POST adress, PUT adress
