# future-collars-java-intro-faq


### Jak oddać zadania z preworku?

Początkowe zadania (zanim dojdziemy do pierwszego zadania z GITem) w których wymagane jest napisanie kodu powinny zostać wykonane albo zostać oddane albo w formie linku do programu na platformie https://ideone.com/  


### Jak oddać zadania w stylu "Zainstaluj GIT"?

Zadania tego typu wystarczy skomentować "zrobione" i wysłać do sprawdzenia.


### Jak uniknąć konfliktów na githubie?

Tak w pełni to się nie da. :) Jednak możemy choć trochę zmniejszyć prawdopodobieństwo ich występowania.
Pamiętaj, aby przed rozpoczęciem każdego zadania: 
  1. Wrócić na główny branch (`git checkout nazwa_brancha`)
  2. Zaciągnąć najnowsze zmiany (`git pull`)
  3. Stworzyć nowy branch (`git checkout -b nazwa_brancha_dla_nowego_zadania`)


### Jak oddać zadania wysłane na GITa?

- Zadania powinny zostać oddane w formie pull requestu (PR). Jeden pull request = jedno zadanie. Link do utworzonego PR wyślij jako komentarz do zadania na platformie.
- W PR powinny być tylko te pliki, które są wymagane dla danego zadania. 


### Kiedy mogę zmergować zadanie?

Nie merguj PR póki nie dostaniesz approve. Zadania zaakceptowane powinny zostać zmergowane tak szybko jak to możliwe.



### Czy dla każdego zadania powinienem tworzyć nowe repozytorium?

Wszystkie zadania trzymamy w 1 repozytorium - aby zachować porządek zastanów się nad odpowiednią strukturą (np. 1 folder = 1 zadanie, albo 1 folder = 1 lekcja, a w środku kolejne n folderów dla konkretnych zadań w ramach danej lekcji).


## Najczęstsze błędy

### Komentarze
Staraj się unikać komentarzy w kodzie jeżeli jest to możliwe. Nie ma sensu robić komentarzy w stylu:
```
// Method returns list with users
List<String> getUsers(){
...
}
```
bo jest to oczywiste i wynika z nazwy i sygnatury metody.

Troche więcej o tym czemu komentarze to zło: https://www.freecodecamp.org/news/code-comments-the-good-the-bad-and-the-ugly-be9cc65fbf83/
Oczywiście czasami komentarz warto dać, ale zastanów się nad tym tysiąc razy czy na pewno jest on konieczny.

### Stałe 
Jeżeli używasz jakichś stałych w kodzie - zapisz je jako (private) static final type NAME_OF_VARIABLE.

Przykład:
```
int calculateSalary() {
  return dailySalary * 20 <--- czym jest to 20?
}
```

Przykład ze stałą:
```
int calculateSalary() {
  return dailySalary * NUMBER_OF_DAYS_IN_MONTH;
}
```


### Checked vs unchecked exceptions
Staraj się unikać checked exception. Czemu? https://phauer.com/2015/checked-exceptions-are-evil/


### Ścieżki absolutne vs relatywne

Nie używaj ścieżek absolutnych w kodzie np: `C:/Users/pater/projects/file.txt`. Nikt inny nie będzie w stanie uruchomić tego programu, ponieważ mała szansa, że będzie miał taką ścieżkę u siebie. ;) Zamiast tego używaj ścieżek relatywnych. https://www.computerhope.com/issues/ch001708.htm


### Struktura testu

Staraj się stosować strukturę testu given when then gdzie:
- given - dane wejściowe
- when - wywołanie funkcjonalności, którą testujemy
- then - asercje czyli sprawdzenie poprawności

Przykład:
```
// given
int minutes = 5;

// when
int result = TimeConverter.minutesToSeconds(minutes);

// then
Assertions.assertEquals(result, 300);
```

Więcej o tym: https://blog.j-labs.pl/index.php?page=2017/02/Given-When-Then-pattern-in-unit-tests

## Ciekawe linki

Zapisz sobie link do skrótu konwencji jakie mamy w javie: https://github.com/rahulgoti1/java-naming-conventions#naming-conventions

