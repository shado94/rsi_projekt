# rsi_projekt
Projekt RSI - Wypożyczalnia


API:




	API CRUD:
	
	GET:
		/ksiazka
		/ksiazka/id_ksiazki
		/ksiazka/id_ksiazki/wypozyczenie
		/ksiazka/id_ksiazki/subskrybcje
		
		/sztuka_ksiazki
		/sztuka_ksiazki/s/id_sztuki_ksiazki
		/sztuka_ksiazki/k/id_ksiazki
		
		/uzytkownik
		/uzytkownik/id_uzytkownika
		/uzytkownik/id_uzytkownika/wypozyczenie
		/uzytkownik/id_uzytkownika/subskrybcje
		
		/wypozyczenie
		/wypozyczenie/id_wypozyczenia
		
		/subskrybcje
		/subskrybcje/id_subskrypcji
		
		/wydawca
		/wydawca/id_wydawcy
		/wydawca/id_wydawcy/ksiazka
		
		/autor
		/autor/id_autora
		/autor/id_autora/ksiazka
		
		/wyszukaj/wszystko/<HASŁO_DO_WYSZUKANIA>
		/wyszukaj/ksiazka/<HASŁO_DO_WYSZUKANIA>
		/wyszukaj/autor/<HASŁO_DO_WYSZUKANIA>
		/wyszukaj/wydawca/<HASŁO_DO_WYSZUKANIA>
		
	POST (dodawanie danych do bazy):
		/autor    ($imie, $nazwisko, $data_urodzenia, $stan)
		/ksiazka    ($tytul, $id_autora, $id_wydawcy, $data_wydania, $stan, $opis, $link)
		/uzytkownik   ($mail)
		/sztuka_ksiazki
		/wypozyczenie
		/subskrybcje
		/wydawca    ($wydawca, $stan)
		
	/* usunięte - dodawanie danych przez post 
	PUT:
		/autor/id_autora
		/ksiazka/id_ksiazki
		/sztuka_ksiazki/s/id_ksiazki
		/uzytkownik/id_uzytkownika
		/wydawca/id_wydawcy
		/wypozyczenie/id_wypozyczenia
		/subskrybcje/id_subskrypcji
	*/
	
	DELETE:
		/autor/id_autora
		/uzytkownik/id_uzytkownika
		/wydawca/id_wydawcy
		/sztuka_ksiazki/s/id_ksiazki
		/wypozyczenie/id_wypozyczenia
		/subskrybcje/id_subskrypcji
		/ksiazka/id_ksiazki
  __________________________________________________________

API integracja:

  GET
  POST
  PUT
  DELETE
____________________________________________________________

	
	API wypożyczalnia:


	GET:
	
	/wyszukaj/wszystko/<HASŁO_DO_WYSZUKANIA>
	/wyszukaj/ksiazka/<HASŁO_DO_WYSZUKANIA>
	/wyszukaj/autor/<HASŁO_DO_WYSZUKANIA>
	/wyszukaj/wydawca/<HASŁO_DO_WYSZUKANIA>
	/autor
	/autor/ksiazka
	/wydawca
	/wydawca/id_ksiazki
	/ksiazka/id_ksiazki
	/ksiazka
	/uzytkownik
	/uzytkownik/id_uzytkownika
	/uzytkownik/id_uzytkownika/subskrybcje
	/uzytkownik/id_uzytkownika/wypozyczenie
	/subskrybcje/id_subskrybcji
	/wypozyczenie/id_wypozyczenia
	/sztuka_ksiazki
	/sztuka_ksiazki/s/id_sztuki_ksiazki
	/sztuka_ksiazki/k/id_ksiazki
	/login
	/index
	
	
	
	
	POST:
	
	/ksiazka/id_ksiazki/wypozycz
	/sztuka_ksiazki/k/id_ksiazki
	/uzytkownik
	/ksiazka
	/wydawca
	/autor
	/subskrybcje
	
	PUT:
	
	/wypozyczenie/id_wypozyczenia/zwroc
	/sztuka_ksiazki/s/id_sztuki_ksiazki
	/uzytkownik/id_uzytkownika
	/uzytkownik/id_uzytkownika/ban
	/ksiazka/id_ksiazki
	/autor/id_autora
	/wydawca/id_wydawcy
	/subskrybcje/id_subskrybcji
	
	DELETE:
	
	/uzytkownik/id_uzytkownika
	/sztuka_ksiazki/s/id_sztuki_ksiazki
	/ksiazka/id_ksiazki
	/wydawca/id_wydawcy
	/autor/id_autora
	/subskrybcje/id_subskrybcji
_________________________________________________________________

Baza danych:

KSIĄŻKA
id_ksiazki
tytul
id_autora
ISBN
id_wydawcy
data_dodania
data_wydania
link_do_encyklopedii
stan

WYDAWCA
id_wydawcy
nazwa
stan

AUTOR
id_autora
imie
nazwisko
data_urodzenia
stan

SZTUKA KSĄŻKI
id_sztuki_ksiazki
id_ksiazki
stan

WYPOŻYCZENIE
id_wypozyczenia
id_sztuki_ksiazki
id_uzytkownika
data_wypozyczenia
data_przewidywanego_zwrotu
data_zwrotu
stan

USER
id_uzytkownika
mail
uprawnienia
stan

SUBSKRYPCJE
id_subskrypcji
id_uzytkownika
id_ksiazki
data_subskrypcji
stan
