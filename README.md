# repo-conflict-testing

lets play

repo do testów i zabawy z gałeziami, wspólnymi commitami itp. mOże też wspólne projekciki, idee i pomysły.
Kto chętny to zapraszam.

Słuchajcie, to repozytorium nie ma żadnych zabezpieczeń. Chcemy celowo wywołać konflikt, żeby zobaczyć, jak go naprawić.
Główna gałąź (main) jest NIE jest zablokowana i chroniona tak jak w repozytorium testing-fork .


Typowe działania

Do pracy w tym projekcie używamy uv – ultraszybkiego menedżera pakietów, który zastępuje tradycyjnego pipa i dba o to, żebyśmy wszyscy mieli dokładnie te same wersje bibliotek 

Krok 1

Jeśli jeszcze nie masz uv na swoim komputerze, otwórz terminal i zainstaluj go.

Krok 2

Otwórz terminal (lub terminal w VS Code), wejdź do folderu, w którym trzymasz projekty, i wpisz

git clone https://github.com/projekcik-testy/repo-conflict-testing.git
cd testing-fork


Krok 3
Mamy w projekcie plik pyproject.toml, który zawiera listę wszystkich naszych bibliotek. Aby je pobrać i stworzyć wirtualne środowisko wpisz w terminalu:

uv sync

Krok 4 Współpraca

Za każdym razem, gdy chcesz dodać nowy model, analizę lub plik, wykonuj te kroki:

1. Zaktualizuj swój kod (żeby mieć to, co zrobili inni):
   
git pull origin main

3. Stwórz nową gałąź:
git checkout -b nowa-galaz
4. Pisz kod, ucz się, baw
5. Zapisz i wyślij swoje zmiany
git add .
git commit -m "Dodano nowy notatnik - cokolwiek piszesz"
git push -u origin nazwa-twojej-galezi albo main

W tym repozytorium "akceptem" jest po prostu to, że Git technicznie pozwoli Ci wysłać kod. Jeśli dwie osoby wejdą sobie w drogę, Git ich zatrzyma błędem w terminalu

KOnfilkty procedura:

Zrobić git pull origin main – Git pobierze zmiany kogos i spróba je połączyć z Twoimi.
Zobaczyć "Conflict" w pliku – Jeśli edytowaliście tę samą linijkę, Git nie będzie wiedział, którą zostawić. W VS Code plik zrobi się kolorowy (fioletowo-niebieski) i pojawią się przyciski:
Accept Current Change (zostaw moje)
Accept Incoming Change (zostaw kogos)
Accept Both (zostaw oba)

Naprawić i dokończyć – Po wybraniu wersji trzeba plik zapisać, jeszcze raz zrobić git add ., git commit i dopiero wtedy git push.

W razie konfliktów lub problemów z gitem – piszcie śmiało na dyskusji - zakładka discussion
