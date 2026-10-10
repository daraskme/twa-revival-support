# Service and update status / 運用・更新状況 / Состояние сервиса

Updated: **2026-10-10 18:56 JST**. [Project](https://darask.me/twa/) · [Support](README.md) · [Launcher source](https://github.com/daraskme/twa-revival-launcher) · [Server source](https://github.com/daraskme/twa-revival-server)

## 日本語

**メンテナンス継続中です。新規ログイン・マッチングの再開日は未定で、本番配信はまだ変更していません。** 現在の検証版はQA0.2.91です。クラウドのQA配布マニフェスト0.2.63とは別に、両VMへ署名済み候補を適用しています。最後に正常取得できた公開安定版は0.2.43で、その後の公開状態照会はHTTP 403のため再確認が必要です。

今回復旧した5マップ定義は、長坂の拠点戦、ミュカレとヴェスヴィウスの両ルールです。いずれも通常の2人対戦、両者の最終戦績、全6部隊の使用構成、本人用と公開APIの一致、同室への復帰までQAで確認済みです。候補には16地形×2ルールを収録しています。

「Private拠点戦」「Private殲滅戦」を別の入口として実装しました。英語・日本語・ロシア語の実画面を確認し、日本語・ロシア語では両ルールの部屋作成、通常退出、再起動なしのルール切り替えに成功しました。マップ変更や招待によって拠点戦が殲滅戦へ戻る問題も修正しました。期限切れ部屋の退出前に準備解除が失敗する経路は修正・関連90件を両OSで確認済みで、待機中に実際に期限切れとなった部屋から通常退出し、再起動せず新しい部屋を作れることも確認しました。対戦中の期限切れなど他条件は残ります。

QA0.2.90では自主退出理由の保存と、通常の勝敗を退出と誤認しない処理を追加しました。Private殲滅戦1試合で、自主退出記録・使用構成の保存、本人用／公開戦績の一致、相手の通常勝利、両者の同室復帰を確認しました。退出理由と構成は相手決着後も不変で、結果受け取りは本人の復帰後に1回だけ完了しました。QA0.2.89のAFK経路の受入も保持しています。関連回帰確認はWindows293件・Linux292件（変更箇所の最終再試験を含む）、実ソースJavaScriptの模擬検証24項目です。他モード、通信断や再起動後の再送、双方退出などは未受入です。

QA0.2.91ではPrivate選択の保存を修正しました。両ルールで通常再起動後の選択保持を確認し、拠点戦では自主退出後の選択保持、退出理由と使用構成の保存、本人用／公開戦績の一致を確認しました。関連Linux29件とWindows上の実JavaScriptハーネス3本が通過しています。拠点戦では相手の通常勝利画面、ハンガー復帰後のPrivate選択保持、両者の本人用／公開戦績一致も確認しました。自主退出側の理由と構成は相手決着後も不変です。QA0.2.91の同室再入室・結果受け取りと、殲滅戦の試合後保持は未受入です。別ルールの以前の部屋が残っている場合、誤ったルールへの復帰は拒否されますが、画面のエラー説明と復旧案内は改善が必要です。元のルールで復帰し、通常退出してから新しいルールで作成する手順は確認しました。

使用構成は既定・固定・選択スキル、消耗品、ツリー配分を含みます。使用率は構成が記録された試合を母数とし、未記録の旧試合と混ぜません。スキルの発動回数は未収集です。サイトの3言語表示は保存済みQA応答で確認しましたが、darask.me上でのEpicログインから絞り込みまでの操作は未受入です。

拠点戦3500点と中国版原本の占領設定をQAへ戻しました。実戦で通常拠点の占領と占領後の90秒ロックを確認済みですが、本陣の占領完了時間を原本と同条件で比較する検証は未完です。317ユニットはT10相当、スキル・消耗品・ツリーは中国版原本の値です。通常・プレミアムを含む武器と防具の能力値効果は無効です。

全件受入・本番配信は未完です。Private選択保持の残る対戦条件と、ロビー競合時の案内は未受入です。全ユニットの実機能力、3〜4人パーティ、残る切断・取消し・再接続条件、長時間対戦、BAN・Kick、対戦統計、更新やOS・ランチャー異常終了からの復旧、負荷、物理PC再起動、リプレイなどの要望が残っています。短いTCP断から約0.43秒で再接続して対戦を継続できることは確認済みです。GPU QAはRTX5060 Tiで継続し、PRO6000は使用していません。

## English

**Maintenance continues. New sign-ins and matchmaking remain paused, with no reopening date. Production has not been updated.** Both VMs run signed QA0.2.91; the cloud QA distribution manifest remains a separate 0.2.63. The last successfully checked public stable launcher was 0.2.43; subsequent status requests returned HTTP 403 and need rechecking.

Five restored map definitions—Changban Territory and both rulesets for Mycale and Vesuvius—passed normal two-player matches, both final histories, six complete loadouts, matching self/public APIs, and return to the same room. The candidate contains 16 terrains with two rulesets each.

Private Territory and Private Annihilation have separate entries. Live English, Japanese and Russian screens were checked. Both room types, normal exit and switching rules without restarting passed in Japanese and Russian. Map changes and invitations now preserve the room ruleset. The additional expired-room Unready path was fixed and passed 90 tests on each OS; live exit from an idle expired room and creation of a new room without restarting also passed. Expiry during combat and other conditions remain open.

QA0.2.90 adds voluntary-quit recording and prevents ordinary results from being classified as departures. One live Private Annihilation match passed quit and loadout recording, matching self/public history, the opponent’s ordinary victory, and both clients returning to the same room. The quit reason and loadout remained unchanged after the opponent finished; the result was delivered once after its owner returned. The earlier QA0.2.89 AFK acceptance remains valid. Related regression coverage is 293 Windows and 292 Linux tests, including final checks of changed modules, plus 24 checks using the actual JavaScript source. Other modes, live retries after network failure or restart, and both players quitting remain open.

QA0.2.91 fixes saving the Private selection. Both rulesets retained their selection after a normal restart. In Territory, voluntary quit also retained the selection and saved the departure reason and loadout with matching self/public history. Related checks passed: 29 Linux tests and three actual-JavaScript harnesses on Windows. Territory also passed the opponent’s ordinary victory screen, retention of the Private selection on return to the hangar, and matching self/public histories for both clients. The quitter’s reason and loadout remained unchanged after the opponent finished. Same-room re-entry and result delivery on QA0.2.91, and post-battle Annihilation retention, remain pending. An existing room with different rules correctly prevents restoration into the wrong mode, but its error message and recovery guidance need improvement. Returning under the old rules, leaving normally, and then creating under the new rules was verified.

Snapshots include default, fixed and selected skills, consumables and ability-tree allocations. Usage rates count recorded builds and exclude older matches without that data; skill activation counts are not collected. Three-language site rendering was checked with saved QA responses; live Epic login and filtering on darask.me remain pending.

Territory uses 3500 points and Chinese-original capture settings in QA. Ordinary capture and the 90-second post-capture lock passed live checks; comparing base-capture completion time with an unchanged original under identical conditions is still open. All 317 units use T10-equivalent stats, original skill/consumable/tree values, and disabled weapon/armour effects, including premium equipment.

Remaining post-battle Private retention cases and guidance for conflicting rooms still need acceptance. Full acceptance and release remain unfinished: all unit abilities, three/four-player parties, remaining disconnect/cancel/reconnect cases, long sessions, bans/kicks, full statistics, update/OS/launcher crash recovery, load, physical-PC reboot and requested features such as replays. A short TCP interruption recovered in about 0.43 seconds with combat continuing. GPU QA uses RTX5060 Ti; PRO6000 is not in use.

## Русский

**Техническое обслуживание продолжается. Новый вход и подбор матчей приостановлены; дата возобновления не назначена. Публичный выпуск не изменён.** Обе VM используют подписанный QA0.2.91; облачный QA-манифест остаётся отдельной версией 0.2.63. Последняя успешно проверенная публичная стабильная версия — 0.2.43; последующие запросы состояния вернули HTTP 403 и требуют повторной проверки.

Пять восстановленных определений карт — Changban Territory и оба режима Mycale и Vesuvius — прошли обычные бои двух игроков: подтверждены оба итога, составы шести отрядов, совпадение личного и публичного API и возврат в ту же комнату. Кандидат содержит 16 ландшафтов с двумя режимами каждый.

Для Private Territory и Private Annihilation реализованы отдельные пункты. Проверены экраны на английском, японском и русском. На японском и русском подтверждены оба типа комнат, обычный выход и смена правил без перезапуска. Смена карты и приглашения сохраняют режим комнаты. Исправлен дополнительный путь Unready перед выходом из просроченной комнаты; пройдены 90 тестов на каждой ОС. Также подтверждены обычный выход из просроченной комнаты в ожидании и создание новой без перезапуска. Истечение срока во время боя и другие условия ещё требуют проверки.

QA0.2.90 добавляет запись добровольного выхода и защиту от ошибочной классификации обычного итога как выхода. В одном реальном бою Private Annihilation подтверждены запись выхода и состава, совпадение личной и публичной истории, обычная победа соперника и возврат обоих клиентов в ту же комнату. Причина выхода и состав не изменились после завершения соперником; результат получен один раз после возвращения владельца. Приёмка AFK-пути QA0.2.89 остаётся действительной. Регрессионные проверки: 293 на Windows и 292 на Linux, включая финальную перепроверку изменённых модулей, а также 24 проверки фактического JavaScript-кода. Другие режимы, повторная отправка после разрыва связи или перезапуска и выход обоих игроков ещё не приняты.

Снимки включают стандартные, фиксированные и выбранные навыки, расходники и распределение дерева. Доли использования учитывают записанные составы; старые бои без этих данных исключены. Число активаций навыков не собирается. Отображение сайта на трёх языках проверено с сохранёнными QA-ответами; вход Epic и фильтрация на darask.me ещё не приняты.

В QA восстановлены 3500 очков Territory и исходные китайские настройки захвата. В игре проверены обычный захват и блокировка на 90 секунд после него; сравнение полного времени захвата базы с неизменённым оригиналом при одинаковых условиях ещё не выполнено. Все 317 отрядов имеют характеристики уровня T10, исходные значения навыков, расходников и дерева. Эффекты оружия и доспехов, включая премиальные, отключены.

QA0.2.91 исправляет сохранение выбранного Private-режима. Для обоих режимов подтверждено сохранение выбора после обычного перезапуска. В Territory также подтверждены сохранение выбора после добровольного выхода, запись причины и состава и совпадение личной и публичной истории. Пройдены 29 тестов Linux и три проверки реального JavaScript-кода в Windows. В Territory также подтверждены экран обычной победы соперника, сохранение Private-режима при возврате в ангар и совпадение личной и публичной истории обоих клиентов. Причина выхода и состав не изменились после завершения соперником. Возврат в ту же комнату и получение результата на QA0.2.91, а также сохранение Annihilation после боя ещё не приняты. Если осталась комната с другим режимом, восстановление в неверном режиме корректно запрещается, но сообщение об ошибке и указания по восстановлению требуют улучшения. Проверен возврат в прежнем режиме, обычный выход и последующее создание комнаты с новыми правилами.

Полная приёмка и выпуск не завершены: способности всех отрядов, группы из трёх/четырёх игроков, оставшиеся случаи разрыва/отмены/переподключения, длительные сессии, блокировки и исключения, полная статистика, восстановление после сбоев обновления/ОС/лаунчера, нагрузка, перезапуск физических ПК и запросы вроде реплеев. Краткий обрыв TCP восстановился примерно за 0,43 секунды с продолжением боя. GPU QA работает на RTX5060 Ti; PRO6000 не используется.

Report issues through the [support form](https://github.com/daraskme/twa-revival-support/issues/new/choose). Do not publish passwords, tokens, account IDs or raw logs.
