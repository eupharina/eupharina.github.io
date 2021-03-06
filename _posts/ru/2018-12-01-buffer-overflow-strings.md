---
layout: article
title: "Об одном подходе к анализу строк в языке Си для поиска переполнения буфера"
ref: trudy30-5
lang: ru

pub_authors: "Дудина И.А., Малышев Н.Е."
pub_journal: "Труды Института системного программирования РАН, том 30, вып. 5, 2018, стр. 55-74."
pub_year: 2018
pub_keywords: "статический анализ; символьное исполнение; анализ строк"
pub_doi: "10.15514/ispras-2018-30(5)-3"

---

Ошибки при работе с библиотечными функциями обработки строк в языке Си являются частой причиной переполнения буфера, что в свою очередь нередко приводит к отказу в обслуживании, некорректной работе программы или появлению эксплуатируемой уязвимости. Одним из способов устранения различных ошибок на стадии разработки программы является статический анализ. Существующие методы статического анализа, ориентированные на работу со строками, либо не обеспечивают должный уровень истинных
срабатываний, либо пропускают большое количество ошибок, либо неприменимы к промышленным программам большого размера, либо реализованы в рамках закрытых инструментов. Для наиболее полного покрытия дефектов в реальных программах необходимо обнаруживать ошибки, происходящие лишь на некоторых путях выполнения и не определяемые единственной точкой программы, и, кроме того, находить ошибки, связанные с некорректным использованием не только библиотечных, но и пользовательских функций. Целью
данного исследования является построение алгоритма поиска ошибок при работе со строками, удовлетворяющего этим свойствам, ограничению на количество ложных срабатываний (не более 40%), применимого к любым программам на языке Си и масштабирующегося на проекты из нескольких миллионов строк. Для решения этой задачи был использован ранее разработанный подход символьного исполнения с объединением состояний, который был адаптирован для поддержки строковых операций. На основе
алгоритма отслеживания операций с целыми числами был предложен алгоритм отслеживания длин строк. Разработанный алгоритм реализован в качестве одного из детекторов семейства детекторов переполнения буфера в рамках инструмента статического анализа Svace. В результате на тестовом наборе Juliet test suite на тестах, связанных с переполнением правой границы буфера, покрытие срабатываниями увеличилось с 15,4% до 41,5%, при этом не было выдано ни одного ложного предупреждения. По сравнению
с известным анализатором Infer на наборе Juliet инструмент Svace без поддержки строк показывает приблизительно те же результаты, за исключением случая сложных циклов, а связанные со строками переполнения Infer, как правило, не находит.
