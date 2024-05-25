---
title: Git Version Management
subtitle: In this publication, I will try to reveal to you the topic of git versioning.

# Summary for listings and search engines
summary: In this publication, I will try to reveal to you the topic of git versioning.

# Link this post with a project
projects: []

# Date published
date: '2024-03-20T23:00:00Z'

# Date updated
lastmod: '2024-03-20T23:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---

## About Version Control

A version control system is a system that records changes to a file or set of files over time and allows you to return to a specific version later. The software source code will be used as an example for versioning files in this workbook, although you can actually use version control for almost any file type.

## Local version control systems

Many people use copying files to a separate directory as a version control method (perhaps even a time-stamped directory, if they are smart enough). This approach is very common because of its simplicity, but it
incredibly highly prone to errors. You can easily forget which directory you are in and accidentally change the wrong file or copy the wrong files you wanted.

In order to solve this problem, programmers long ago developed local VCSs with a simple database that stores records of all changes in files, thereby monitoring revisions.

<img src="1.png" alt="drawing" width=55%/>

## Centralized version control systems

The next major challenge people face is the need to interact with other developers. In order to deal with it, centralized version control systems (Centralized Version Control System, hereinafter CVCS) were developed. Systems such as CVS, Subversion, and Perforce use a single server containing all versions of files, and a number of clients that receive files from this centralized repository. The use of CVCS has been the standard for many years.

This approach has many advantages, especially over local VCSs. For example, all project developers know to a certain extent what each of them is doing. Administrators have complete control over who can do what, and it is much easier to administer CVCS than to operate local databases on each client.

Despite this, this approach also has serious disadvantages. The most obvious disadvantage is a single point of failure represented by a centralized server. If this server fails for an hour, then during this time no one will be able to use version control to save the changes they are working on, and no one will be able to exchange these changes with other developers. If the hard disk on which the central database is stored is damaged, and there are no timely backups, you will lose everything - the entire history of the project, not counting the single repository snapshots that were saved on the local developer machines. Local VCSs suffer from the same problem: when the entire project history is stored in one place, you risk losing everything.

<img src="2.png" alt="drawing" width=55%/>

## Distributed version control systems

This is where Distributed Version Control System (DVCS) comes into play. In DVCS (such as Git, Mercurial, Bazaar or Darcs), clients do not just download a snapshot of all files (file status at a certain point in time) - they completely copy the repository. In this case, if one of the servers through which the developers exchanged data dies, any client repository can be copied to another server to continue working. Each copy of the repository is a complete backup of all data.

Moreover, many DVCS can simultaneously interact with several remote repositories, so you can work with different groups of people, applying different approaches at the same time within the same project. This allows you to apply several approaches at once in development, for example, hierarchical models, which is completely impossible in centralized systems.

<img src="3.png" alt="drawing" width=55%/>---
title: Управление версиями Git
subtitle: В данной публикации я постараюсь раскрыть вам тему об управлении версиями git.

# Summary for listings and search engines
summary: В данной публикации я постараюсь раскрыть вам тему об управлении версиями git.

# Link this post with a project
projects: []

# Date published
date: '2024-03-20T23:00:00Z'

# Date updated
lastmod: '2024-03-20T23:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---

## О системе контроля версий

Система контроля версий — это система, записывающая изменения в файл или набор файлов в течение времени и позволяющая вернуться позже к определённой версии. Для контроля версий файлов в этой книге в качестве примера будет использоваться исходный код программного обеспечения, хотя на самом деле вы можете использовать контроль версий практически для любых типов файлов.

## Локальные системы контроля версий

Многие люди в качестве метода контроля версий применяют копирование файлов в отдельный каталог (возможно даже, каталог с отметкой по времени, если они достаточно сообразительны). Данный подход очень распространён из-за его простоты, однако он
невероятно сильно подвержен появлению ошибок. Можно легко забыть в каком каталоге вы находитесь и случайно изменить не тот файл или скопировать не те файлы, которые вы хотели.

Для того, чтобы решить эту проблему, программисты давным-давно разработали локальные VCS с простой базой данных, которая хранит записи о всех изменениях в файлах, осуществляя тем самым контроль ревизий.

<img src="1.png" alt="drawing" width=55%/>

## Централизованные системы контроля версий

Следующая серьёзная проблема, с которой сталкиваются люди, — это необходимость взаимодействовать с другими разработчиками. Для того, чтобы разобраться с ней, были разработаны централизованные системы контроля версий (Centralized Version Control System, далее CVCS). Такие системы, как CVS, Subversion и Perforce, используют единственный сервер, содержащий все версии файлов, и некоторое количество клиентов, которые получают файлы из этого централизованного хранилища. Применение CVCS являлось стандартом на протяжении многих лет.

Такой подход имеет множество преимуществ, особенно перед локальными VCS. Например, все разработчики проекта в определённой степени знают, чем занимается каждый из них. Администраторы имеют полный контроль над тем, кто и что может делать, и гораздо проще администрировать CVCS, чем оперировать локальными базами данных на каждом клиенте.

Несмотря на это, данный подход тоже имеет серьёзные минусы. Самый очевидный минус — это единая точка отказа, представленная централизованным сервером. Если этот сервер выйдет из строя на час, то в течение этого времени никто не сможет использовать контроль версий для сохранения изменений, над которыми работает, а также никто не сможет обмениваться этими изменениями с другими разработчиками. Если жёсткий диск, на котором хранится центральная БД, повреждён, а своевременные бэкапы отсутствуют, вы потеряете всё — всю историю проекта, не считая единичных снимков репозитория, которые сохранились на локальных машинах разработчиков. Локальные VCS страдают от той же самой проблемы: когда вся история проекта хранится в одном месте, вы рискуете потерять всё.

<img src="2.png" alt="drawing" width=55%/>

## Распределённые системы контроля версий
Здесь в игру вступают распределённые системы контроля версий (Distributed Version Control System, далее DVCS). В DVCS (таких как Git, Mercurial, Bazaar или Darcs) клиенты не просто скачивают снимок всех файлов (состояние файлов на определённый момент времени) — они полностью копируют репозиторий. В этом случае, если один из серверов, через который разработчики обменивались данными, умрёт, любой клиентский репозиторий может быть скопирован на другой сервер для продолжения работы. Каждая копия репозитория является полным бэкапом всех данных.

Более того, многие DVCS могут одновременно взаимодействовать с несколькими удалёнными репозиториями, благодаря этому вы можете работать с различными группами людей, применяя различные подходы единовременно в рамках одного проекта. Это позволяет применять сразу несколько подходов в разработке, например, иерархические модели, что совершенно невозможно в централизованных системах.

<img src="3.png" alt="drawing" width=55%/>
