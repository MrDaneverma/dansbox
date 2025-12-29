# Dansbox

В оригинале Beepbox, я сделол перевод для тех кто хочет вкатится, но не
знает английский.
DansBox это онлайн тулза для написания и распространения инструментальных мелодий.
тут скоро будет ссылка когда доделаю [ы](https://owlprog.ru)!

Вся музыка находится в ссылке на страницу, шо удобно. Когда
ты пишешь музыку, URL изменяется. Когда ты дописал музон, ты просто
можешь поделится ссылкой? Не верх ли удобства?

BeepBox был проектом бесплатным и всегда им будет. Задонать оригинальным
создателям бипбокса если хочешь!
[PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=QZJTX9GRYEV9N&currency_code=USD)

BeepBox был разработан [Джоном Нески](https://johnnesky.com/).
В (LICENSE.md) наврали, исходники я никому не отдам.

## Compiling

Код написян в TypeScript, я его не знаю а тока перевожу

```
git clone https://github.com/johnnesky/beepbox.git
cd beepbox
npm install
npm run build
```

## Code

The code is divided into several folders.

The [synth/](synth) folder has just the code you need to be able to play BeepBox
songs out loud, and you could use this code in your own projects, like a web
game. After compiling the synth code, open website/synth_example.html to see a
demo using it. To rebuild just the synth code, run:

```
npm run build-synth
```

The [editor/](editor) folder has additional code to display the online song
editor interface. After compiling the editor code, open website/index.html to
see the editor interface. To rebuild just the editor code, run:

```
npm run build-editor
```

The [player/](player) folder has a miniature song player interface for embedding
on other sites. To rebuild just the player code, run:

```
npm run build-player
```

The [website/](website) folder contains index.html files to view the interfaces.
The build process outputs JavaScript files into this folder.

## Dependencies

Most of the dependencies are listed in [package.json](package.json), although
I'd like to note that BeepBox also has an indirect, optional dependency on
[lamejs](https://www.npmjs.com/package/lamejs) via
[jsdelivr](https://www.jsdelivr.com/) for exporting .mp3 files. If the user
attempts to export an .mp3 file, BeepBox will direct the browser to download
that dependency on demand.
