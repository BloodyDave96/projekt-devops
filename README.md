Dokumentacja Projektu DevOps
Krótkie wprowadzenie do projektu
Projekt DevOps polega na stworzeniu prostej aplikacji webowej w Pythonie przy użyciu frameworka Flask. Celem projektu jest wykorzystanie narzędzi DevOps do
konteneryzacji aplikacji oraz automatyzacji procesu CI/CD.
Instrukcja uruchamiania aplikacji lokalnie
1. Sklonuj repozytorium:    git clone <URL do repozytorium>    cd <nazwa-folderu>
2. Zainstaluj zależności:
   pip install -r requirements.txt
3.	Uruchom aplikację:
   python main.py
4.	Otwórz przeglądarkę i przejdź pod adres: http://127.0.0.1:5000.
Instrukcja uruchamiania aplikacji w kontenerze Docker
1.	Zbuduj obraz Docker:    docker build -t my-app .
2.	Uruchom kontener:
   docker run -p 5000:5000 my-app
3.	Otwórz przeglądarkę i przejdź pod adres: http://127.0.0.1:5000.
Opis procesu CI
Projekt wykorzystuje GitHub Actions do automatyzacji procesu CI. Główne elementy pipeline to:
1.	Trigger: Pipeline uruchamia się automatycznie przy każdym pushu i pull request na gałęzi main.
2.	Kroki procesu CI:
-	Pobieranie repozytorium.
-	Budowanie obrazu Docker.
-	Uruchamianie prostego testu (np. echo "Test succeeded!").
3.	Wynik: Przy każdej aktualizacji pipeline zapewnia poprawność działania aplikacji oraz budowy obrazu.
