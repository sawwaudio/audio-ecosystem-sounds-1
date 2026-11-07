# 本体へ反映するためのパッチ（作業用）
このチャットのセッションと自動実行は本体 sawwaudio/audio-ecosystem に書き込めない（403）ため、ここに置いている。

## いちばん新しいもの（v0.61 まで）
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
git am -3 --keep-cr v0.50-v0.52_series.patch      # v0.50（MIDI 相対エンコーダー）、v0.51（合成音を鳴らさない）、v0.52（層の設定をプリセットに）と記録、6コミット
git am -3 --keep-cr v0.53.patch                    # v0.53（軽量の音源を既定に・端末への保存・画面の重複を減らす）。軽量の音源 audio/lite/（118本・71MB）はこのリポジトリにあり、本体には置かない
git am -3 --keep-cr v0.54.patch                    # v0.54（サンプラーのパッドごとの音量・ゼロ交差合わせ。自動実行）
# v0.55 の伝統楽器（バイナリ 64ファイル）は、このリポジトリの同じパスから複製してコミットする
cp <このリポジトリ>/instruments/pcm/vcsl_{MBira4,EthnicXylo,BowedPsaltery,HB_,Didgeridoo1_Phrase}*.flac <このリポジトリ>/instruments/pcm/vcsl_[A-G]*_mf_1.flac instruments/pcm/
cp <このリポジトリ>/instruments/compat/{mbira,balafon,danTranh,bowedPsaltery,handBells,didgePhrase}-*.mp3 instruments/compat/
git add instruments && git commit -m "v0.55：VCSL（CC0）の伝統楽器の実録音 64ファイル"
git am -3 --keep-cr v0.55.patch                    # v0.55（伝統楽器6種・無料版で出せる楽器を限る）
git am -3 --keep-cr v0.56.patch                    # v0.56（サンプラーの区間の拡大表示。自動実行）
git am -3 --keep-cr v0.57.patch                    # v0.57（課金：Stripe の月額・無料版と PRO の区別・server/）
git am -3 --keep-cr v0.58.patch                    # v0.58（初期設定：ディジュリドゥ・低音・鳥）
git am -3 --keep-cr v0.59.patch                    # v0.59（特商法の表記・定期購入の表示・イメージ写真）
git am -3 --keep-cr v0.60.patch                    # v0.60（自動実行：MIDI 出力・機器のランプ）
git am -3 --keep-cr v0.61.patch                    # v0.61（リールを作るを3番目に）
```

- 入っている内容：v0.35〜v0.43 に加え、v0.46（Web MIDI）、v0.47（ポップな配色・書体・リール「ポップ」）、v0.48（リール「自然」・写真から色・明朝・生き物と環境音の分類）、v0.44（ミキサー等の設定をプリセットに保存）と v0.45（並び順・重複の解消・説明の畳み込み・再生バー、フルート・ハーモニクスの削除、実録音の低音6種・打撃5種）。
- 確認：data/audio_manifest.json の instruments の sha256 と、複製したファイルの SHA-256 が一致すること（v0.45 の37ファイル＋v0.49 の40ファイル）。
- 作業用ブランチ latest は本体リポジトリにも push 済み（2026-11-07 v0.61。main への書き込みは不可のまま）。
- テストでは、本体の直下に audio-ecosystem-sounds-1 という名前でこのリポジトリへのリンクを作る（../audio-ecosystem-sounds-1 を参照するため）。

## 古いもの（上に含まれる）
- v0.35b_spec10.patch、v0.38_library.patch
