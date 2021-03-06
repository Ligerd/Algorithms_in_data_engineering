# Algorithms_in_data_engineering
Celem projektu jest zaimplementowanie i przeprowadzanie analizy porównawczej dwóch wersji algorytmu automatycznego różniczkowania. Proponowane aspekty podlegające porównaniu:

    tryb różniczkowania w przód / w tył (ang. forward mode automatic differentiation / ang. reverse mode automatic differentiation),
    różniczkowanie oparte o przeciążanie operatorów / o generowanie kodu.

Implementacja algorytmów musi być wykonana w sposób możliwie efektywny i kontrolowany. Oznacza to, że należy dołożyć starań, aby uruchamiany kod był możliwie zoptymalizowany. Przykładowo: dla implementacji w języku Julia należy zadbać m.in. o stabilność typów funkcji, wykorzystanie typów konkretnych w definicji struktur i funkcji. W języku Python niezbędne jest wykorzystanie modułu Numba i ogólna inspekcja kodu LLVM.

Porównaniu powinny podlegać: dokładność wyznaczonych pochodnych cząstkowych dla wyrażenia zróżniczkowanego samodzielnie, czas wyznaczenia macierzy Jacobiego dla testowanych wyrażeń oraz ilość alokowanej pamięci w trakcie działania algorytmu.

Algorytm powinien pozwalać na różniczkowanie takich funkcji jak: soft-max, ReLU, podstawowe funkcje matematyczne (m.in. f. wykładnicza, sin/cos, potęgowanie).
Opis pochodnych funkcji soft-max czy ReLU można znaleźć w [2].

Raport końcowy powinien składać się z czterech części:

    wstępu precyzującego jakie algorytmy i w jakim języku zostały zaimplementowane;
    opisu badania, przedstawiającego wybrane przypadki testowe, aspekty porównania oraz (najważniejsze) sposoby i warunki ich pomiaru; w warunkach pomiaru proszę uwzględnić parametry środowiska uruchomieniowego: rozmiar i prędkość pamięci, model procesora, model i typ dysku; niezbędne jest wyszczególnienie wszystkich zastosowanych optymalizacji algorytmów;
    sekcji z wynikami przedstawionymi w odpowiedniej formie wizualnej;
    podsumowania, odnoszącego się do wyników, obiektywnie zestawiających cechy charakterystyczne tych algorytmów; należy skonfrontować uzyskane wyniki ze spodziewanymi; warto odnieść się w dyskusji do aspektu związane z implementacją algorytmów (należy unikać zrzucania winy za różnice w wydajności algorytmów na środowisko Python).

W raporcie końcowym należy przetestować wybrane algorytmy zarówno pod kątem obliczania pochodnej cząstkowej względem wybranych argumentów (tzw. pochodna kierunkowa), jak i pod kątem wyznaczania macierzy Jacobiego (macierzy pierwszych pochodnych cząstkowych).

[1] Charles C. Margossian, 2018, A Review of automatic differentiation and its efficient implementation URL: arXiv

[2] Arun Mallya, 2019, A Quick Introduction to Backpropagation, http://arunmallya.github.io/writeups/nn/backprop.html
