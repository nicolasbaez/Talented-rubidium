# Talented-rubidium
5 years of love to #つぶやきProcessing

![buh](https://github.com/nicolasbaez/Talented-rubidium/blob/main/xp035.gif)
```javascript
// noprotect
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  rotateX(w);
  clear();
  for (k = 1; k < 7; k++)
    for (i = 0; i < 3; i += 0.05) {
      fill(0);
      beginShape();
      for (j = 0; j < 6; j += 0.05) {
        stroke(k * 42, w / k, w / 2);
        r = (w / 2) * sin(w + k) * noise(i, j, w / k);
        vertex(r * sin(i) * cos(j), r * sin(i) * sin(j), r * cos(i));
      }
      endShape();
    }
  w -= 0.01;
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp035.gif", 628, { delay: 0, units: "frames" });
  }
};
