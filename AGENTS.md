# Bravo Fawzy — Game State

## Goal
Jeopardy-style Arabic trivia game with 14 categories, 10-question pools per category, timer (60s), 2-team scoring, and a "جدد الأسئلة" button to reshuffle mid-game.

## Categories (all with 10-question pools)
1. الدوري الإنجليزي ⚽
2. الدوري المصري ⚽
3. عملات 💰
4. ولايات أمريكية 🗺️
5. عواصم 🌍
6. تاريخ إسلامي ☪️
7. أفلام مصرية 🎬
8. علوم وطب 🔬
9. دول وأعلام 🚩
10. كوبليهات عمرو دياب 🎵
11. مسلسلات مصرية 📺
12. كأس الأمم الأفريقية 🏆
13. كأس العالم 🏆
14. كوبليهات تامر حسني 🎵

## Sound Effects (Web Audio API, no files)
- **Timer ≤ 10s**: 880Hz beep each second
- **✔ صح**: Ascending arpeggio (C5→E5→G5→C6), sine wave
- **❌ خطأ**: Descending sad buzz (E4→C4→G3→E3), sawtooth

## Progress
### Done
- ✅ All 14 categories populated: English League, Egyptian League, Currencies, US States, Capitals, Islamic History, Egyptian Movies, Science & Medicine, Flags/Countries, Amr Diab, Egyptian TV Series, Africa Cup of Nations, World Cup, Tamer Hosny.
- ✅ Sound effects (timer beep last 10s, correct/incorrect) via Web Audio API.
- ✅ User provides source material (Genius URLs, question lists); used directly.
- ✅ No auto-deploy — user explicitly approves each deploy.

### Pending
- User review and approval before Netlify deploy.

## Deploy (Netlify — primary)
```bash
cp Bravo_Fawzy_v2.html index.html && netlify deploy --prod --dir=.
```
Production URL: https://bravo-fawzy-game.netlify.app

## Deploy (GitHub Pages — backup)
Only deploy when user explicitly asks.
```bash
cp Bravo_Fawzy_v2.html index.html && git add index.html && git commit -m "update game" && git push
```
Public URL: https://capotin9-dev.github.io/bravo-fawzy/
