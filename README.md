# Примеры GSAP и React Guide
[![Dependency Status](https://img.shields.io/david/rhernandog/gsap-react-guide.svg)](https://david-dm.org/rhernandog/gsap-react-guide)
## Описание
Это набор примеров, используемых в официальном руководстве GSAP & React.

В этом репо сгруппированы все образцы из официального руководства [GreenSock](https://github.com/greensock) по анимации элементов DOM в приложении React с помощью [GSAP]() и (в некоторых случаях) [React Transition Group]()

#### Важная заметка
Код и комплектация в этом репозитории не предназначены для производственного кода, а предназначены только для целей разработки и обучения. Если вы хотите развернуть некоторую часть этого кода в производственном приложении, используйте аналогичный запуск, например Create React App или другой, а затем включите код в эту среду сборки.

## Установка
Просто клонируйте репо:
```
$ git clone https://github.com/rhernandog/gsap-react-guide.git
```
Или просто скачайте ZIP-файл и распакуйте его на свой локальный компьютер.

Затем установите зависимости:
```
$ npm install
```

## Живые семплы и редактирование
Для просмотра живых примеров вам нужно открыть файл `index.js` в папке `src/`. В нем импортируйте нужный образец из папки `src/components/` и запустите:
```
$ npm start
```
Чтобы обновить стили, измените файлы в папке `src/styles/`. Файл `base.css` также используется ... база для всех образцов. Тогда каждый образец может иметь определенную таблицу стилей, которая импортирована в конкретный файл `js` в папке `src/components/`.

```js
import ComponentName from "./components/path-to-component";

// в методе рендеринга
render(){
  return <div>
    <ComponentName />
  </div>;
}
```

#### О компоненте TransitionList.
Компонент списка переходов, очевидно, работает с динамическим списком элементов, который может быть увеличен или уменьшен при взаимодействии с пользователем. Этот список передается через свойства компонентов в файле `src/index.js` и должен быть импортирован в этот корневой файл из папки `helpers/`:

```js
import TransitionList from "./components/transition-list";
import { cards } from "./helpers/transition-group-cards";

// затем в методе рендеринга основного приложения
render(){
  return <div>
    <TransitionList cards={cards} />
  </div>;
}
```

## Журнал изменений

#### Version 1.2.2
- Синхронизированное содержание статьи между файлом article.md и статьей в блоге GreenSock.

#### Version 1.2.1
- Правильно отформатированные FAQ в markdown.

#### Version 1.2.0
- Исправлен маршрут в файле readme.
- Добавлены благодарности в статьи и файлы readme.
- Создан файл FAQ.
- Добавлен образец для управления состоянием с помощью GSAP.

#### Version 1.1.0
- Исправляет неявный возврат в обратных вызовах `ref`.
- Добавляет метод `constructor` к каждому образцу и передает `props` вызову `super`.
- Устраняет проблемы в JSX, перемещая атрибуты из длинных строк в независимую строку.
- Изменяет пример кода в примере [несколько элементов](https://github.com/rhernandog/gsap-react-guide/blob/master/src/components/simple%20tween/multiple-elements.js), чтобы удалить побочные эффекты от обратного вызова ref. Создает массив с элементами DOM, а затем использует этот массив в `componentDidMount` для создания временной шкалы.

#### Version 1.0.0
- Стабильная начальная фиксация.

## Отчёт об ошибке
Просто создайте [проблему](https://github.com/rhernandog/gsap-forums-react/issues).

## Содействие
Создайте PR и тщательно проверьте его перед отправкой. 

## Лицензия
Этот проект находится под лицензией MIT License - подробности см. В файле [LICENSE.md](https://github.com/rhernandog/gsap-react-guide/blob/master/LICENSE.md).

## Author
- Rodrigo Hernando
- Twitter [@websnapcl](https://twitter.com/websnapcl)
- Codepen [rhernando](https://codepen.io/rhernando/)

## Благодарности
Сначала я хотел бы поблагодарить Джека Дойла (создателя GreenSock) и [Карла Шоффа](https://twitter.com/snorklTV) (единственного и неповторимого посла GreenSock Geek) за то, что они доверили мне такую важную задачу.

Также хочу поблагодарить следующих разработчиков:

- Xiaoyan Wang (Horizon Blue). A very talented React developer, while Xiaoyan doesn't have a very active *social* life (twitter, facebook, etc), you can follow what He does in [GitHub](https://github.com/horizon-blue).
- Jason Quense. One of the maintainers of React Transition Group and part of React Bootstrap. Also collaborates in many other React-related projects. Check Jason's [GitHub profile](https://github.com/jquense) for more info.
- Last but not least, Matija Marohnić. The most active contributor and maintainer of React Transition Group and Part of the Yeoman Team. Matija also contributes in a lot of React-related projects as well as many other open source software. Be sure to follow Matija in [GitHub](https://github.com/silvenon) and [Twitter](https://twitter.com/silvenon).
