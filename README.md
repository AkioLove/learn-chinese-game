# Learn Chinese Game

A simple browser game for kids to learn basic Chinese characters using a board-game style interface. The board loops endlessly like a game of Monopoly.

## How to Play

1. Open `index.html` in your browser.

2. Choose your character token (👦, 🦮, 🐔 or 🐵).
3. Click `擲骰子` to roll the dice and watch the token move.
4. When you land on a square, a flashcard appears with a Chinese character and three zhuyin options.
5. Choose the correct zhuyin to earn ⭐ points. The phonetic symbols are shown vertically in standard bopomofo style.
6. Squares you answer correctly are marked with a ✔.
7. The board's first and last cells are shown with 🚩 and 🏁 icons.
8. Completing a lap around the board awards an extra +10 ⭐.
9. A boss waits on the final square. Answer three questions in a row to defeat it! A wrong answer shows a losing icon and moves you back ten spaces.
10. Click the 🎵 icon to hear each reading, or listen automatically when a card opens.
11. On touch devices, swipe across the board to move your character.
12. Unselected characters appear on the map. Bump into them and they'll join your team, following behind like a snake!

## Tech

- Pure HTML, CSS and vanilla JavaScript
- Uses the [pinyin4js](https://github.com/commonsense/pinyin4js) library via CDN to convert any Chinese character to zhuyin
  Include it in `index.html` with:

  ```html
  <script src="https://cdn.jsdelivr.net/npm/pinyin4js/dist/pinyin4js.min.js"></script>
  ```

  Then call `PinyinHelper.convertToBopomofoString()` to obtain zhuyin, e.g.:

  ```javascript
  const bopomofo = PinyinHelper.convertToBopomofoString('你好', '', PinyinFormat.WITH_TONE_MARK);
  ```

Enjoy learning!
