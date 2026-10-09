# Service and update status / 運用・更新状況 / Состояние сервиса

Updated: **2026-10-10 02:00 JST**. [Project](https://darask.me/twa/) · [Support](README.md) · [Launcher source](https://github.com/daraskme/twa-revival-launcher) · [Server source](https://github.com/daraskme/twa-revival-server)

## 日本語

**メンテナンス継続・受付再開日は未定です。今回、本番の配信変更・受付再開は行っていません。** 最後に正常取得できた公開安定版は0.2.43です。最新の公開状態照会はHTTP 403となったため、新しい状態確認が完了したとは扱っていません。

QA0.2.73の2台Private対戦で、双方の入場、正常な勝敗確定、戦績保存、結果受け取りまで確認しました。主催者が先に部屋へ戻ると参加者の結果受け取りだけ完了しない問題を修正し、実機でも「相手の復帰では受け取らず、自分の復帰で一度だけ受け取る」ことを確認しました。Private招待の503エラーは修正が残っています。

試合に出した6部隊について、既定・固定・選択スキル、消耗品、ツリー配分を記録し、本人と公開の戦績APIが一致しました。使用率は実際の構成を保存した試合を母数とし、情報のない旧試合を混ぜません。スキルの発動回数は未収集です。サイトの日本語・英語・ロシア語での保存済みQA応答の表示確認は済んでいますが、darask.me上のEpicログインから絞り込みまでの最終操作確認は残っています。

**拠点戦は3500点・中国版原本の占領設定に戻す方針です。** 未配信QA0.2.74を両VMへ署名付き適用しました。基地の必要占領量を3000、占領後のロックを90秒へ戻し、兵種別占領速度・倍率・ユニットの占領力を含む原本照合を実施しました。実戦での占領時間の確認は継続中です。

通常・プレミアムの武器と防具の能力値効果は全無効です。317ユニットのT10相当、スキル・消耗品・ツリーの中国版原本値を維持しています。QA0.2.73はWindows統合394件と追加の回帰86件、QA0.2.74の変更箇所はWindows8件・装備等の境界11件・生成器6件・サーバー関連35件が成功しました。試験は重複を含むため合算しません。

**全件受入と本番配信は未完です。** 3〜4人パーティ、切断・取消し・再接続、長時間・連続対戦、AFK退出後の未確定結果、全ユニットと砲兵・象の能力、対戦統計の全項目、更新中断・修復、BAN・Kick、RTX PRO6000と負荷、PC本体再起動後の確認が残っています。リプレイ・追加マップ等の新機能要望も未完です。クラウドのQA配布マニフェストは0.2.63のままで、VMの署名済み0.2.74とは別です。

## English

**Maintenance continues; no reopening date is set. No production release or admission change was made.** The last successfully checked public stable launcher was 0.2.43. The latest public status request returned HTTP 403, so a fresh status verification is still pending.

Two real QA0.2.73 Private clients completed entry, final results, history storage and result delivery. The owner-first return bug is fixed: a peer returning does not acknowledge your result; your own return delivers it exactly once. Private invitations still have an unresolved 503 error.

All six deployed units recorded default, fixed and selected skills, consumables and tree allocations. Self and public history APIs agreed. Usage statistics exclude old matches without complete snapshots; skill activation counts are not collected. Recorded QA responses render in Japanese, English and Russian, but final Epic sign-in and filtering checks on darask.me remain pending.

QA0.2.74 is installed and signature-verified in both VMs. Territory is being restored to **3500 points and Chinese-original capture settings**, including a base capture amount of 3000 and a 90-second post-capture lock. Capture tables, multipliers and unit capture power were compared with the original. Actual capture timing remains under verification. All weapon/armor stat effects remain disabled; T10-equivalent units and original skill, consumable and tree values are retained.

Full acceptance and production release remain pending: three/four-person parties, disconnect/cancel/reconnect, long sessions, AFK result handling, all unit families, full statistics, update interruption/repair, ban/kick, GPU/load and host reboot checks. Replay and additional-map requests are also unfinished. The cloud QA download manifest remains 0.2.63; the VMs use an offline signed 0.2.74 candidate.

## Русский

**Техническое обслуживание продолжается; дата открытия не назначена. Выпуск в production и возобновление входа не выполнялись.** Последняя успешно проверенная стабильная версия — 0.2.43. Последний запрос публичного состояния получил HTTP 403; новая проверка пока не завершена.

В двух реальных клиентах QA0.2.73 проверены вход в Private-бой, итог, сохранение истории и получение результата. Исправлена ошибка, возникавшая при возвращении хозяина комнаты первым: возвращение другого игрока не подтверждает ваш результат, собственное возвращение доставляет его один раз. Ошибка 503 при приглашении в Private ещё не исправлена.

Для всех шести отрядов сохранены стандартные, фиксированные и выбранные навыки, расходники и распределение дерева. Личная и публичная история API совпали. Старые бои без полного снимка не включаются в доли использования; число активаций навыков не собирается. Отображение сохранённых QA-ответов проверено на трёх языках, но вход Epic и фильтрация на darask.me ещё требуют финальной проверки.

Подписанный QA0.2.74 установлен в обе VM. Для режима захвата возвращаются **3500 очков и исходные китайские настройки захвата**: объём захвата базы 3000 и блокировка после захвата 90 секунд. Проверены исходные таблицы, множители и сила захвата отрядов. Измерение времени в реальном бою продолжается. Эффекты всего оружия и доспехов отключены; сохранены характеристики уровня T10 и исходные значения навыков, расходников и дерева.

Полная приёмка и выпуск не завершены. Остались группы из трёх/четырёх игроков, разрывы связи и отмены, длительные сессии, результаты после AFK, все типы отрядов, полная статистика, прерывание и восстановление обновлений, блокировки/исключения, GPU/нагрузка и перезапуск физических ПК. Реплеи и дополнительные карты также не завершены. Облачный QA-манифест остаётся 0.2.63; VM используют отдельно установленный подписанный кандидат 0.2.74.

Report issues through the [support form](https://github.com/daraskme/twa-revival-support/issues/new/choose). Do not publish passwords, tokens, account IDs or raw logs.
