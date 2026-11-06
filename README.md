# saww audio ecosystem — 音源リポジトリ 1

**最新版のアプリ（v0.45・試用）：https://sawwaudio.github.io/audio-ecosystem-sounds-1/**
本体の公開サイト（https://sawwaudio.github.io/audio-ecosystem/）は、本体リポジトリに書き込めるようになるまで古い版（v0.34）のままです。それまでの間、このリポジトリの `index.html` に最新版を置いています（`build/deploy_sounds_site.py` で作成。本体にある41録音と楽器は本体の公開サイトから読み込みます。v0.45 で足した VCSL の楽器37ファイルは、このリポジトリの `instruments/` に置いています）。

[saww audio ecosystem](https://sawwaudio.github.io/audio-ecosystem-sounds-1/)（自然界の実録音で演奏する仮想楽器）が読み込む音源の置き場所です。本体（sawwaudio/audio-ecosystem）の容量を抑えるため、v0.37 から音源を別のリポジトリに分けています。本体からは同じ sawwaudio.github.io の `../audio-ecosystem-sounds-1/` として読み込みます。

- `audio/pcm/<id>.flac`：配信用の抜粋（FLAC・可逆圧縮）。16/24-bit の原本は原本のサンプルをそのまま切り出したもの（ビット完全）。32-bit・192kHz・多チャンネルの原本は変換して切り出し、内容を本体の台帳（data/recording_licenses.json の changes 欄）に記録しています。
- `audio/compat/<id>.mp3`：互換用（44.1kHz・モノラル・128kbps）。抜粋 FLAC から作成。
- `index.html`：最新版のアプリ（上記）。
- `transfer/`：本体へ反映するための作業用ファイル（反映後は不要）。

## 権利
各ファイルの権利は原典のライセンスに従います（CC0 1.0／CC BY 4.0／CC BY 3.0。BY-SA・NC は含みません）。CC BY の音源を使うときは、作者・題名・ライセンス・原典 URL を表示し、抜粋・変換したことを示してください。権利者による推奨を意味しません。

| id | 内容 | 作者 | ライセンス | 原典 |
|---|---|---|---|---|
| tawny-owl | モリフクロウ | Benboncan | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Owls.wav](https://freesound.org/people/Benboncan/sounds/63220/) |
| european-nightjar | ヨーロッパヨタカ | Benboncan | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Nightjar .wav](https://freesound.org/people/Benboncan/sounds/75073/) |
| eurasian-wren | ミソサザイ（さえずり） | Sacha.Julien | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Wren song close](https://freesound.org/people/Sacha.Julien/sounds/734533/) |
| eurasian-wren-ireland | ミソサザイ（さえずり・アイルランド） | iainmccurdy | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Wren Birdsong](https://freesound.org/people/iainmccurdy/sounds/643455/) |
| eurasian-wren-alarm | ミソサザイ（警戒声） | klankbeeld | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Eurasian Wren alarm call.wav](https://freesound.org/people/klankbeeld/sounds/260797/) |
| song-thrush | ウタツグミ | Artemis_R_Swann | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Song Thrush.wav](https://freesound.org/people/Artemis_R_Swann/sounds/517477/) |
| song-thrush-2 | ウタツグミ（サウサンプトン） | richwise | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Song Thrush](https://freesound.org/people/richwise/sounds/785669/) |
| nightingale | サヨナキドリ（ナイチンゲール） | iainmccurdy | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Nightingale](https://freesound.org/people/iainmccurdy/sounds/801117/) |
| nightingale-russia | ナイチンゲール（ロシア北西部・種名記載なし） | smand | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Nightingale Song](https://freesound.org/people/smand/sounds/521035/) |
| nightingale-vendee | ナイチンゲール（ヴァンデ・近接・種名記載なし） | bruno.auzet | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [nightingale close up](https://freesound.org/people/bruno.auzet/sounds/852685/) |
| uguisu-yokohama | ウグイス（横浜・街なか） | warukunai | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Japanese bush warbler (uguisu) in a city ambiance](https://freesound.org/people/warukunai/sounds/524526/) |
| loon-1 | アビの声（ウィスコンシン）1 | nicStage | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Loon / Diver call 1](https://freesound.org/people/nicStage/sounds/432605/) |
| loon-2 | アビの声（ウィスコンシン）2 | nicStage | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Loon / Diver call 2](https://freesound.org/people/nicStage/sounds/432604/) |
| loon-3 | アビの声（ウィスコンシン）3 | nicStage | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Loon / Diver call 3](https://freesound.org/people/nicStage/sounds/432603/) |
| lyrebird | コトドリ | samarobryn | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Superb Lyrebird II](https://freesound.org/people/samarobryn/sounds/399796/) |
| lyrebird-healesville | コトドリ（ヒールズビル・サンクチュアリ・物まね） | youthful_implants | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Lyrebird imitating sounds at Healesville Sanctuary.wav](https://freesound.org/people/youthful_implants/sounds/203498/) |
| woodpecker | キツツキ類（種名記載なし） | johnaudiotech | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Woodpecker](https://freesound.org/people/johnaudiotech/sounds/347047/) |
| woodpecker-leipzig | キツツキ類（ライプツィヒ・種名記載なし） | Garuda1982 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [woodpecker tap knock hammer in wood sound effect](https://freesound.org/people/Garuda1982/sounds/554594/) |
| woodpecker-illinois | キツツキ類のドラミング（イリノイ・種名記載なし） | kvgarlic | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Woodpecker drumming in morning March 6 2026](https://freesound.org/people/kvgarlic/sounds/847353/) |
| scops-owls-crete | コノハズク類（クレタ島・種名記載なし） | iainmccurdy | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Scops Owls (Crete)](https://freesound.org/people/iainmccurdy/sounds/744205/) |
| edge-forest-nl | オランダの森の縁の朝（アカゲラ・ウタツグミ等） | klankbeeld | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [edge forest 0738AM 210221_0257.wav](https://freesound.org/people/klankbeeld/sounds/619718/) |
| dawn-chorus-ashdown | 夜明けの合唱とカッコウ（英国・アッシュダウンの森） | Simon Spiers | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Dawn chorus Ashdown Forrest Distact Cuckoo.wav](https://freesound.org/people/Simon%20Spiers/sounds/344880/) |
| dawn-chorus-brittany | 夜明けの合唱（フランス・ブルターニュ） | kevp888 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [210528_1603_FR_DawnChorus.wav](https://freesound.org/people/kevp888/sounds/576578/) |
| dawn-chorus-provence | 夜明けの合唱とナイチンゲール（プロヴァンス） | iainmccurdy | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Provençal Dawn Chorus - Nightingale](https://freesound.org/people/iainmccurdy/sounds/843606/) |
| fujinomiya-forest-birds | 森の鳥のさえずり（静岡・富士宮） | florianreichelt | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [singing birds in the forest](https://freesound.org/people/florianreichelt/sounds/440604/) |
| fox | キツネ（夜の鳴き声） | Simon Spiers | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Fox Cry.wav](https://freesound.org/people/Simon%20Spiers/sounds/431302/) |
| wolf | オオカミ（群れの遠吠え・ヴェルコール） | Sacha.Julien | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Wolves howling (spontaneous and free )](https://freesound.org/people/Sacha.Julien/sounds/762242/) |
| roe-deer | ノロジカの鳴き交わし（ブルターニュ） | bruno.auzet | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [two roe-deers](https://freesound.org/people/bruno.auzet/sounds/850406/) |
| siamang | フクロテナガザル（香港動物園） | RTB45 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Siamang Gibbon Calls](https://freesound.org/people/RTB45/sounds/327443/) |
| siamang-belgium | フクロテナガザル（ベルギーの動物園） | ikbenraar | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [siamang monkeys](https://freesound.org/people/ikbenraar/sounds/819670/) |
| howler-belize | クロホエザルの夜の声（ベリーズ） | RTB45 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Howler Monkeys-Belize.wav](https://freesound.org/people/RTB45/sounds/148422/) |
| elephant-zoo | ゾウ（ベルギーの動物園・種名記載なし） | ikbenraar | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Elephant sound](https://freesound.org/people/ikbenraar/sounds/819668/) |
| sea-lion-valparaiso | アシカの叫び（チリ・バルパライソ・種名記載なし） | felix.blume | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Sea Lion screaming in Caleta Portales (Chile)](https://freesound.org/people/felix.blume/sounds/498626/) |
| sea-lion-valdivia | アシカのうなり声（チリ・バルディビア・種名記載なし） | Diim_1 | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Lobo Marino Grunendo - Growling Sea Lion](https://freesound.org/people/Diim_1/sounds/849186/) |
| bats-backyard | コウモリの狩りの声（種名記載なし） | digifishmusic | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Bats Hunting For Insects.wav](https://freesound.org/people/digifishmusic/sounds/43824/) |
| bat-batbox | コウモリのエコーロケーション（バットディテクター・フランス） | Sacha.Julien | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Bat echolocation call captured with a batbox](https://freesound.org/people/Sacha.Julien/sounds/724581/) |
| bat-slowed | コウモリのエコーロケーション（0.05倍速） | Garuda1982 | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [bat echolocation at 0.05 times speed](https://freesound.org/people/Garuda1982/sounds/755275/) |
| dolphin | イルカの声（カリブ海・水中・種名記載なし） | felix.blume | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Dolphin screaming underwater in Caribbean Sea (Mexico)](https://freesound.org/people/felix.blume/sounds/161691/) |
| atlantic-spotted-dolphin | タイセイヨウマダライルカ | geraldfiebig | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Atlantic Spotted Dolphins off the coast of La Gomera, Canary Islands](https://freesound.org/people/geraldfiebig/sounds/385796/) |
| amazon-river-dolphins | アマゾンのカワイルカ（テフェ川・種名記載なし） | felix.blume | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Amazonian Dolphins](https://freesound.org/people/felix.blume/sounds/408555/) |
| humpback | ザトウクジラの歌（モントレー湾・深海） | MBARI_MARS | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [MBARI_MARS_2017_1107h22_HS1P2.wav](https://freesound.org/people/MBARI_MARS/sounds/496870/) |
| treefrog-france | アマガエル類（フランス南西部・種名記載なし） | reinsamba | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [tree frog.wav](https://freesound.org/people/reinsamba/sounds/15689/) |
| common-toad | ヨーロッパヒキガエル | Breviceps | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Common toad (Bufo bufo)](https://freesound.org/people/Breviceps/sounds/462863/) |
| small-frog-ojai | カエルの声（カリフォルニア・オーハイ・種名記載なし） | clif_creates | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Small Frog Croaks](https://freesound.org/people/clif_creates/sounds/802737/) |
| pacific-treefrog-chorus | タイヘイヨウアマガエル類の合唱（カリフォルニア・ペトロリア） | CVLTIV8R | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Pacific Tree Frogs in Secluded Pond, Petrolia, CA](https://freesound.org/people/CVLTIV8R/sounds/852657/) |
| owl-fox-brittany | モリフクロウとキツネの夜（ブルターニュ） | bruno.auzet | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [owl and fox in large](https://freesound.org/people/bruno.auzet/sounds/850410/) |
| whales-orcas-norway | ザトウクジラとシャチ（ノルウェー・水中） | raiden04 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [humpback_whales_and_orcas_ambient_underwater_recording](https://freesound.org/people/raiden04/sounds/797762/) |
| snapping-shrimp | テッポウエビ類のはじける音（フロリダ・水中） | nathanwolek | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [ANMLAqua-snapping-shrimp-choppy-water-20240223](https://freesound.org/people/nathanwolek/sounds/737242/) |
| bullfrogs-hk | ウシガエル類の合唱（香港・駐車場・種名記載なし） | soloan | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Bullfrog Concerto.wav](https://freesound.org/people/soloan/sounds/188723/) |
| peepers-toads-ozarks | スプリングピーパーとアメリカヒキガエル（オザーク） | NickTayloe | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Spring Night Frogs (loop)](https://freesound.org/people/NickTayloe/sounds/813256/) |
| treefrogs-newyork | アマガエル類の合唱（ニューヨーク州・種名記載なし） | knufds | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Tree Frogs](https://freesound.org/people/knufds/sounds/242851/) |
| frog-pond-netherlands | 森の池のカエルの合唱（オランダ） | Sandermotions | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Nature sounds frog 3.WAV](https://freesound.org/people/Sandermotions/sounds/278871/) |
| lake-frogs-katydids | 夜の湖のカエルとキリギリス類（イリノイ） | Danjocross | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Lilipads and frogs at night.wav](https://freesound.org/people/Danjocross/sounds/503206/) |
| utah-canyon-frogs | 峡谷のカエル・ヒキガエルと夜の鳥（ユタ） | Danjocross | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Frogs Toads and Night Birds in Utah.wav](https://freesound.org/people/Danjocross/sounds/503211/) |
| brazil-frog-chorus | 夜のカエルの合唱とコオロギ（ブラジル・リオデジャネイロ州） | MeliaRoger | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [AMBRurl_BR Serrinha do alambari night frogs chorus with close crickets_Melia Roger_ORTF Schoeps.WAV](https://freesound.org/people/MeliaRoger/sounds/645706/) |
| amazon-night-jungle | アマゾンの夜の森（テフェ） | billcutbill（Bill’s Amazonas Sound Library (by Bill Cutbill)） | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [D332 Night Jungle Ambience 1.WAV](https://freesound.org/people/billcutbill/sounds/669408/) |
| podlaskie-spring-night | 春の夜のカエルの合唱（ポーランド・ポドラシェ） | TenderMicrophones.pl | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Spring Night peepers Crickets European Frogs Choir  Croaking Sounds Podlaskie  02-MAY-2024 32bit 192khz_PART_01](https://freesound.org/people/TenderMicrophones.pl/sounds/769592/) |
| frog-creek-ojai | 夜の小川のカエルとコオロギ（カリフォルニア・オーハイ） | clif_creates | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Frog Creek Ambience](https://freesound.org/people/clif_creates/sounds/802736/) |
| malaysian-frogs | カエルの群れ（マレーシア・メルシン） | ikbenraar | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Malaysian frogs](https://freesound.org/people/ikbenraar/sounds/819667/) |
| wetlands-night | 夜の湿地（カエル・ヒキガエル・鳥の声） | RealSquink | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Wetlands Night - Frogs, toads, bird whistles](https://freesound.org/people/RealSquink/sounds/826445/) |
| amphibians-campsite | 両生類の夜の合唱（フランス北部・アブヴィル近郊） | kevp888 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [260427_024431_FR_Amphibians_night_chorus_in_campsite](https://freesound.org/people/kevp888/sounds/856015/) |
| pond-hydrophone-essex | 小さな池の水中音（英国エセックス） | naturenotesuk | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Small Pond (Hydrophone)](https://freesound.org/people/naturenotesuk/sounds/729082/) |
| reedbed-pondlife | ヨシ原の池の生き物の水中音（英国ノーサンプトンシャー） | Mark_Taylor_Echophora_ | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Reedbed and Pondlife Sounds](https://freesound.org/people/Mark_Taylor_Echophora_/sounds/733081/) |
| garden-pond-hydrophone | 庭の池の水中音（英国デヴォン） | odilonmarcenaro | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [garden pond hydrophone](https://freesound.org/people/odilonmarcenaro/sounds/271673/) |
| titi-monkeys-tefe | サルの叫び（アマゾン・原典は “zogzog”・種名記載なし） | felix.blume | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Zogzog monkey yelling in the Amazonian Rainforest](https://freesound.org/people/felix.blume/sounds/508987/) |
| tokyo-cicadas-afternoon | 夏の午後のセミ（東京） | sound pro | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Tokyo_Cicada.wav](https://freesound.org/people/sound%20pro/sounds/483360/) |
| crickets-washington | 夜のコオロギ（ワシントン州ナチェス） | ES335-001 | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [crickets.wav](https://freesound.org/people/ES335-001/sounds/440574/) |
| night-woods-pennsylvania | 夜の森のコオロギとキリギリス類（ペンシルベニア） | widgetstudios | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Night Woods](https://freesound.org/people/widgetstudios/sounds/532301/) |
| night-insects-indiana | 9月の夜の虫（インディアナ） | NickTayloe | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Night Insects in September - Midwest US (loop)](https://freesound.org/people/NickTayloe/sounds/825635/) |
| rain-loon-ontario | 雨とアビの声（カナダ・オンタリオ） | jakobthiesen | [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) | [Medium Rain with Loon Call.WAV](https://freesound.org/people/jakobthiesen/sounds/101684/) |
| iceland-forest | アイスランドの森の開けた場所 | nickcath | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Atmos Country Open area in forest.aif](https://freesound.org/people/nickcath/sounds/176680/) |
| rock-tide-northumberland | 岩場に寄せる潮（英国ノーサンバーランド） | Tessa_Elieff | [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) | [Bathing House Rock Surface Close.wav](https://freesound.org/people/Tessa_Elieff/sounds/206044/) |
| forest-thunderstorm-hamburg | 森の雷雨（ドイツ・ハンブルク近郊） | pulswelle | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Rain And Thunder In The Forest.wav](https://freesound.org/people/pulswelle/sounds/280214/) |
| stormy-night | 嵐の夜 | VKProduktion | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Stormy Night](https://freesound.org/people/VKProduktion/sounds/344975/) |
| yukinoura-bamboo | 雪浦の竹林（長崎・西海市） | RutgerMuller | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Japan_Yukinoura_Bamboo_Forest_and_Road_.wav](https://freesound.org/people/RutgerMuller/sounds/368823/) |
| river-cicadas-provence | 川とセミ（フランス・ヴォクリューズ） | SamuelGremaud | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [RIVER AND CICADAS - 2](https://freesound.org/people/SamuelGremaud/sounds/437062/) |
| forest-drips-after-storm | 雷雨のあとの森の滴 | djtiii | [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) | [Water falling from forest trees after intense thunderstorm](https://freesound.org/people/djtiii/sounds/577568/) |
| waves-deadmans-cove | 入り江に砕ける波（ワシントン州ロングビーチ） | tim.kahn | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [WATRWave_medium waves breaking at deadman's cove_TK_SASSMKH8020.wav](https://freesound.org/people/tim.kahn/sounds/667786/) |
| winter-fens-kampina | 冬の湿原（オランダ・カンピナ国立公園） | klankbeeld | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [Winter fens NL 1129AM Kampina Kogelvangersven 230214_0559](https://freesound.org/people/klankbeeld/sounds/709372/) |
| yamanushi-river | 川（Yamanushi・日本） | kzarkses | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [WATRFall_Yamanushi Medium River Town_CP_NONE_ZOOM XY](https://freesound.org/people/kzarkses/sounds/746930/) |
| ice-lake-sweden | 氷の下を流れる水と森の風（スウェーデン） | vhio | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [AMBLake Water moving under ice, lake ambience in a windy forest, Stora Alljungen, Sweden](https://freesound.org/people/vhio/sounds/790541/) |
| waves-big-lagoon | 海岸に打ち寄せる波（カリフォルニア・ビッグラグーン） | CVLTIV8R | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Ocean Waves Crashing on the Coast of Big Lagoon, Redwoods](https://freesound.org/people/CVLTIV8R/sounds/803679/) |
| rain-rapids-nz | 雨と急流（ニュージーランド・シャープリン滝） | Desmond178 | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Rain and rapids](https://freesound.org/people/Desmond178/sounds/843888/) |
| birds-stream-paris | 朝の鳥と小川（パリ西郊・リュエイユ＝マルメゾン） | kevp888 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [260528_050202_FR_Birds_and_water_stream_in_the_morning](https://freesound.org/people/kevp888/sounds/857847/) |
| waterfall-hexenklamm | 滝と遠くの鳥（ドイツ・ヘクセンクラム） | Shuhmi | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | [WATRFall_Waterfall closeup birds distant_SHMI](https://freesound.org/people/Shuhmi/sounds/859225/) |
| rain-frogs-guiana | 夜の小雨とカエル（仏領ギアナ） | felix.blume | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | [Light Rain, Frogs and Toads at Night - Rémire-Montjoly, French Guiana](https://freesound.org/people/felix.blume/sounds/868995/) |
