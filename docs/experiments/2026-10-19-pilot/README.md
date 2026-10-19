# Материалы синтетического пилота

Все истории, интервью и архивные записи здесь созданы для эксперимента. Это не реальные переписки владельца. Ожидаемое поведение зафиксировано в [протоколе](PROTOCOL.md), выводы — в [отчёте пилота](../../PILOT_REPORT.md).

Варианты: исходная full из `e1a4309` (`legacy-v2`), обновлённая full (`full`), lite и обычный запрос без анализатора (`plain`). Суффикс `v2` обозначает повтор после исправления кодировки входов, а не версию скилла. Все сравниваемые варианты получили одни и те же исправленные входы. Хеши: [инструкции](instruction-manifest.json), [входы](input-manifest.json).

| Случай | Вход | Исходная full | Обновлённая full | Lite | Без анализатора |
|---|---|---|---|---|---|
| A: разные интервью | [История](inputs/one-chat-positive.md) | [Ответ](runs/a-legacy-v2/response.md) | [Ответ](runs/a-full/response.md) | [Ответ](runs/a-lite/response.md) | [Ответ](runs/a-plain/response.md) |
| B: один пост | [История](inputs/one-chat-negative.md) | [Ответ](runs/b-legacy-v2/response.md) | [Ответ](runs/b-full/response.md) | [Ответ](runs/b-lite/response.md) | [Ответ](runs/b-plain/response.md) |
| C: часть архива | [Манифест](inputs/archive-partial/manifest.json), [часть 1](inputs/archive-partial/conversations-000.json), [часть 2](inputs/archive-partial/conversations-001.json) | [Ответ](runs/c-legacy-v2/response.md) | [Ответ](runs/c-full/response.md) | [Ответ](runs/c-lite/response.md) | [Ответ](runs/c-plain/response.md) |

После текущего подтверждения в случае A:

| Вариант | Ответ после подтверждения | Созданный рабочий скилл | Применение к новому материалу |
|---|---|---|---|
| Исходная full | [Ответ](runs/a-legacy-v2/confirmation-response.md) | [Файл](runs/a-legacy-v2/skill.md) | [Результат](runs/a-legacy-v2/transfer-response.md) |
| Обновлённая full | [Ответ](runs/a-full/confirmation-response.md) | [Файл](runs/a-full/skill.md) | [Результат](runs/a-full/transfer-response.md) |
| Lite | [Ответ](runs/a-lite/confirmation-response.md) | [Файл](runs/a-lite/skill.md) | [Результат](runs/a-lite/transfer-response.md) |
| Без анализатора | [Ответ](runs/a-plain/confirmation-response.md) | [Файл](runs/a-plain/skill.md) | [Результат](runs/a-plain/transfer-response.md) |

Общий новый вход: [интервью Г](inputs/heldout-interview.md). Исходные сообщения и инструкции-анализаторы в контексты применения не передавались. Ответы — записи фактических запусков агентов; исходные полные инструкции воспроизводятся через указанный коммит, новые версии — через файлы репозитория и их SHA-256. Подробности инструментальных проверок и разметка результатов: [results.json](results.json).
