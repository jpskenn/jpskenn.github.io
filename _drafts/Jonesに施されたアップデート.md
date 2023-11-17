# Jonesに施されたアップデートをSandyへ適用する

## 対応方針

JonesがQMKへマージされて以降におこなわれたアップデート、つまりjpskenn以外のメンテナー等によりおこなわれたアップデートを、Sandyへ適用する。

Jonesのv1に対するアップデートを元とする。

Sandyは開発経緯により`dn0020`, `dn0030`, `v01`の3バージョンのファームウェアが存在するが、それらすべてに適用する。

## 注意点

自宅とリモート環境からの適用作業となるが、リモート環境にはビルド環境がないため、ビルド結果を見ずにコミットする。

それらコミットは、自宅においてビルド結果を確認する。

## アップデート一覧

- Move RGBLight animations to data driven (qmk#21635) 

    RGBアニメをinfo.json化。
    Sandy未使用。

- jones/v1: fix layout offset and disable audio on via keymap (qmk#21468)

    レイアウトオフセット修正  
    →Jonesのみ。対応不要

- Fix encoder map declarations (qmk#21435)

  エンコーダーマッピングの方向指定  
  →マジックナンバーから定数へ変更

    ```diff
    + const uint16_t PROGMEM encoder_map[][NUM_ENCODERS][2] = {
    - const uint16_t PROGMEM encoder_map[][NUM_ENCODERS][NUM_DIRECTIONS] = {
    ```

- Move miscellaneous defines to data driven (qmk#21382)

    コメント内の古い定義は、コメントごと消す。

    ```diff
    /* COL2ROW, ROW2COL*/
    // No need to define DIODE_DIRECTION for Jones' custom Round-Robin matrix.
    //#define DIODE_DIRECTION COL2ROW
    ```

    SandyはCOL2ROWを使っていてinfo.json化するので、これは対象外。

- Move RGBLIGHT_HUE/SAT/VAL_STEP to data driven (qmk#21292) 

    RGBLIGHT_HUEとかをinfo.jsonへ

- Remove encoder in-matrix workaround code (qmk#20389)

    エンコーダーの仮想マッピングを廃止  
    →config.hでの仮想定義をやめる  
    →keymap.cでキーコードの仮想割り当てやめる

- Move RGBLED_NUM to data driven (qmk#21278)

    →info.json化

- Move RGBLIGHT_SLEEP to data driven (qmk#21072)

    ```diff
    - // #define RGBLIGHT_SLEEP  /* If defined, the RGB lighting will be switched off when the host goes to sleep */
    ```

    Sandy未使用。

- Move RGBLIGHT_LED_MAP to data driven (qmk#21095)

    LEDマッピングしてるときのみ。
    Sandy未使用。

- Move RGBLIGHT_LIMIT_VAL to data driven (qmk#20974) 

    →info.json化

- Remove use of layout macros for music_map (qmk#20634)

    →music使用の場合のみ。対応不要

- Move single LAYOUTs to data driven (qmk#20365)

    →info.jsonでマトリックス指定
    →v1.cでv1.hをincludeせず、QMK_KEYBOARD_Hをインクルード

    ```diff
    - #include "v1.h"
    + #include QMK_KEYBOARD_H
    ```

    →v1.h削除（レイアウト部分）

- Migrate rgblight.pin and RGB_DI_PIN to ws2812.pin (qmk#20303)

    →Sandy対応済み

- [Core] Refactor keyevent_t for 1ms timing resolution (qmk#15847)

    →キーイベントのタイマー指定方法変更

    ```diff
        keyevent_t encoder_event = (keyevent_t) {
            .key = encoder_state[index] >> 1 ? encoder_cw[index] : encoder_ccw[index],
            .pressed = false,
    -       .time = (timer_read() | 1)
    +       .time = timer_read(),
    +       .type = KEY_EVENT
    ```

- Remove RGB_DI_PIN ifdefs (qmk#20218)

    →RGB_DI_PINについての#ifdefをやめる

    ```diff
    - #ifdef RGB_DI_PIN
    -
    - hogehoge
    -
    - #endif
    ```

- Remove more empty headers (qmk#20155)

    keyboard.hを#includeするだけのkeyboard.cを消す

- Fix layout macro keys with no matrix position (qmk#20033)

    マトリクス定義をミスってるところの修正？
    **よくわからん**

- Move matrix config to info.json, part 1 (qmk#19985)

    →マトリックスピン（MATRIX_ROW_PINSとか）をinfo.json化

- Move encoder config to data driven (qmk#19923) 

    →エンコーダー指定をinfo.json化

- Remove matrix size defines (qmk#19581)

    →マトリックスサイズ（MATRIX_ROWSとCOLS）をinfo.json化

- Move Bootmagic config to data driven (qmk#19860)

    →Bootmagic指定をinfo.json化  
    →Sandyは使ってないはず？

- Remove unused RGBLight defines from config.h (qmk#19859)

    未使用の定義（コメントアウトしてあるもの）があれば消す。

***これより下は、対応済み***

- Migrate MCU and BOOTLOADER to data-driven (qmk#19529)

    →MCUまわりをinfo.json化

    info.json

    ```diff
    +   "processor": "atmega32u4",
    +   "bootloader": "atmel-dfu",
    ```

    rules.mk

    ```diff
    -   # MCU name
    -   MCU = atmega32u4
    -
    -   # Bootloader selection
    -   BOOTLOADER = atmel-dfu
    ```

    →対応した

- Remove unused SOFT_SERIAL_PIN from config.h (qmk#19768)

    →Sandy未使用

- Remove unused Bootmagic row/col defines from config.h (qmk#19761)

    →Sandy未使用

- Remove unused GRAVE_ESC_CTRL_OVERRIDE from config.h (qmk#19752)

    →Sandy未使用

- Remove IS_HOST_LED_ON and migrate usages (qmk#19753)

    →ホストのLED状態読み取りを変更。  

    ```diff
    -    if (IS_HOST_LED_ON(USB_LED_CAPS_LOCK)) {
    +    if (host_keyboard_led_state().caps_lock) {
    ```

    →対応した

- Remove unused LOCKING_SUPPORT_ENABLE from config.h (qmk#19748)

    →Sandy未使用

- Debounce defines cleanup (qmk#19742) 

    →debounceの設定は消す

    ```diff
    - /* Debounce reduces chatter (unintended double-presses) - set 0 if debouncing is not needed */
    - #define DEBOUNCE 5
    ```

    →25keysさんのチャタリング防止ネタは、コメントアウトで書いてるだけなので、実害はない。
    →が、どうせ使ってないので消すことにする。

    →対応した

- Remove usages of config_common.h from config.h files. (qmk#19714)

    →#include "config_common.h"削除  
    →Sandyで変更済み

    **ここでプッシュされてないことがわかったので、一旦作業中断**

    ```text
    develop_Sandyへ、2件コミットしてしまっていた分は、家にてRevertをかけた。

    topic_sandy_qmk_v22_migrationブランチに切り替えて、最初（一番下）から作業やりなおし
    ```

- Update use of legacy keycodes (qmk#19120)

    古いキーコードを更新（音楽系）  
    →Sandy対応不要

- Remove legacy keycodes, part 5 (qmk#18710) 

    →`KC_SLCK` -> `KC_SCRL`

    →対応した

- Remove legacy international keycodes (qmk#18588)

    →`LANG1` -> `LNG1`, `LANG2` -> `LNG2`

    →対応した

- Move keyboard USB IDs and strings to data driven: J (qmk#17837)

    →USB関連をinfo.json化。  
    →Sandy対応済み。

- Rename keymap_extras headers for consistency (qmk#16939)

    →日本語キーマップのヘッダファイル名変更

    ```diff
    -   #include "keymap_jp.h"
    +   #include "keymap_japanese.h"
    ```

    →Sandyは変更済みの`keymap_japanese.h`を使用済み。

- Remove NO_ACTION_MACRO and NO_ACTION_FUNCTION from keyboard config.h 

    →定義削除

    ```diff
    -   #define NO_ACTION_MACRO
    -   #define NO_ACTION_FUNCTION
    ```

    →Sandyに該当箇所なし。

- [keyboard]Add v1 to jones keyboard (qmk#14405) 

    ここからはじまり

## アップデート以外の対応確認事項

- Bootmagic関連

    `rules.mk`に以下の記述があるが、残しておいてもよいのか？  
    削除必要？

    ```Makefile
    BOOTMAGIC_ENABLE = no       # Virtual DIP switch configuration
    ```
