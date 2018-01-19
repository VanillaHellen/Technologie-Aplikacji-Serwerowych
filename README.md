# Technologie-Aplikacji-Serwerowych

## API
Główna strona: **http://bamfs.grzegorz-pietrzak.pl/index.php**

##### Podstrony i funkcje:
/user/{id}				---     wszystkie informacje usera o podanym id <br>
/user/{id}/koszyk    			---     produkty z tabeli koszyk przypisane do usera o podanym id, które mają status **koszyk**
/user/{id}/historia   			---     produkty z tabeli koszyk przypisane do usera o podanym id, które mają status **kupiony**

/produkty             			---     wyświetla wszystkie elementy tabeli produkty <br>
/produkty/{kategoria} 			---     wyświetla wszystkie elementy tabeli produkty WHERE 'kategoria' = {kategoria}
/produkty/{kategoria}/{podkategoria}  	---	wyświetla wszystkie elementy tabeli produkty WHERE 'kategoria' = {kategoria} AND 'podkategoria' = {podkategoria}

*temporary*<br>
/szukaj/{klucz}				---	wyświetla produkty zawierające w opisie (nazwie??) {klucz}
