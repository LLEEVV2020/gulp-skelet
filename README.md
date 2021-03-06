# gulp-skelet
Паттерн системы сборки (gulp 4 + pug + sass)

Установка и запуск нового проекта

1.	Для запуска нового проекта необходимо скачать паттерн системы сборки.
2.	В папке со скачанным паттерном следует запустить команду npm install.
3.	После установки всех пакетов будут доступны две команды:
a)	gulp build для сборки production версии проекта;
b)	gulp dev для сборки development версии и ее запуска на локальном сервере.
4.	Если все будет выполнено правильно, то:
a)	на экране откроется страница со подобным сообщением:
	https://viacheslavdemchenko.github.io/gulp-4-start-page/
b)	в консоле выведется Hellow!

Структура production версии после сборки

На выходе при сборке проекта создается папка build. В ней располагается главная страница index.html с подключенным к ней файлом шрифтов fonts.css и минимизированными файлами main.min.css и main.min.js, а также все прочие html-страницы проекта.
Ниже представлена примерная структура production версии проекта после сборки:

build
	 ---css
		main.min.css
	 --fonts
		fonts.css
	 --img
		image-1
		image-2
		...
		sprite.svg
	 --js
		main.min.js
	index.html
	page.html
	404.html
	
Используемые пдагины:

gulp – галп;
gulp-pug – плагин для компиляции pug файлов в HTML файлы;
del – плагин для удаления папок и файлов;
gulp-plumber – плагин для предотвращения разрывов цепочки пайпов (pipe) при выполнении тасков (task) в файле gulpfile.js, вызванных ошибками плагинов; 
gulp-rename – плагин для переименования файлов;
gulp-concat – плагин для объединения файлов;
gulp-htmlhint – пдагин для валидации HTML файлов; 
gulp-htmlmin – пдагин для минимизации HTML файлов;
gulp-sass – плагин компиляции sass файлов в css файлы;
gulp-autoprefixer – плагин добавления вендорных префиксов;
gulp-group-css-media-queries – плагин группировки медиа-запросов; 
gulp-csso – плагин для минимизации css файлов с сокращенной формой записи кода;
gulp-uglify – плагин минимизации js файлов;
gulp-babel – плагин компиляции js файлов в стандарт ES5; 
gulp-tinypng-nokey – плагин минимизации картинок через сервис Tinypng без необходимости использования персонального API-ключа;
gulp-svg-sprite – плагин создания файла спрайтов для svg;
gulp-svgmin – плагин минимизации svg;
gulp-cheerio – плагин удаления атрибутов внутри svg;
gulp-replace – замена необходимых частей кода в svg для исправления некоторых багов; 
browser-sync – плагин для обновления браузера при каждом внесении изменения в код проекта.