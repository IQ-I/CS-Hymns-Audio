# Yorùbá tone-mark review sheet (draft v1)

The Yorùbá audio was generated from **tone-marked text**. The marks were added by a machine
(`Davlan/mT5_base_yoruba_adr`) and then corrected with hymn-vocabulary rules (Ọlọ́run, Olúwa, Jésù,
mímọ́, Hallelúyà, ọba, ògo …). A guard keeps every word's letters exactly as in the hymnbook,
so only the tone marks and under-dots can differ. **A Yorùbá speaker must still review it.**
The app shows the original lyrics; nothing on screen changes until the review is done.

- `yoruba_tone_review.csv`: every line, original vs marked (23,730 lines; open in Excel / Google Sheets).
  Fill in "correct? (Y/N)" and, if N, the corrected line.
- `top_words.csv`: the 600 most frequent marked words. **Start here.** Fixing one common word fixes
  hundreds of lines at once.
- `marked_text_v1.json`: the marked text, kept separate from the app's lyrics.

Stats: 909 hymns · 23,730 lines · 2267 lines where the machine tried to change a word
(the original word was kept) · 0 lines not yet marked.

After review, the corrected lines are fed back in and only the changed hymns are re-generated (minutes per hymn).
