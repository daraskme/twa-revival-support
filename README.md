# TWA Revival — Support

TWA Revivalの公開問い合わせ窓口です。daraskが個人で開発・運営しています。

- [プロジェクト・ダウンロード案内](https://darask.me/twa/)
- [プライバシーについて](https://darask.me/twa/privacy/)
- [問い合わせの案内](https://darask.me/twa/support/)
- [ランチャーの公開ソースとバージョン別の検証手順](https://github.com/daraskme/twa-revival-launcher)
- [Discordコミュニティ / Discord community / Сообщество Discord](https://discord.gg/w9vnpAJ7ET)
- [サーバーソース / Server source / Исходный код сервера](https://github.com/daraskme/twa-revival-server)
- [原作・現在のデータ比較 / Data comparison / Сравнение данных](https://darask.me/twa/source/)
- [問い合わせを作成](https://github.com/daraskme/twa-revival-support/issues/new/choose)

**メンテナンス中：新規ログイン・マッチングを停止しています。再開日時は未定です。** [現在の進捗・次回更新の確認範囲（日本語・English・Русский）](STATUS.md)。ランチャーは引き続きダウンロードできます。このリポジトリでは問い合わせを受け付けます。ランチャーの公開ソースは特定バージョンのスナップショットです。READMEの配信版・QA版の区別と検証対象バージョンを確認してください。

## 日本語

復旧5マップ定義、Private拠点戦／殲滅戦の二入口、通常対戦の戦績・使用構成保存、本陣占領の原本コードとの一致は確認済みです。 Private対戦後の公開マッチング失敗とモード選択不能は未解決です。診断修正はLinux・実Windows各35件を通過し、署名付きQA0.2.94を両VMへ適用しました。再起動直後の公開殲滅戦は受付・入場に成功。実際の通信断中に自主退出した記録がPC内に残り、接続復旧後に同じイベントとして再送され、本人用／公開戦績へ反映されることを確認しました。続いて相手が全滅後の観測中にAFKとなり、双方の退出理由と全6部隊のスキル・消耗品・ツリー配分が保持されました。この試合は通常決着の受入には含めません。再起動後の再送と残る条件は未完了です。 本番配信と受付再開はまだです。[検証状況](STATUS.md)。

不具合や遊び方についてIssuesから連絡できます。閲覧は誰でもできます。投稿にはGitHubアカウントが必要です。日本語・英語・ロシア語に対応しています。

報告には、分かる範囲で次の情報を添えてください。

- ランチャーのバージョン、Windowsのバージョン、GPU名。
- 発生日時とタイムゾーン、操作手順、期待した動作と実際の動作。
- マッチング・読み込みの問題：ソロかパーティか、人数、モード、マップ、何分待ったか。
- 起動・設定保存の問題：画面のエラー文、再起動前後で変わる設定、表示されるポート番号。

**投稿内容は公開されます。** パスワード、認証コード、トークン、メールアドレス、アカウントID、未加工のログは投稿しないでください。スクリーンショットの個人情報は隠してください。診断ファイルが必要な場合は、公開Issueに添付する前に運営の案内を待ってください。

アカウント情報の確認・修正・削除は、最初に「アカウントについて相談したい」とだけ記載してください。運営が本人確認と対応範囲を案内します。公開投稿やプレイヤーネームだけで本人確認は完了しません。Epicアカウント自体の削除は扱いません。

## English

QA has confirmed five restored map definitions, separate Private Territory/Annihilation entries, recorded normal-match histories/builds and agreement with the original capture code. Public matchmaking failure and a locked mode selector after a Private match remain unresolved. The diagnostic fix passed 35 Linux and 35 actual Windows tests, and signed QA0.2.94 is installed in both VMs. Freshly restarted clients successfully entered public Annihilation. A voluntary exit during a real network outage persisted locally and was retried as the same event after connectivity returned, with matching self/public history. The peer later became AFK during observation after losing all units; both departure reasons and all six units’ skills, consumables and tree allocations were preserved. This trial does not count as ordinary match completion. Retry after restarting and other conditions remain open. Production and admission remain unchanged. See [QA status](STATUS.md#english).

**Maintenance: new sign-ins and matchmaking are paused. No reopening date is set.** See [current progress and remaining release checks](STATUS.md#english).

Public support for TWA Revival, developed and operated by darask as an individual. The player launcher is available through the project website. The source repository documents a specific release snapshot and distinguishes production from ongoing QA; it does not promise that every branch matches the latest download.

Open an issue for a bug report or gameplay question. A GitHub account is required to post. Japanese, English and Russian are welcome. Include, where known:

- Launcher version, Windows version and GPU.
- Date, time and time zone; steps to reproduce; expected and actual behavior.
- Matchmaking or loading: solo or party, party size, mode, map and elapsed waiting time.
- Launch or settings: exact error text, which setting changes after restart, and any port number shown.

**All issues are public.** Do not post passwords, authentication codes, tokens, email addresses, account IDs or raw logs. Remove personal information from screenshots. If diagnostics are needed, wait for the operator's instructions before attaching an archive publicly.

For account access, correction or deletion requests, initially say only that you need account support. The operator will explain identity verification and the scope of the request. A public post or player name alone does not verify ownership. We cannot delete your Epic account.

## Русский

В QA проверены пять восстановленных определений карт, отдельные пункты Private Territory/Annihilation, история и составы обычных боёв и совпадение с исходным кодом захвата. Сбой публичного подбора и блокировка выбора режима после Private-боя остаются нерешёнными. Исправление диагностики прошло по 35 тестов в Linux и реальной Windows; подписанная QA0.2.94 установлена в обе VM. После перезапуска клиенты успешно вошли в публичный Annihilation. Выход во время реального обрыва сети сохранился локально и после восстановления связи был отправлен повторно как то же событие; личная и публичная история совпали. Позже соперник получил AFK во время наблюдения после потери всех отрядов. Обе причины выхода, навыки, расходники и распределение дерева всех шести отрядов сохранились. Этот бой не считается проверкой обычного завершения. Повторная отправка после перезапуска и другие условия ещё не проверены. Публичный выпуск и приём игроков не изменены. См. [состояние QA](STATUS.md#русский).

**Техническое обслуживание: новый вход и подбор матчей приостановлены. Дата возобновления не назначена.** См. [ход работ и оставшиеся проверки](STATUS.md#русский).

Открытая поддержка TWA Revival. Проект разрабатывает и поддерживает darask как частное лицо. Лаунчер для игроков доступен на сайте проекта. В репозитории исходного кода указана конкретная версия; опубликованный выпуск и изменения на проверке обозначены отдельно. Не каждая ветка соответствует последней загрузке.

Для сообщения об ошибке или вопроса создайте issue. Для публикации нужна учётная запись GitHub. Можно писать на японском, английском или русском языке. По возможности укажите:

- Версию лаунчера, версию Windows и видеокарту.
- Дату, время и часовой пояс, порядок действий, ожидаемый и фактический результат.
- При проблемах с подбором матча или загрузкой: играете ли вы в одиночку или в группе, размер группы, режим, карту и время ожидания.
- При проблемах с запуском или настройками: точный текст ошибки, какие настройки меняются после перезапуска, и указанный номер порта.

**Все обращения публичны.** Не публикуйте пароли, коды подтверждения, токены, адреса электронной почты, ID аккаунтов и необработанные журналы. Скройте личные данные на снимках экрана. Если понадобятся диагностические файлы, дождитесь указаний оператора, прежде чем прикреплять архив к публичному обращению.

Для запроса на просмотр, исправление или удаление данных сначала укажите только, что нужна помощь с аккаунтом. Оператор объяснит порядок подтверждения владельца и доступные действия. Публичное сообщение или имя игрока сами по себе не подтверждают владение аккаунтом. Удаление аккаунта Epic здесь не выполняется.

---

TWA Revival is an unofficial community project, not an official service of Creative Assembly, SEGA or Epic Games.

Updated: 2026-10-10.
