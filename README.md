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

QA0.2.103を両VMへ署名付き適用し、起動を確認しました。受付拒否案内の表示と、対戦終了後に相手より先にPrivateロビーへ戻る際のエラーを修正しています。関連90件・112件は、それぞれLinux・Windowsで成功しました。ウィンドウ表示の案内は実機単体で自動表示・通常OK・復帰まで確認しましたが、QA0.2.103で実際のマッチングから通す確認は残っています。QA0.2.102の通常対戦では両者の戦績・結果受信と、代表6部隊のT10・全スキル・消耗品・ツリー配分の保存、本人用／公開APIの一致を確認しました。一方、ゲストのロビー復帰では準備済みエラーと、その後の期限切れを観測しました。全件受入・本番配信・受付再開は未完了です。

QA0.2.98の公開殲滅戦Oasisで両者の通常決着・結果受信、全スキル・消耗品・ツリー配分と戦績保存、本人用／公開APIの一致を確認しました。同じ起動中の司令官変更→再受付→キャンセルも単独参加で成功しています。原因別ログを追加したQA0.2.99は両VMへ適用・起動確認済みです。Private経由のプロフィール不一致と期限切れ復帰の残条件、全件受入・本番配信・受付再開は未完了です。[検証状況](STATUS.md)。

不具合や遊び方についてIssuesから連絡できます。閲覧は誰でもできます。投稿にはGitHubアカウントが必要です。日本語・英語・ロシア語に対応しています。

報告には、分かる範囲で次の情報を添えてください。

- ランチャーのバージョン、Windowsのバージョン、GPU名。
- 発生日時とタイムゾーン、操作手順、期待した動作と実際の動作。
- マッチング・読み込みの問題：ソロかパーティか、人数、モード、マップ、何分待ったか。
- 起動・設定保存の問題：画面のエラー文、再起動前後で変わる設定、表示されるポート番号。

**投稿内容は公開されます。** パスワード、認証コード、トークン、メールアドレス、アカウントID、未加工のログは投稿しないでください。スクリーンショットの個人情報は隠してください。診断ファイルが必要な場合は、公開Issueに添付する前に運営の案内を待ってください。

アカウント情報の確認・修正・削除は、最初に「アカウントについて相談したい」とだけ記載してください。運営が本人確認と対応範囲を案内します。公開投稿やプレイヤーネームだけで本人確認は完了しません。Epicアカウント自体の削除は扱いません。

## English

Signed QA0.2.103 is installed and has launched on both VMs. It addresses refusal-dialog visibility and an error when a completed participant returns to a Private lobby before the owner reopens it. The related suites passed 90 and 112 tests respectively on both Linux and Windows. An isolated real-client check confirmed automatic windowed guidance, normal OK and return to the same game; end-to-end matchmaking acceptance in QA0.2.103 is still pending. A normal QA0.2.102 round verified both saved histories and result deliveries, with all skills, consumables and tree allocations preserved for the six tested T10 unit slots and matching self/public APIs. The guest lobby return encountered a prepared-room error, then a separate expiry on retry. Full acceptance, production release and reopening remain pending.

QA0.2.98 completed a normal public Annihilation round on Oasis with both results delivered, complete skills/consumables/tree allocations preserved, and matching self/public histories. A solo commander change, requeue and cancellation also passed without restarting. Signed QA0.2.99 adds cause-specific diagnostics and has been installed and launched on both VMs. The earlier Private-to-public profile mismatch, remaining expiry recovery cases, full acceptance, production release and reopening remain pending. See [QA status](STATUS.md#english).

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

Подписанная QA0.2.103 установлена и запущена на обеих VM. Исправляются видимость подсказки при отказе и ошибка возврата завершившего бой участника в Private-лобби до его повторного открытия владельцем. Связанные наборы из 90 и 112 тестов прошли на Linux и Windows. Отдельная проверка на реальном клиенте подтвердила автоматический показ подсказки в оконном режиме, обычное нажатие OK и возврат в ту же игру; сквозная проверка подбора в QA0.2.103 ещё не завершена. Обычный бой QA0.2.102 подтвердил сохранение истории и получение результатов обоими игроками, все навыки, расходники и распределение дерева для шести проверенных слотов T10, а также совпадение личного и публичного API. Возврат гостя встретил ошибку подготовленной комнаты, а повторная попытка — отдельное истечение срока. Полная приёмка, публичный выпуск и возобновление входа остаются незавершёнными.

В QA0.2.98 обычный публичный бой Annihilation на Oasis завершился у обоих игроков: результаты получены, все навыки, расходники и распределение дерева сохранены, личная и публичная история совпали. Смена командира, повторный одиночный вход в очередь и отмена также прошли без перезапуска. Подписанная QA0.2.99 с уточнением причин ошибок установлена и запущена на обеих VM. Прежнее несоответствие профиля при переходе из Private, оставшиеся случаи возврата после истечения срока, полная приёмка, публичный выпуск и возобновление входа ещё не завершены. См. [состояние QA](STATUS.md#русский).

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

Updated: 2026-10-11.
