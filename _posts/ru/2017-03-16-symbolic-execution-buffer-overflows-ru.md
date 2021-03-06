---
layout: article
title: "Применение статического символьного выполнения для поиска ошибок доступа к буферу"
ref: programming2017
lang: ru

pub_authors: "Дудина И.А., Белеванцев А.А."
pub_journal: "Программирование, № 5, с. 3-17 "
pub_year: 2017
pub_keywords: "переполнение буфера, символьное исполнение"

---

Ошибки доступа к буферу остаются одним из наиболее серьезных источников ошибок и уязвимостей в программах на языках Си и Си++. Для их обнаружения в числе прочих подходов используется статический анализ. В данной работе предложен метод чувствительного к путям статического анализа, основанный на символьном исполнении с объединением состояний. Для буферов с известным в момент компиляции размером предложен межпроцедурный чувствительный к путям и контексту алгоритм, позволяющий находить
ситуации, удовлетворяющие введенному формальному определению ошибки. Данный алгоритм был реализован в инструменте статического анализа Svace, при этом удалось избежать существенного ухудшения производительности. На проекте Android 5.0.2 было получено 351 предупреждение об ошибке доступа к буферу, среди которых 64% оказались истинными. Также в статье рассматривается прототип внутрипроцедурного детектора для обнаружения ошибок доступа к буферу, расположенному в динамической
памяти, и приводится пример найденного им дефекта.
