# 本体へ反映するためのパッチ（作業用）
このチャットのセッションと自動実行は本体 sawwaudio/audio-ecosystem に書き込めない（403）ため、ここに置いている。

## いちばん新しいもの（これだけ使えばよい）
**v0.35-v0.43_series.patch**：本体の main（306830d）に、v0.35〜v0.43 の11コミットをまとめて当てる。

```
git checkout -b latest 306830d
git am -3 --keep-cr v0.35-v0.43_series.patch
```

中身：v0.35〜v0.37（ミキサー・BEAT FX・リールの動き）、M2 を10種類に（設計書）、v0.38（実録音86本）、v0.39〜v0.42（トランスゲート・ビットクラッシュ・効果ごとのつまみ・チャンネル FX・サンプラー）、v0.43（写真で選ぶ音・マスター EQ・リール作成・マルチトラック・FREE/PRO・名称変更）。

テストでは、本体の直下に audio-ecosystem-sounds-1 という名前でこのリポジトリへのリンクを作る（../audio-ecosystem-sounds-1 を参照するため）。

## 古いもの（上のまとめに含まれる）
- v0.35b_spec10.patch、v0.38_library.patch
