---
layout: article
title: "Разработка и реализация облачного планировщика, учитывающего топологию коммуникационной среды при высокопроизводительных вычислениях"
ref: trudy24
lang: ru

pub_authors: " Дудина И.А., Кудрявцев А.О., Гайсарян С.С. "
pub_journal: "Труды Института системного программирования РАН, том 24, 2013, стр. 35-48."
pub_year: 2013
pub_keywords: "планирование, виртуализация, облачные вычисления, hop-byte метрика"
pub_doi: "10.15514/ISPRAS-2013-24-2"

---

Для эффективного решения высокопроизводительных задач в облаке необходимо планирование виртуальных машин на серверах, учитывающее особенности высокопроизводительных вычислений, чтобы уменьшить потери производительности, связанные с задержками в сети. В данной работе рассматривается подход к планированию, основанный на оценке размещения с помощью Hop-Byte метрики. Для конкретного варианта коммуникационной среды (сети Infiniband с топологией «толстое дерево») производится подсчет Hop-Byte
метрики в предположении, что взаимодействие между виртуальными машинами одинаково. На основе полученных результатов разработан алгоритм планирования, выполнена его реализация в облачной системе OpenStack. Показано, что для отдельных тестов удается получить прирост производительности, при этом существенно снижается разброс значений при повторных запусках.