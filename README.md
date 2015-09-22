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

    ```
    HTTP GET    /user/ - pobieramy dane o sobie
    HTTP POST   /user/sign-in/ - logujemy się
    HTTP POST   /user/sign-up/ - rejestrujemy konto
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
