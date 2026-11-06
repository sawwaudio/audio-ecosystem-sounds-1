# 本体へ反映するためのパッチ（作業用）
このチャットのセッションと自動実行は本体 sawwaudio/audio-ecosystem に書き込めない（403）ため、ここに置いている。

## いちばん新しいもの（v0.49 まで）
本体の main（306830d）に、次の順で当てる。

```
git checkout -b latest 306830d
git am -3 --keep-cr v0.35-v0.43_series.patch      # v0.35〜v0.43（11コミット）
# v0.45 の楽器ファイル（バイナリ）は、このリポジトリの同じパスから複製してコミットする（パッチが大きくなりすぎるため）
cp -r <このリポジトリ>/instruments/pcm/vcsl_*.flac instruments/pcm/
cp <このリポジトリ>/instruments/compat/{didge,organPedal,timpaniRoll,gong,pianoLow,frameDrum,cajon,darbuka,slitDrum,conga}-*.mp3 instruments/compat/
git add instruments && git commit -m "v0.45：VCSL（CC0）の実録音楽器 37ファイル"
git am -3 --keep-cr v0.44-v0.45_series.patch      # v0.44（M5 第1段階・ログ）と v0.45（UI 再設計・楽器の層）の3コミット
git am -3 --keep-cr v0.46-v0.48_series.patch      # v0.46（Web MIDI・ログ）、v0.47（ポップ）、v0.48（自然な上質の見た目・生き物と環境音の分類）の4コミット
# v0.49 の旋律楽器（バイナリ）も同じく複製してコミットする
cp <このリポジトリ>/instruments/pcm/vcsl_{Mbira6,Marimba,TB_hit,glock}*.flac instruments/pcm/
cp <このリポジトリ>/instruments/compat/{kalimba,marimba,tubularBells,glockenspiel}-*.mp3 instruments/compat/
git add instruments && git commit -m "v0.49：VCSL（CC0）の旋律楽器の実録音 40ファイル"
git am -3 --keep-cr v0.49_series.patch            # v0.49（ロゴ・タブ・音量と休み・鳴っている音の一覧・イラスト・楽器と合成音の整理・密度・旋律4種）
```

- 入っている内容：v0.35〜v0.43 に加え、v0.46（Web MIDI）、v0.47（ポップな配色・書体・リール「ポップ」）、v0.48（リール「自然」・写真から色・明朝・生き物と環境音の分類）、v0.44（ミキサー等の設定をプリセットに保存）と v0.45（並び順・重複の解消・説明の畳み込み・再生バー、フルート・ハーモニクスの削除、実録音の低音6種・打撃5種）。
- 確認：data/audio_manifest.json の instruments の sha256 と、複製したファイルの SHA-256 が一致すること（v0.45 の37ファイル＋v0.49 の40ファイル）。
- 作業用ブランチ latest は本体リポジトリにも push 済み（2026-11-06 v0.49。main への書き込みは不可のまま）。
- テストでは、本体の直下に audio-ecosystem-sounds-1 という名前でこのリポジトリへのリンクを作る（../audio-ecosystem-sounds-1 を参照するため）。

## 古いもの（上に含まれる）
- v0.35b_spec10.patch、v0.38_library.patch
