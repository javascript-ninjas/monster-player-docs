# project-x

## Features

 - wpisywanie frazy

    ```
    HTTP GET    /search/:q(/:p)
    ```

 - [CLIENT] prezentacja wyników
 - kasowanie wyników

    ```
    HTTP GET    /media/:media_id
    HTTP DELETE /media/:media_id/delete - ignorowanie materiału przy wynikach wyszukiwania
    HTTP POST   /media/:media_id/favourite - dodanie materiału do listy ulubionych
    HTTP POST   /media/:media_id/playback - zwiększenie ilości odtworzeń
    ```

 - sing in, sign up, password change
 
   - HTTP GET    /user/ - pobieramy dane o sobie
     ```
     Request: 
     email: kebab2@cos.pl
     password: dhkjsadhkjahdkjsahkjdha
     User-Agent: Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/45.0.2454.99 Safari/537.36
     token: 811a8f175fd08d58c3d09e5305250bf6
     Accept: */*
     Accept-Encoding: gzip, deflate, sdch
     Accept-Language: en-US,en;q=0.8,pl;q=0.6
     ```
     ```
     Response
     {
        status: "success"
        user: {
            _id: "560695f3ffcf021c19b35a63"
            name: "kebabab"
            email: "kebab2@cos.pl"
            password: "dhkjsadhkjahdkjsahkjdha"
            avatar: "http://placehold.it/32x32"
        }
     }
     ```
     
   - HTTP POST   /user/sign-in/ - logujemy się  
     ```
     Request
     name=kebabab&password=dhkjsadhkjahdkjsahkjdha&email=kebab2@cos.pl
     ```
   
     ```
     Response
     {
        status: "success"
        login: true
        user: {
            _id: "560695f3ffcf021c19b35a63"
            name: "kebabab"
            email: "kebab2@cos.pl"
            password: "dhkjsadhkjahdkjsahkjdha"
            avatar: "http://placehold.it/32x32"
            token: "811a8f175fd08d58c3d09e5305250bf6"
        }
     }
     ```
    
   - HTTP POST   /user/sign-up/ - rejestrujemy konto
     
     ```
     Request
     name=kebabab&password=dhkjsadhkjahdkjsahkjdha&password2=dhkjsadhkjahdkjsahkjdha&email=kebab2@cos.pl
     ```
     
     ```
     Response
     {
        status: "success"
        login: true
     }
     ```

    ```
    HTTP POST   /user/password-change/ - zmieniamy hasło
    HTTP DELETE /user/ - usuwamy konto
    HTTP GET    /user/:id - pobieramy dane o kimś
    HTTP GET    /user/:id/friends - pobieramy listę przyjaciół danego użytkownika
    HTTP GET    /user/notification - pobieramy powiadomienia 
    HTTP PUT    /user/notification - dodajemy do powiadomień 
    HTTP POST   /user/invite/:friend_id - wysyłamy zaproszenie do grona przyjaciół 
    HTTP GET    /user/accept/:friend_id - akceptujemy zaproszenie przyjaciela
    ```

 - [CLIENT] odtwarzanie, pauzowanie, przewijanie
 - [CLIENT] equalizer (wspólny moduł)
 - playlisty

    ```
    HTTP GET    /playlist/ - pobieramy dane playlistach użytkownika
    HTTP DELETE /playlist/:playlist_id - usuwa playlistę
    HTTP POST   /playlist/:name - tworzy nową playlistę
    HTTP PUT    /playlist/:playlist_id/:media_id - dodaje element na playlistę
    HTTP GET    /playlist/:playlist_id - zwraca zawartość playlisty
    HTTP GET    /playlist/:id - pobieramy dane o konkretnej playliście
    HTTP DELETE /playlist/:id { media_id: 123 } - usuwa playlistę
    ```

 - share

    ```
    HTTP POST   /share/:media_id/:user_id/:friend_id - wysłanie piosenki przyjacielowi
    ```

 - chat
    - słuchający
    - friends
 - friends
 - [CLIENT] podgląd wideo
 - [CLIENT] wizualizacja
 - stats (ilość odtworzeń)
 - ulubione

## Platforms

 - Node.js
 - WWW
 - PC (Electron)
 - Mobile (Ionic)
 - Smart TV (Samsung)
 - Plugin (Chrome, Firefox)

## Providers

 - YouTube
 - Vimeo
 - SoundCloud
 - Dailymotion
 - Spotify
 - Wrzuta
