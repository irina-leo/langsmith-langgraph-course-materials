# langsmith-langgraph-course-materials
Educational Colab notebooks and homeworks on LangSmith, LangGraph, LangChain, ReAct agents, tracing, experiments and LLM-as-a-Judge.
# LangSmith / LangGraph Course Materials

Учебно-методический комплект по LangSmith, LangChain и LangGraph: лекционный Google Colab-ноутбук, домашние задания Lite/Pro, полный разбор решений и отдельный LangGraph-агент для демонстрации влияния системных промптов на поведение LLM.

Проект был разработан как практический учебный материал для студентов, изучающих наблюдаемость, трассировку, агентные сценарии и оценку качества LLM-приложений.

## Моя роль

AI Course Materials Developer / Prompt Engineer / Developer of Educational AI Agents.

## Что было разработано

* Спроектирован лекционный Colab-ноутбук по LangSmith и агентным сценариям.
* Подготовлены домашние задания Lite и Pro.
* Разработан полный разбор домашнего задания Pro с кодом, комментариями, анализом запусков и выводами.
* Реализованы учебные примеры LLM-агентов с трассировкой в LangSmith.
* Подготовлены блоки по ReAct-паттерну, инструментам, Runs, Datasets, Experiments и LLM-as-a-Judge.
* Разработан отдельный агент на LangGraph: Psychoanalyst with Three Prompting Styles.
* Показано, как изменение system prompt влияет на стиль, структуру и содержание ответа модели.
* Подготовлена логика сравнения трёх стилей: Humanistic, CBT и Psychoanalytic.
* Продумана архитектура многошагового графа с состоянием, узлами обработки и вспомогательными инструментами.

## LangGraph Agent: Psychoanalyst with Three Prompting Styles

Отдельный учебный агент на LangGraph, разработанный для демонстрации влияния системных промптов на поведение языковой модели и возможностей трассировки в LangSmith.

Агент показывает, как одна и та же LLM может воспроизводить разные стили взаимодействия с пользователем за счёт изменения системной инструкции без изменения модели или основной бизнес-логики.

### Цель агента

Продемонстрировать:

* построение агента на LangGraph;
* использование состояния State;
* организацию многошагового пайплайна;
* трассировку выполнения графа в LangSmith;
* влияние системных промптов на ответы модели;
* анализ и сравнение результатов разных запусков.

### Архитектура агента

Агент реализован в виде графа LangGraph и работает с тремя стилями:

* Humanistic — гуманистический подход;
* CBT — когнитивно-поведенческий подход;
* Psychoanalytic — психоаналитический подход.

Для каждого стиля используется собственный system prompt, который задаёт стратегию ответа модели.

Основные узлы графа:

1. Style Selector
   Выбор активного стиля взаимодействия.

2. Thought Node
   Генерация внутреннего плана ответа.

3. Action Nodes
   Вызов вспомогательных инструментов:

   * psychoeducation_tool;
   * mindfulness_tool;
   * micro_plan_tool.

4. Final Node
   Формирование итогового ответа пользователю.

## LangSmith

В проекте использовались возможности LangSmith:

* Tracing;
* Runs;
* Nested Runs;
* Tags;
* Metadata;
* сравнение запусков;
* анализ промежуточных шагов агента;
* просмотр маршрута прохождения по графу;
* анализ влияния разных system prompts на поведение модели.

Каждый запуск сохраняет полный маршрут работы агента, что позволяет анализировать не только финальный ответ, но и промежуточную логику выполнения.

## Домашние задания

### Lite

Домашнее задание Lite направлено на базовое освоение LangSmith. Студент запускает минимального агента, включает трассировку и проверяет результат работы в интерфейсе LangSmith.

### Pro

Домашнее задание Pro направлено на анализ влияния system prompt на поведение агента. Студент запускает три варианта агента в стилях Humanistic, CBT и Psychoanalytic, сохраняет скриншоты трейсов, сравнивает ответы, изменяет один из промптов и делает вывод о влиянии промпта на структуру и качество ответа.

### Разбор Pro

В полном разборе показаны:

* установка зависимостей;
* настройка ключей и окружения;
* запуск трёх стилей;
* просмотр Runs в LangSmith;
* сравнение ответов;
* модификация CBT-промпта;
* анализ различий между исходным и изменённым вариантом;
* финальный вывод о влиянии system prompt.

## Учебная ценность проекта

Проект демонстрирует полный цикл работы с учебным LLM-агентом:

* создание агента;
* подключение инструментов;
* построение графа состояний;
* трассировка запусков;
* анализ промежуточных шагов;
* сравнение разных промптов;
* автоматическая оценка качества;
* подготовка заданий для студентов;
* разбор типового решения.

Материалы помогают студентам понять, как не просто запускать LLM-агентов, а наблюдать их поведение, анализировать reasoning, сравнивать версии и управлять качеством ответа через prompt engineering и evaluation.

## Технологии

Python, Google Colab, LangSmith, LangGraph, LangChain, OpenAI API, ChatOpenAI, ReAct, State, Tools, Agent Tracing, Runs, Nested Runs, Datasets, Experiments, LLM-as-a-Judge, Prompt Engineering, Evaluation.
Copyright and usage
Copyright (c) 2026 Irina Leonova. All rights reserved.
This repository is published for portfolio and demonstration purposes only.
No part of this project description, architecture, documentation, prompts, schemas, workflows, or related materials may be copied, modified, redistributed, sublicensed, used in commercial products, or represented as someone else's work without prior written permission from the author.
