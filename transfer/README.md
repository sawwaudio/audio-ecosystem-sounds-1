# 本体へ反映するためのパッチ（作業用）
このチャットのセッションは本体 sawwaudio/audio-ecosystem に直接書き込めないため、ここに置いて自動実行で本体に適用する。

適用の順番（本体の main が 306830d の場合）：
1. プロジェクト「saww audio ecosystem」の claude/patches/20261102-1800_v0_35-v0_37_mixer_fx_reel_motion.patch（v0.35・v0.36・v0.37）
2. v0.35b_spec10.patch（DJ_MIXER_SPEC の M2 を10種類に。docs のみ）
3. v0.38_library.patch（実録音86本の台帳・マニフェスト等。`git am -3` で適用。docs/AUTOMATION_LOG.md の衝突は両方の記録を残す）

v0.38 の index.html は、v0.35 の index.html（blob 2544796）を元にしている。適用後のテストでは、本体の直下に audio-ecosystem-sounds-1 という名前でこのリポジトリへのリンクを作ること（../audio-ecosystem-sounds-1 を参照するため）。
