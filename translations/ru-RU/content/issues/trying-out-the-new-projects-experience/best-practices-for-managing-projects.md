---
title: Рекомендации по управлению проектами (бета-версия)
intro: Советы по управлению проектами в {% data variables.product.company_short %}.
allowTitleToDifferFromFilename: true
miniTocMaxHeadingLevel: 3
versions:
  fpt: '*'
  ghec: '*'
type: overview
topics:
- Projects
- Issues
- Project management
ms.openlocfilehash: 70c50bf58f99575759b91fb520fa3275127d9a49
ms.sourcegitcommit: 22d665055b1bee7a5df630385e734e3a149fc720
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2022
ms.locfileid: "145135368"
---
{% data reusables.projects.projects-beta %}

Вы можете использовать проекты для управления работой в {% data variables.product.company_short %}, где находятся ваши проблемы и запросы на вытягивание. Ознакомьтесь с советами по эффективному управлению проектами. Дополнительные сведения о проектах см. в статье [Сведения о проектах](/issues/trying-out-the-new-projects-experience/about-projects).

## <a name="break-down-large-issues-into-smaller-issues"></a>Разделение больших проблем на небольшие

Благодаря разделению большой проблемы на небольшие работа становится более управляемой и позволяет членам команды работать параллельно. Это также способствует созданию меньших запросов на вытягивание, которые проще проверять.

Для отслеживания того, как небольшие проблемы соответствуют большей цели, используйте списки задач, вехи или метки. Дополнительные сведения см. в статьях [Сведения о списках задач](/issues/tracking-your-work-with-issues/creating-issues/about-task-lists), [Сведения о вехах](/issues/using-labels-and-milestones-to-track-work/about-milestones) и [Управление метками](/issues/using-labels-and-milestones-to-track-work/managing-labels).

## <a name="communicate"></a>Взаимодействие

Проблемы и запросы на вытягивание включают встроенные возможности, позволяющие легко взаимодействовать с участниками совместной работы. Используйте @mentions, чтобы отправить оповещение о комментарии для одного пользователя или всей команды. Назначьте проблемы участникам совместной работы, чтобы сообщить об ответственности. Предоставьте ссылки на связанные проблемы или запросы на вытягивание, чтобы объяснить, как они связаны.

## <a name="make-use-of-the-description-and-readme"></a>Использование описания и файла README

Используйте описание проекта и файл README, чтобы предоставить общий доступ к сведениям о проекте.

Пример:

- объяснение назначения проекта;
- описание представлений проекта и их использования;
- включение соответствующих ссылок и пользователей для получения дополнительных сведений.

Файлы README проекта поддерживают Markdown, что позволяет использовать изображения и расширенное форматирование, например ссылки, списки и заголовки. 

Дополнительные сведения см. в статье [Создание проекта (бета-версия)](/issues/trying-out-the-new-projects-experience/creating-a-project#updating-your-project-description-and-readme).

## <a name="use-views"></a>Использование представлений

Используйте представления для разностороннего просмотра проекта.

Пример:

- Фильтрация по состоянию для просмотра всех незапущенных элементов
- Группирование по полям настраиваемого приоритета для отслеживания объема элементов с высоким приоритетом
- Сортировка поля с настраиваемой датой для просмотра элементов с самой ранней целевой датой доставки

Дополнительные сведения см. в разделе [Настройка представлений проекта](/issues/trying-out-the-new-projects-experience/customizing-your-project-views).

## <a name="have-a-single-source-of-truth"></a>Наличие единого истинного источника

Чтобы предотвратить нарушение синхронизации сведений, сохраните один источник истины. Например, отслеживайте целевую дату доставки в одном расположении вместо распределения по нескольким полям. Затем в случае сдвига целевой даты доставки необходимо обновить дату только в одном расположении.

Проекты {% data variables.product.company_short %} автоматически остаются в актуальном состоянии с данными {% data variables.product.company_short %}, такими как уполномоченные, вехи и метки. Если одно из этих полей изменяется в запросе на вытягивание или в проблеме, изменение автоматически отражается в проекте.

## <a name="use-automation"></a>Использование автоматизации

Вы можете автоматизировать задачи, чтобы меньше заниматься бесполезной работой и тратить больше времени на сам проект. Чем меньше задач вам нужно выполнять вручную, тем более вероятно, что ваш проект будет оставаться актуальным.

Проекты (бета-версия) предлагают встроенные рабочие процессы. Например, проект можно настроить так, что при закрытии проблемы автоматически будет выбираться состояние "Готово".

Кроме того, API GraphQL и {% data variables.product.prodname_actions %} позволяют автоматизировать рядовые задачи по управлению проектами. Например, для отслеживания запросов на вытягивание, ожидающих проверки, можно создать рабочий процесс, который добавляет запрос на вытягивание в проект и задает состояние "требует проверки". Этот процесс можно активировать автоматически, когда запрос на вытягивание помечается как "готовый к проверке".

- Пример рабочего процесса см. в статье [Автоматизация проектов](/issues/trying-out-the-new-projects-experience/automating-projects).
- Дополнительные сведения об API см. в статье [Использование API для управления проектами](/issues/trying-out-the-new-projects-experience/using-the-api-to-manage-projects).
- Дополнительные сведения о {% data variables.product.prodname_actions %} см. в статье [{% data variables.product.prodname_actions %}](/actions).

## <a name="use-different-field-types"></a>Использование различных типов полей

Используйте различные типы полей в соответствии со своими потребностями.

Поле итерации используется для планирования работы или создания временной шкалы. Вы можете выполнить группировку по итерации, чтобы узнать, сбалансированы ли элементы между итерациями, или можете активировать фильтр, чтобы сосредоточиться на одной итерации. Поля итерации также позволяют просматривать работу, выполненную в прошлых итерациях, что может помочь с планированием скорости и отражением достижений вашей команды. Эти поля также поддерживают перерывы, чтобы показать, когда вы и ваша команда делаете перерывы от итераций. Дополнительные сведения см. в статье [Управление итерациями в проектах](/issues/trying-out-the-new-projects-experience/managing-iterations).

Используйте поле с возможностью одного выбора для отслеживания сведений о задаче на основе предопределенного списка значений. Например, используйте его для отслеживания приоритета или этапа проекта. Так как значения выбираются из предопределенного списка, вы легко можете выполнить группирование или фильтрование, чтобы сосредоточиться на элементах с определенным значением.

Дополнительные сведения о различных типах полей см. в статье [Создание проекта (бета-версия)](/issues/trying-out-the-new-projects-experience/creating-a-project#adding-custom-fields).
