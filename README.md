# pisnoplus-apk

Публічне дзеркало APK додатку **«Пісні+»** для сайту завантаження.

- У git самі файли `README.md` / `.gitignore` — **бінарники не комітимо**.
- APK кладеться лише як ассет релізу (`gh release create`), тому історія
  репозиторію не роздувається.

## Стабільне посилання («остання версія»)

```
https://github.com/zeroprotocolx86/pisnoplus-apk/releases/latest/download/PisniPlus-latest.apk
```

Браузер по цьому посиланню одразу починає завантаження — це і кнопка на
сайті `pisnoplus-site`.

## Публікація нової версії

Робиться автоматично скриптом із репозиторію додатку:

```
node scripts/sync-site.js <папка сайту>
```

або вручну:

```
gh release create vX.Y.Z path/to/PisniPlus-X.Y.Z.apk#PisniPlus-latest.apk `
  --repo zeroprotocolx86/pisnoplus-apk --title "Пісні+ X.Y.Z" --notes "..."
```

Імʼя ассету має бути саме `PisniPlus-latest.apk` — тоді URL вище завжди
веде на останній реліз.
