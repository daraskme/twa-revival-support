# Service and update status / 運用・更新状況 / Состояние сервиса

Updated: **2026-10-09 JST**. [Project](https://darask.me/twa/) · [Support](README.md) · [Launcher source](https://github.com/daraskme/twa-revival-launcher) · [Server source](https://github.com/daraskme/twa-revival-server)

## 日本語

**メンテナンスを継続しています。新規ログインとマッチングを停止しており、再開日時は未定です。** 進行中の試合の中継を継続する方針で、既存中継は停止していません。10月9日の[公開health](https://staging-api.darask.me/health)でメンテナンスON・終了時刻なしを確認しました。

公開ランチャーのstableは**0.2.43**です（10月9日の[配信一覧](https://downloads.darask.me/launcher-manifests/stable.json)確認）。検証環境の最終配信は0.2.63。GitHubの旧0.2.48 QAブランチと、現在の内部統合候補は別のものです。この資料更新でゲームの新版を配信したり、受付を再開したりしていません。

次回更新に向けて取り組んでいる内容:

- マッチング、起動・終了、Private部屋、結果保存の不具合を修正し、どの段階で失敗したか分かる診断ログを追加。
- 中国版の未改変原本を基準に、スキル・消耗品・アビリティツリーの数値と配分ポイントを確認し、全ユニットをT10相当に統一。
- 戦績と試合時のツリー配分・スキル・消耗品を保存し、サイトで条件を絞って使用状況を分析できるようにする。
- BAN/Kick・期間付き停止と監査機能を検証。

RTX 5060 Ti 16GBのWindows VMで、QA0.2.63に最小修正を加えた通常PvPを1戦完走し、結果画面・格納庫復帰・戦績増加を確認しました。前回固定候補のWindows315件とbackend1015件の自動検査も成功しています。**全装備スキルの採取、全ユニット、2クライアントの結果・再戦、最終署名パッケージとサイトを含む全体受入は未完了です。** すべての不具合が直ったとはまだ判断していません。

10月9日の追加修正では、戦績の通信停止・ページ切替の競合・再試行・認証切れ後の表示と、同時更新でダウンロード一時ファイルが衝突する問題を対処しました。更新処理の回帰52件、Windows実機の追加2件、戦績の通信4件・画面6ケースを検証済みです。これらは未配信候補の検証で、全体受入完了ではありません。

追加検証では、スキル交換の再起動保持と実戦発動を確認し、通常PvPの完走確認が累計2戦になりました。今回の勝利も戦績へ保存・配達されています。別PCでWindows追加回帰92件、最新のサーバー修正全体で1,020件と型検査が成功しました。試合結果の復旧、Private試合の再取得・期限処理、集計の欠測扱いと重複消耗品を修正し、不変の待機状態を書き直す処理も削減しました。承認済みのOpus5.5追加レビューは完了しています。これらも未配信で、全装備記録と全件受入は引き続き作業中です。

未観測のスキルを「使用率0%」にはしません。明示的に保存された選択と、実際の装備・戦闘中の発動は区別します。新しい分析機能は未公開です。

不具合報告は[問い合わせ](https://github.com/daraskme/twa-revival-support/issues/new/choose)へ。版、日時・タイムゾーン、GPU、モード、再現手順、画面のエラー文を記載してください。パスワード・トークン・アカウントID・未加工ログは公開しないでください。

## English

**Maintenance remains enabled. New sign-ins and matchmaking are unavailable; there is no reopening date yet.** Existing battle relays have been left running so matches already in progress can continue. The [public health response](https://staging-api.darask.me/health) on October 9 reported maintenance enabled with no end time.

The public stable launcher remains **0.2.43**, checked against its [manifest](https://downloads.darask.me/launcher-manifests/stable.json) on October 9. The last deployed QA launcher is 0.2.63. The older public 0.2.48 QA branch is a separate snapshot, not the current integrated candidate. This documentation update does not release a new game build or reopen admission.

Work for the next update covers matchmaking, launch/exit, private-room and result-persistence fixes; diagnostics that identify the failing stage; original Chinese skill, consumable and ability-tree values and point budgets with T10-equivalent units; match-time build history and website filters/statistics; and auditable ban, kick and timed-suspension controls.

One normal PvP match completed on an RTX 5060 Ti 16GB Windows VM using QA0.2.63 plus a minimal patch. Result screens, return to the hangar and the career increment were verified. The previous frozen candidate passed 315 Windows tests and 1,015 backend tests. **Complete equipped-skill capture, all-unit acceptance, both clients' results/rematches, and acceptance of the final signed package and website remain unfinished.** This does not establish that every reported problem is fixed.

Additional October 9 fixes address stalled history requests, overlapping page/detail loads, retries, stale displays after authentication expiry, and concurrent updaters colliding on a download temporary file. Validation includes 52 updater regression tests, 2 additional Windows VM cases, 4 history timeout tests and 6 browser recovery/authentication cases. These changes remain unreleased and do not establish full candidate acceptance.

Further QA verified skill replacement across a clean restart and activation in battle; two normal PvP matches have now completed in the patched QA baseline, with the latest victory saved and delivered. An additional 92 Windows regression tests passed on the other PC. All 1,020 backend tests and type checking passed with the latest fixes for result recovery, private-battle replay and expiry, missing-catalogue aggregation and duplicate consumables. Unchanged matchmaking polls also avoid redundant state and alarm writes. The approved additional Opus5.5 review is complete. These changes remain unreleased; full equipment capture and complete acceptance are still in progress.

Unobserved skills will not be shown as 0% usage. Saved explicit selections, equipped loadouts and actual activations are different observations. The new analytics features are not public yet.

Use [support](https://github.com/daraskme/twa-revival-support/issues/new/choose) to report a problem. Include version, time/time zone, GPU, mode, reproduction steps and the displayed error. Do not publish passwords, tokens, account IDs or raw logs.

## Русский

**Техническое обслуживание продолжается. Новый вход и подбор матчей недоступны; дата возобновления пока не назначена.** Ретрансляция уже начавшихся матчей оставлена включённой, чтобы игроки могли продолжить их. В ответе [публичного API состояния](https://staging-api.darask.me/health) от 9 октября обслуживание включено, время окончания не задано.

Публичная стабильная версия лаунчера — **0.2.43**, по [манифесту](https://downloads.darask.me/launcher-manifests/stable.json), проверенному 9 октября. Последняя установленная в QA версия — 0.2.63. Старая публичная ветка QA0.2.48 — отдельный снимок, а не текущий объединённый кандидат. Обновление документации не выпускает новую сборку игры и не возобновляет приём игроков.

Для следующего обновления проверяются исправления подбора матчей, запуска и завершения игры, приватных комнат и сохранения результатов; журналы с указанием этапа ошибки; исходные значения навыков, расходников и дерева способностей китайской версии с силой всех отрядов на уровне T10; история составов на момент боя, фильтры и статистика на сайте; блокировки, исключение из боя и временные ограничения с журналом действий.

На Windows VM с RTX 5060 Ti 16GB завершён один обычный PvP-матч с QA0.2.63 и минимальным исправлением. Проверены экраны результатов, возврат в ангар и увеличение счётчика боёв. Предыдущий зафиксированный кандидат прошёл 315 тестов Windows и 1015 тестов сервера. **Полный сбор выбранных навыков, проверка всех отрядов, результатов обоих клиентов и повторных боёв, итогового подписанного пакета и сайта ещё не завершены.** Это не означает, что все заявленные ошибки исправлены.

Дополнительные исправления от 9 октября устраняют зависание запросов истории, конфликт загрузки списка и подробностей, проблемы повторного запроса, устаревшее отображение после истечения авторизации и конфликт временного файла при одновременном обновлении. Проверены 52 регрессионных теста обновления, 2 дополнительных случая на Windows VM, 4 теста тайм-аута истории и 6 браузерных сценариев восстановления и авторизации. Эти изменения ещё не опубликованы и не означают завершения полной приёмки.

Дополнительная проверка подтвердила сохранение замены навыка после перезапуска и его применение в бою. На исправленной QA-сборке завершено уже два обычных PvP-матча; последняя победа сохранена и доставлена клиенту. На другом ПК пройдены ещё 92 регрессионных теста Windows. Последние исправления прошли все 1020 серверных тестов и проверку типов: восстановление результатов, повторное получение приватного боя и сроки комнаты, неизвестные исторические каталоги и повторные расходники. Убраны лишние записи неизменившейся очереди и таймера. Дополнительное согласованное ревью Opus5.5 завершено. Изменения ещё не опубликованы; полный учёт снаряжения и общая приёмка продолжаются.

Неизвестные навыки не будут показаны как 0% использования. Сохранённый выбор, фактически выбранный набор и применение навыка в бою учитываются отдельно. Новая аналитика пока не опубликована.

Для сообщения об ошибке используйте [поддержку](https://github.com/daraskme/twa-revival-support/issues/new/choose). Укажите версию, время и часовой пояс, видеокарту, режим, шаги воспроизведения и текст ошибки. Не публикуйте пароли, токены, ID аккаунтов и необработанные журналы.
