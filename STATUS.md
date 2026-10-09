# Service and update status / 運用・更新状況 / Состояние сервиса

Updated: **2026-10-10 00:03 JST**. [Project](https://darask.me/twa/) · [Support](README.md) · [Launcher source](https://github.com/daraskme/twa-revival-launcher) · [Server source](https://github.com/daraskme/twa-revival-server)

## 日本語

**メンテナンスを継続しています。新規ログイン・マッチングの受付再開日は未定です。** 進行中の試合の中継は継続する運用です。10月9日の[公開状態](https://staging-api.darask.me/health)確認では受付停止・終了時刻なしでした。[公開安定版](https://downloads.darask.me/launcher-manifests/stable.json)は0.2.43です。この資料更新はゲーム配信・受付再開ではありません。

未配信候補QA0.2.68と更新済みQAサーバーで、RTX 5060 Ti 16GBの実戦から戦績・使用率まで確認できました。同じゲーム起動中に通常PvPを2戦完走し、後半の試合では3部隊の9スキル（既定スキルと選択したスキル）、各部隊の消耗品、ツリーの振り方を開始時から終了時まで保存。本人と公開の戦績が一致し、構成を記録していない旧試合はスキル使用率の母数へ混ぜていません。

追加の2台パーティPvPも両者の入場から結果確定・戦績配信まで確認し、公開・本人戦績が一致しました。QA0.2.70では、通知用の空メッセージをチャットエラーと誤認する問題を修正し、実機でエラーが消えたことを確認しました。Arcaniへの変更と消耗品2枠の保存、更新後の画面設定・ツリー配分の保持も確認済みです。Arcaniの実戦でも、固定・既定スキル、2枠の消耗品、ツリー配分が結果確定後の戦績と公開使用率に一致しました。両VMのWindows再起動後も設定を保持し、ゲームが格納庫へ戻ることを確認しました。

QA0.2.71ではチャット通信失敗の原因分類を改善し、プレイヤーが書き出す診断ログへも記録されるよう修正しました。両VMで署名更新・全ファイル照合・起動・構成と画面設定の保持を確認済みです。ログはメッセージ本文や認証情報を含まず、同一エラーの大量出力を抑制します。

同じ試合の別クライアントは全滅後にAFK退出し、終了通知が届かず戦績が未確定のまま残りました。この試合を「両者正常完走」とは扱っていません。無操作5分のAFK設定は維持し、退出後の結果待ちと低フレームレートの原因を調査中です。

実QAデータをサイトへ読み込む表示検査では、日本語・英語・ロシア語の詳細と4種類の集計を確認しました。これは取得済みAPI応答を使った表示検査で、本番サイトとEpicログインの最終受入は残っています。発動回数は未取得で、選択・持ち込み数とは区別します。

通常・プレミアムの武器と防具の能力値効果はすべて無効です。中国版の未改変スキル・消耗品・ツリー値と全317ユニットのT10相当基礎値を保持しています。現候補のサーバー1,022件とWindows304件の自動検査が成功しました。所有スキルと部隊ごとの選択を混同する問題も修正済みです。

**全不具合の受入と本番配信は未完了です。** 全ユニット、3〜4人パーティ・Private部屋、切断・長時間稼働、BAN/Kick、RTX PRO 6000での実戦などを引き続き検証します。QA配信一覧は0.2.63のままで、最新の署名付き候補0.2.71を2台の検証VMへ適用しています。GitHubの旧QAブランチも現在の内部候補とは別です。

[不具合報告](https://github.com/daraskme/twa-revival-support/issues/new/choose)には版、日時・タイムゾーン、GPU、モード、再現手順、画面のエラー文を添えてください。パスワード・トークン・アカウントID・未加工ログは公開しないでください。

## English

**Maintenance continues. New sign-ins and matchmaking remain closed, with no reopening date.** Relays for matches already in progress remain available. The October 9 [health check](https://staging-api.darask.me/health) reported maintenance without an end time. The [public stable launcher](https://downloads.darask.me/launcher-manifests/stable.json) remains 0.2.43. This documentation update does not release the game or reopen admission.

Unreleased QA0.2.68 and the updated QA backend passed a representative real-match history check on an RTX 5060 Ti 16GB Windows VM. Two normal PvP matches completed in one game process. The later match retained all nine equipped skills across three units, including defaults and explicit selections, consumables per unit and tree allocations from entry through settlement. Self and public history agreed. Older matches without complete skill records were excluded from the skill-usage denominator.

A further two-client party PvP test completed entry, settlement and history delivery for both clients; public and self records matched. QA0.2.70 fixes empty notification messages being misclassified as chat errors, with the correction verified on the running VMs. Changing to Arcani, saving both consumable slots and retaining graphics and tree settings across an update also passed. Arcani also passed real-match history checks: fixed/default skills, both consumables and tree allocations matched the settled record and public usage statistics. Both VMs retained settings across Windows reboots and returned to the game hangar.

QA0.2.71 improves chat-failure classification and includes those failures in exported player diagnostics. Both VMs passed signed installation, file verification, startup and configuration/graphics retention checks. Logs exclude message bodies and credentials and limit repeated errors.

The other client in that same match exited for AFK after its units were eliminated; no final report arrived and its result remains pending. That match is not counted as a normal completion by both clients. The five-minute inactivity policy is unchanged. Missing results after departure and low frame rates remain under investigation.

Captured real QA API responses also passed Japanese, English and Russian website checks for match details and all four usage categories. This was a frozen-response display test; final production-site and Epic-login acceptance remain pending. Activation counts are not collected and are distinct from equipped selections.

All normal and premium weapon/armour stat effects are disabled. Original Chinese skill, consumable and tree values and T10-equivalent baselines for all 317 units are preserved. The current candidate passed 1,022 backend tests and 304 Windows tests, including the fix separating owned skills from each deployed unit's actual selection.

**Full issue acceptance and production release are unfinished.** Remaining checks include all units, parties of three or four, private rooms, disconnects, sustained play, ban/kick and RTX PRO 6000 gameplay. The cloud QA launcher manifest remains 0.2.63; signed 0.2.71 is installed on both test VMs. Older public QA branches are separate snapshots.

[Report an issue](https://github.com/daraskme/twa-revival-support/issues/new/choose) with version, time/time zone, GPU, mode, reproduction steps and the displayed error. Do not publish passwords, tokens, account IDs or raw logs.

## Русский

**Техническое обслуживание продолжается. Новый вход и подбор матчей закрыты; дата открытия не назначена.** Ретрансляция начатых матчей сохранена. Проверка [состояния сервиса](https://staging-api.darask.me/health) 9 октября подтвердила обслуживание без времени окончания. [Публичный стабильный лаунчер](https://downloads.darask.me/launcher-manifests/stable.json) — 0.2.43. Обновление документации не выпускает игру и не открывает вход.

Неопубликованный QA0.2.68 с обновлённым QA-сервером прошёл выборочную проверку истории реального боя на Windows VM с RTX 5060 Ti 16GB. В одном процессе завершены два обычных PvP-матча. Во втором сохранены все девять выбранных навыков трёх отрядов, включая стандартные, расходники каждого отряда и распределение очков дерева — от входа до результата. Личная и публичная история совпали. Старые матчи без полного набора навыков исключены из знаменателя их частоты использования.

Дополнительный групповой PvP-тест с двумя клиентами подтвердил вход, итог и доставку истории для обоих; публичные и личные записи совпали. В QA0.2.70 исправлено ошибочное распознавание пустых уведомлений как ошибок чата, что подтверждено в работающих VM. Проверены смена отряда на Arcani, сохранение двух расходников, графики и дерева после обновления. В реальном бою Arcani также подтверждены фиксированные и стандартные навыки, оба расходника и распределение дерева: итоговая история и публичная статистика совпали. Обе VM сохранили настройки после перезапуска Windows и вернулись в ангар.

В QA0.2.71 улучшена классификация сбоев чата и их включение в экспортируемую диагностику. В обеих VM проверены подписанное обновление, все файлы, запуск и сохранение настроек. Тексты сообщений и данные входа не записываются; повторяющиеся ошибки ограничены.

Другой клиент в том же бою вышел по AFK после потери всех отрядов; итоговый отчёт не поступил, результат остаётся незавершённым. Этот бой не считается нормальным завершением обоих клиентов. Пятиминутный предел бездействия сохранён. Отсутствующий итог после выхода и низкая частота кадров ещё исследуются.

Сохранённые ответы реального QA API проверены в японском, английском и русском интерфейсах: подробности боя и четыре категории статистики. Это проверка отображения записанных ответов; итоговая проверка публичного сайта и входа Epic ещё предстоит. Число применений навыков не собирается и не заменяется числом выбранных наборов.

Отключены изменения характеристик от всего обычного и премиального оружия и доспехов. Сохранены исходные китайские значения навыков, расходников и дерева, а также базовые характеристики уровня T10 для всех 317 отрядов. Текущий кандидат прошёл 1022 серверных теста и 304 теста Windows. Исправлено смешение владения навыком с фактическим выбором каждой копии отряда.

**Полная приёмка ошибок и выпуск в production не завершены.** Продолжаются проверки всех отрядов, групп из трёх и четырёх игроков, приватных комнат, отключений, длительной игры, блокировок и исключений, а также боёв на RTX PRO 6000. Облачный QA-манифест пока содержит 0.2.63; подписанный 0.2.71 установлен в обе тестовые VM. Старые публичные QA-ветки — отдельные снимки.

В [сообщении об ошибке](https://github.com/daraskme/twa-revival-support/issues/new/choose) укажите версию, время и часовой пояс, GPU, режим, шаги и текст ошибки. Не публикуйте пароли, токены, ID аккаунтов и необработанные журналы.
