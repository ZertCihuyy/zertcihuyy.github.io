#ZertCihuy

```js
const messages = [
  "Konnichiwa.",
  "Watashi no namae wa ZERT desu.",
  "Indonesia shusshin desu.",
  "Backend developer toshite katsudou shiteimasu.",
  "",
  "Website: https://zertcraft.xyz",
  "GitHub: https://github.com/zertcihuyy"
];

let line = 0;
let char = 0;

function typeLine() {
  if (line >= messages.length) {
    return;
  }

  if (char < messages[line].length) {
    process.stdout.write(messages[line][char]);
    char++;
    setTimeout(typeLine, 40); // kecepatan ngetik
  } else {
    process.stdout.write("\n");
    char = 0;
    line++;
    setTimeout(typeLine, 400); // jeda antar baris
  }
}

typeLine();
```
