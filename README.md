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

2026-10-10のQAでは、復旧した5マップ定義の通常対戦と両者の戦績保存を確認しました。「Private拠点戦」「Private殲滅戦」の二つの入口も実装済みです。QA0.2.88では日本語・ロシア語それぞれの実画面で両ルールの作成・通常退出・切り替えを確認しました。QA0.2.89のAFK経路に加え、QA0.2.90では殲滅戦1試合の自主退出保存、相手の通常勝利、両者の同室復帰まで確認しました。QA0.2.91では両Private選択の再起動保持と、拠点戦の自主退出記録、相手の通常勝利、ハンガー復帰後の選択保持、本人用／公開戦績一致を確認しました。未配信で、残る確認項目は[運用・更新状況](STATUS.md)に記載しています。

不具合や遊び方についてIssuesから連絡できます。閲覧は誰でもできます。投稿にはGitHubアカウントが必要です。日本語・英語・ロシア語に対応しています。

報告には、分かる範囲で次の情報を添えてください。

- ランチャーのバージョン、Windowsのバージョン、GPU名。
- 発生日時とタイムゾーン、操作手順、期待した動作と実際の動作。
- マッチング・読み込みの問題：ソロかパーティか、人数、モード、マップ、何分待ったか。
- 起動・設定保存の問題：画面のエラー文、再起動前後で変わる設定、表示されるポート番号。

**投稿内容は公開されます。** パスワード、認証コード、トークン、メールアドレス、アカウントID、未加工のログは投稿しないでください。スクリーンショットの個人情報は隠してください。診断ファイルが必要な場合は、公開Issueに添付する前に運営の案内を待ってください。

アカウント情報の確認・修正・削除は、最初に「アカウントについて相談したい」とだけ記載してください。運営が本人確認と対応範囲を案内します。公開投稿やプレイヤーネームだけで本人確認は完了しません。Epicアカウント自体の削除は扱いません。

## English

QA on 2026-10-10 confirmed normal matches and both players’ histories for five restored map definitions. Separate Private Territory and Private Annihilation entries are implemented. QA0.2.88 also verified both room types, normal exit, and rule switching in the live Japanese and Russian clients. In addition to the QA0.2.89 AFK path, QA0.2.90 passed voluntary-quit recording, the opponent’s ordinary victory and both clients returning to the same room in one live Annihilation match. QA0.2.91 also verified restart retention for both Private choices and Territory quit recording, the opponent’s ordinary victory, selection retention on return to the hangar, and matching self/public histories. These changes are unreleased; outstanding checks are listed in [service status](STATUS.md#english).

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

В QA от 2026-10-10 подтверждены обычные бои и история обоих игроков для пяти восстановленных определений карт. Реализованы отдельные пункты Private Territory и Private Annihilation. В QA0.2.88 также проверены создание обоих типов комнат, обычный выход и смена правил в работающем клиенте на японском и русском языках. Помимо AFK-пути QA0.2.89, в QA0.2.90 подтверждены запись добровольного выхода, обычная победа соперника и возврат обоих клиентов в ту же комнату в одном бою Annihilation. В QA0.2.91 также проверены сохранение обоих Private-режимов после перезапуска и запись выхода, обычная победа соперника, сохранение выбора при возврате в ангар и совпадение личной и публичной истории в Territory. Изменения ещё не выпущены; оставшиеся проверки указаны в [состоянии сервиса](STATUS.md#русский).

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
