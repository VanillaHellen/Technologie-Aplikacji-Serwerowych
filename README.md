# Technologie-Aplikacji-Serwerowych

## API

Główna strona: **http://bamfs.grzegorz-pietrzak.pl/index.php**

##### Podstrony i funkcje:
/user/{id}				                ---     wszystkie informacje usera o podanym id <br>
/user/{id}/koszyk    		        	---     produkty z tabeli koszyk przypisane do usera o podanym id, które mają status **koszyk**
/user/{id}/historia   			        ---     produkty z tabeli koszyk przypisane do usera o podanym id, które mają status **kupiony**

/produkty             			        ---     wyświetla wszystkie elementy tabeli produkty <br>
/produkty/{kategoria} 			        ---     wyświetla wszystkie elementy tabeli produkty WHERE 'kategoria' = {kategoria}
/produkty/{kategoria}/{podkategoria}  	---	wyświetla wszystkie elementy tabeli produkty WHERE 'kategoria' = {kategoria} AND 'podkategoria' = {podkategoria}

/szukaj/user/{klucz}			    	---	wyświetla usera posiadającego w loginie {klucz} <br>
/szukaj/produkty/{klucz}                --- wyświetla produkty posiadające w opisie (nazwie?) {klucz} - *może wyszukać klucz o nazwie równej którejś z kategorii* <br>
/szukaj/produkty/{kategoria}/{klucz}    --- wyświetla produkty w kategorii {kategoria} posiadające w opisie {klucz} - *może wyszukać klucz o nazwie równej którejś z podkategorii* <br>
/szukaj/produkty/{kategoria}/{podkategoria}/{klucz} --- wyświetla produkty w kategorii {kategoria} w podkategorii {podkategoria} posiadające w opisie {klucz}

/zaloguj/user/{login}/{haslo}           --- *jeżeli* jest w bazie użytkownik o zgadzającym się loginie i haśle, wyświetla wszystkie dane tego użytkownika - **! {login} może być zarówno loginem jak i e-mailem!** <br>
