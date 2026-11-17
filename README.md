# Deep Learning for Computer Vision and NLP

Практичні ноутбуки до курсу магістратури «Deep Learning for Computer Vision and NLP». Кожен ноутбук відповідає
темі конспекту й містить увесь код заняття: завантаження даних, підготовку, навчання та оцінювання моделей.
Теоретичний матеріал і пояснення до коду — у конспектах на навчальній платформі курсу.

Ноутбуки збережено разом із результатами виконання (виводами клітинок і графіками), тому їх можна переглядати
прямо на GitHub без запуску.

## Зміст

- [Швидкий старт](#швидкий-старт)
- [Ноутбуки](#ноутбуки)
- [Що в кожному ноутбуці](#що-в-кожному-ноутбуці)
- [Як запустити](#як-запустити): [Google Colab](#google-colab), [Kaggle](#kaggle), [локально](#локально)
- [Дані](#дані)
- [Середовище](#середовище)
- [Відтворюваність результатів](#відтворюваність-результатів)
- [Типові проблеми](#типові-проблеми)
- [Структура репозиторію](#структура-репозиторію)

## Швидкий старт

1. Знайдіть ноутбук своєї теми в [таблиці](#ноутбуки) й відкрийте його за посиланням **Colab** або **Kaggle**.
2. Якщо в таблиці вказано **GPU**, увімкніть прискорювач: у Colab — *Runtime → Change runtime type → T4 GPU*,
   на Kaggle — *Accelerator → GPU T4 x2*.
3. Виконайте всі клітинки (*Runtime → Run all*). Дані й бібліотеки, яких немає в середовищі, ноутбук завантажить
   і встановить сам.

## Ноутбуки

| Модуль | Тема | Ноутбук | Запуск | Прискорювач і час (орієнтовно) |
|---|---|---|---|---|
| 1 | 2. Нейронна мережа на прикладі логістичної регресії | [`Module_1_Lecture_2_Class`](notebooks/Module_1_Lecture_2_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_1_Lecture_2_Class.ipynb) | CPU, до 1 хв |
| 2 | 3. Поняття тензора. Операції над тензорами | [`Module_2_Lecture_3_Class`](notebooks/Module_2_Lecture_3_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_2_Lecture_3_Class.ipynb) | CPU, до 1 хв |
| 2 | 4. Нейронні мережі для задач багатокласової класифікації та регресії | [`Module_2_Lecture_4_Class`](notebooks/Module_2_Lecture_4_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_2_Lecture_4_Class.ipynb) | CPU, до 1 хв |
| 3 | 5. Згорткові мережі | [`Module_3_Lecture_5_Class`](notebooks/Module_3_Lecture_5_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_3_Lecture_5_Class.ipynb) | GPU, 10–30 хв |
| 3 | 6. Архітектури згорткових мереж. Трансферне навчання | [`Module_3_Lecture_6_Class`](notebooks/Module_3_Lecture_6_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_3_Lecture_6_Class.ipynb) | GPU, кілька хвилин |
| 4 | 7. Детекція об'єктів: огляд архітектур | [`Module_4_Lecture_7_Class_kaggle`](notebooks/Module_4_Lecture_7_Class_kaggle.ipynb) | [Kaggle](https://kaggle.com/kernels/welcome?src=https://github.com/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_4_Lecture_7_Class_kaggle.ipynb) | GPU, кілька годин |
| 4 | 7. Детекція об'єктів: огляд архітектур (той самий код для Colab і локального запуску) | [`Module_4_Lecture_7_Class`](notebooks/Module_4_Lecture_7_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_4_Lecture_7_Class.ipynb) | GPU, кілька годин |
| 4 | 8. Детекція об'єктів: аналіз результатів. Автокодери | [`Module_4_Lecture_8_Class`](notebooks/Module_4_Lecture_8_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_4_Lecture_8_Class.ipynb) | GPU, кілька хвилин |
| 5 | 9. Підготовка даних в обробці природної мови | [`Module_5_Lecture_9_Class`](notebooks/Module_5_Lecture_9_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_5_Lecture_9_Class.ipynb) | CPU, кілька хвилин |
| 5 | 10. Word embeddings | [`Module_5_Lecture_10_Class`](notebooks/Module_5_Lecture_10_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_5_Lecture_10_Class.ipynb) | CPU, 10–30 хв і завантаження векторів (≈3,6 ГБ) |
| 6 | 11. RNN, LSTM, GRU | [`Module_6_Lecture_11_Class`](notebooks/Module_6_Lecture_11_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_6_Lecture_11_Class.ipynb) | GPU, кілька хвилин |
| 6 | 12. Sequence to Sequence. Механізм уваги | [`Module_6_Lecture_12_Class`](notebooks/Module_6_Lecture_12_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_6_Lecture_12_Class.ipynb) | GPU, 10–30 хв |
| 7 | 13. Трансформери: відповіді на запитання (BERT) | [`Module_7_Lecture_13_Class_kaggle`](notebooks/Module_7_Lecture_13_Class_kaggle.ipynb) | [Kaggle](https://kaggle.com/kernels/welcome?src=https://github.com/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_7_Lecture_13_Class_kaggle.ipynb) | GPU, кілька годин |
| 7 | 13. Трансформери: сумаризація (T5) | [`Module_7_Lecture_13_Class_summarization_kaggle`](notebooks/Module_7_Lecture_13_Class_summarization_kaggle.ipynb) | [Kaggle](https://kaggle.com/kernels/welcome?src=https://github.com/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_7_Lecture_13_Class_summarization_kaggle.ipynb) | GPU, близько години |
| 7 | 14. Методи оптимізації. Підбір гіперпараметрів | [`Module_7_Lecture_14_Class`](notebooks/Module_7_Lecture_14_Class.ipynb) | [Colab](https://colab.research.google.com/github/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP/blob/main/notebooks/Module_7_Lecture_14_Class.ipynb) | CPU, 1–2 години |

Тема 1 («Вступ до глибокого навчання») теоретична й окремого ноутбука не має. Результати навчання YOLO, які
аналізуються в Темі 8, отримують у ноутбуці Теми 7.

Час наведено для безкоштовних GPU T4 у Colab і Kaggle; на потужнішому GPU ноутбуки виконуються в кілька разів
швидше. Ноутбуки з позначкою CPU прискорювача не потребують.

## Що в кожному ноутбуці

Нижче коротко описано, що робить кожен ноутбук і які результати в ньому отримано. Числа взято зі збережених
виводів; у вашому запуску вони можуть трохи відрізнятися (див.
[Відтворюваність результатів](#відтворюваність-результатів)).

### Модуль 1

**Тема 2 — [`Module_1_Lecture_2_Class`](notebooks/Module_1_Lecture_2_Class.ipynb).** Логістична регресія як
найпростіша нейронна мережа, реалізована з нуля на NumPy: розвідувальний аналіз і підготовка даних Spaceship
Titanic, ініціалізація параметрів, пряме поширення, бінарна крос-ентропія, градієнтний спуск і передбачення.
Результат: точність ≈ 78 % на тренувальній і ≈ 79 % на тестовій вибірці.

### Модуль 2

**Тема 3 — [`Module_2_Lecture_3_Class`](notebooks/Module_2_Lecture_3_Class.ipynb).** Тензори PyTorch: створення
й ініціалізація, типи даних, арифметичні операції, broadcasting, зміна форми, перенесення обчислень на GPU. Друга
частина — логістична регресія на PyTorch для даних Spaceship Titanic: модель на основі `nn.Module`, функція
втрат, оптимізатор і цикл навчання. Результат: точність ≈ 0,78.

**Тема 4 — [`Module_2_Lecture_4_Class`](notebooks/Module_2_Lecture_4_Class.ipynb).** Повнозв'язні нейронні
мережі для двох задач: багатокласова класифікація виду пінгвіна (3 класи, `CrossEntropyLoss`) і регресія продажів
BigMart (`MSELoss`). Підготовка ознак, власні `Dataset` і `DataLoader`, цикли навчання й оцінювання, графіки
функції втрат і метрик. Результат: класифікація — ≈ 96 % на тренувальній і 87–95 % на тестовій вибірці (залежно
від запуску); регресія — RMSE ≈ 1100.

### Модуль 3

**Тема 5 — [`Module_3_Lecture_5_Class`](notebooks/Module_3_Lecture_5_Class.ipynb).** Згорткові нейронні мережі
для класифікації фотографій жестів SIGNS (числа від 0 до 5): згортки, падінг, пулінг, аугментації (зокрема
Random Blocks), batch normalization, оптимізатор Adam, навчання 15 епох на GPU. Результат: збалансована точність
на тестовій вибірці ≈ 0,9.

**Тема 6 — [`Module_3_Lecture_6_Class`](notebooks/Module_3_Lecture_6_Class.ipynb).** Трансферне навчання на
прикладі ResNet18, попередньо навченої на ImageNet: донавчання всієї моделі й навчання лише нового
класифікаційного шару на зображеннях мурах і бджіл (hymenoptera), візуалізація передбачень. Результат: точність
на валідації ≈ 0,93 і ≈ 0,95 відповідно.

### Модуль 4

**Тема 7 — [`Module_4_Lecture_7_Class_kaggle`](notebooks/Module_4_Lecture_7_Class_kaggle.ipynb) і
[`Module_4_Lecture_7_Class`](notebooks/Module_4_Lecture_7_Class.ipynb).** Детекція об'єктів за допомогою YOLO
(бібліотека Ultralytics) на датасеті Construction Site Safety з 10 класами (каски, маски, захисні жилети, люди,
конуси, техніка тощо): підготовка `data.yaml`, огляд і статистика датасету, інференс попередньо навченої моделі,
навчання YOLOv9e (70 епох), валідація, криві метрик, матриця помилок і експорт моделі. Результат: precision
≈ 0,95, recall ≈ 0,81, mAP50 ≈ 0,87, mAP50-95 ≈ 0,62. Обидва ноутбуки містять однаковий код: версію `_kaggle`
зручно запускати на Kaggle у фоновому режимі, другу — у Colab або локально. Для швидкої перевірки встановіть
`DEBUG = True` у класі `CFG`: тоді модель навчається 3 епохи на 5 % даних.

**Тема 8 — [`Module_4_Lecture_8_Class`](notebooks/Module_4_Lecture_8_Class.ipynb).** Згортковий автокодер для
Fashion-MNIST: кодувальник (`Conv2d`) і декодувальник (`ConvTranspose2d`), навчання на відновлення зображень,
порівняння оригіналів і відновлених зображень, генерація нових зображень із випадкових точок латентного простору.
Результат: функція втрат на валідаційній і тестовій вибірках ≈ 0,019. Аналіз результатів навчання YOLO, який теж
входить до Теми 8, виконується в ноутбуці Теми 7.

### Модуль 5

**Тема 9 — [`Module_5_Lecture_9_Class`](notebooks/Module_5_Lecture_9_Class.ipynb).** Підготовка тексту на
відгуках Amazon: нормалізація, стоп-слова, стемінг, мішок слів (Bag of Words) і TF-IDF з уні- та біграмами,
класифікація тональності логістичною регресією, оцінювання за ROC-AUC. Результат: ROC-AUC 0,86–0,92 залежно від
способу представлення тексту.

**Тема 10 — [`Module_5_Lecture_10_Class`](notebooks/Module_5_Lecture_10_Class.ipynb).** Векторні представлення
слів: навчання Word2Vec з нуля (gensim), попередньо навчені GloVe і Word2Vec Google News, пошук схожих слів за
косинусною подібністю, візуалізація t-SNE, класифікація відгуків за усередненими векторами слів і за Doc2Vec.
Результат: найближче до «cat» у GloVe — «dog» (0,92); ROC-AUC ≈ 0,89 для Word2Vec і ≈ 0,88 для Doc2Vec.

### Модуль 6

**Тема 11 — [`Module_6_Lecture_11_Class`](notebooks/Module_6_Lecture_11_Class.ipynb).** Розпізнавання
іменованих сутностей (NER) на CoNLL-2003 за допомогою тришарової двонаправленої LSTM (BiLSTM): словник і
кодування міток, навчання з ранньою зупинкою, збереження найкращої моделі, оцінювання за macro F1 і
classification report. Результат: macro F1 на тестовій вибірці ≈ 0,74.

**Тема 12 — [`Module_6_Lecture_12_Class`](notebooks/Module_6_Lecture_12_Class.ipynb).** Модель Sequence to
Sequence з механізмом уваги (кодувальник і декодувальник на GRU) для перекладу з німецької на англійську
(Multi30k): токенізація spaCy, побудова словників, навчання, оцінювання за функцією втрат і perplexity, переклад
речень і візуалізація ваг уваги. Результат: test loss ≈ 3,29 (perplexity ≈ 27).

### Модуль 7

**Тема 13, відповіді на запитання —
[`Module_7_Lecture_13_Class_kaggle`](notebooks/Module_7_Lecture_13_Class_kaggle.ipynb).** Екстрактивні
відповіді на запитання: донавчання BERT (`google-bert/bert-base-cased`) на SQuAD — токенізація довгих контекстів
вікнами з перекриттям, пошук початку й кінця відповіді, оцінювання за Exact Match і F1. Наприкінці донавчена
модель відповідає на запитання з валідаційної вибірки та до власного тексту. Результат за 3 епохи: EM ≈ 80, F1 ≈ 88.

**Тема 13, сумаризація —
[`Module_7_Lecture_13_Class_summarization_kaggle`](notebooks/Module_7_Lecture_13_Class_summarization_kaggle.ipynb).**
Абстрактивна сумаризація відгуків: донавчання T5 (`google-t5/t5-small`) на 2 % датасету Review Summarizer,
оцінювання за ROUGE, приклади підсумків, згенерованих донавченою моделлю. Результат: ROUGE-1 ≈ 21 після 10 епох.

**Тема 14 — [`Module_7_Lecture_14_Class`](notebooks/Module_7_Lecture_14_Class.ipynb).** Регуляризація й
оптимізація навчання на MNIST: L2-регуляризація (weight decay), dropout, batch normalization, рання зупинка,
підбір гіперпараметрів за допомогою Optuna (100 спроб) з аналізом важливості параметрів. Результат: точність на
валідаційній вибірці ≈ 0,98.

## Як запустити

### Google Colab

1. Відкрийте ноутбук за посиланням **Colab** у таблиці або кнопкою *Open in Colab* на початку ноутбука.
   Щоб зберегти власні зміни, створіть копію: *File → Save a copy in Drive*.
2. Для ноутбуків з позначкою **GPU** увімкніть прискорювач: *Runtime → Change runtime type → T4 GPU*. Робіть це
   до запуску клітинок, бо зміна типу середовища перезапускає сесію.
3. Виконайте клітинки по черзі (*Shift+Enter*) або всі одразу (*Runtime → Run all*).

Що варто знати про Colab:

- Пакети, яких немає в Colab (`gensim`, `ultralytics`, `optuna`, `evaluate`, `rouge_score`, модель spaCy
  `de_core_news_sm`), встановлюються першими клітинками відповідних ноутбуків. Вони лише додають нові пакети й не
  змінюють уже встановлених, тому перезапускати сесію після встановлення не потрібно.
- Завантажені дані й навчені моделі зберігаються лише до кінця сесії. Після перепідключення ноутбук завантажить
  дані знову.
- Безкоштовні сесії Colab обмежені в часі й завершуються після тривалої бездіяльності. Довге навчання (Теми 7 і 13)
  зручніше запускати на Kaggle.

### Kaggle

Ноутбуки із суфіксом `_kaggle` розраховані на тривале навчання, тому їх зручно запускати на Kaggle.

1. Увійдіть в обліковий запис Kaggle. Щоб увімкнути GPU й доступ до інтернету, підтвердьте обліковий запис
   номером телефону (у налаштуваннях облікового запису).
2. Відкрийте ноутбук за посиланням **Kaggle** у таблиці або кнопкою *Open in Kaggle* на початку ноутбука.
3. У панелі налаштувань ноутбука оберіть *Accelerator → GPU T4 x2* і переконайтеся, що *Internet* увімкнено:
   ноутбуки завантажують дані й моделі з інтернету.
4. Натисніть *Save Version → Save & Run All (Commit)*. Ноутбук виконається у фоновому режимі (до 12 годин), а
   виводи збережуться у версії ноутбука; вкладку браузера можна закрити.

GPU P100 поточна збірка PyTorch не підтримує (CUDA 13 потребує GPU з compute capability 7.5 і вище), тому
обирайте T4. Безкоштовний час GPU на Kaggle обмежений щотижневою квотою, тож перед повним навчанням YOLO варто
перевірити код у режимі `DEBUG = True`.

### Локально

Знадобляться Python 3.13 і Jupyter; для ноутбуків з позначкою GPU — відеокарта NVIDIA з підтримкою CUDA.

```bash
git clone https://github.com/BetterED-Neoversity/DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP.git
cd DEEP-LEARNING-FOR-COMPUTER-VISION-AND-NLP

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

pip install jupyter ipywidgets numpy pandas matplotlib seaborn plotly scikit-learn tqdm \
    pillow opencv-python pyyaml torch torchvision transformers datasets evaluate rouge_score \
    sentencepiece nltk spacy gensim ultralytics optuna kagglehub gdown

jupyter notebook notebooks/
```

Версію PyTorch з підтримкою GPU встановлюйте за інструкцією на [pytorch.org](https://pytorch.org/get-started/locally/).
Моделі spaCy і дані NLTK ноутбуки завантажують самі.

Ноутбуки зберігають завантажені дані в теку `data/` поруч із собою (у Colab — `/content/data`), вектори Теми 10 —
у `pretrained_models/`, а моделі й датасети Hugging Face — у стандартний кеш `~/.cache/huggingface`. Повний список
тек, які створюють ноутбуки, наведено в розділі [Структура репозиторію](#структура-репозиторію).

## Дані

| Ноутбук | Дані | Джерело |
|---|---|---|
| `Module_1_Lecture_2_Class`, `Module_2_Lecture_3_Class` | Spaceship Titanic | [`data/`](data/) цього репозиторію |
| `Module_2_Lecture_4_Class` | Palmer Penguins, BigMart Sales | [`data/`](data/) цього репозиторію |
| `Module_3_Lecture_5_Class` | SIGNS — фото жестів рук (архів ≈1,1 ГБ) | Google Drive (через `gdown`) |
| `Module_3_Lecture_6_Class` | Hymenoptera — мурахи й бджоли | download.pytorch.org |
| `Module_4_Lecture_7_Class*` | Construction Site Safety; ваги YOLOv9e | Kaggle (через `kagglehub`); Ultralytics |
| `Module_4_Lecture_8_Class` | Fashion-MNIST | torchvision |
| `Module_5_Lecture_9_Class`, `Module_5_Lecture_10_Class` | Amazon Product Reviews | Kaggle (через `kagglehub`) |
| `Module_5_Lecture_10_Class` | GloVe 6B 50d, Word2Vec Google News 300 (≈3,6 ГБ); за бажанням — fastText wiki-news | Kaggle (через `kagglehub`) |
| `Module_6_Lecture_11_Class` | CoNLL-2003 | Kaggle (через `kagglehub`) |
| `Module_6_Lecture_12_Class` | Multi30k (німецька → англійська); моделі spaCy `de_core_news_sm`, `en_core_web_sm` | Hugging Face Hub; spaCy |
| `Module_7_Lecture_13_Class_kaggle` | SQuAD; модель `google-bert/bert-base-cased` | Hugging Face Hub |
| `Module_7_Lecture_13_Class_summarization_kaggle` | Review Summarizer; модель `google-t5/t5-small` | Hugging Face Hub |
| `Module_7_Lecture_14_Class` | MNIST | torchvision |

Усі дані ноутбуки завантажують самі під час першого запуску; повторно вони використовують уже завантажені файли.
Для публічних датасетів Kaggle обліковий запис не потрібен: `kagglehub` завантажує їх анонімно. Моделі й
датасети Hugging Face теж завантажуються без токена.

## Середовище

Ноутбуки розраховані на поточні середовища Google Colab і Kaggle та перевірені з такими версіями:

| Пакет | Версія |
|---|---|
| Python | 3.13 |
| PyTorch / torchvision | 2.14 / 0.29 |
| transformers / datasets | 5.22 / 4.8 |
| scikit-learn | 1.6 |
| pandas / NumPy | 2.2 / 2.4 |
| spaCy / NLTK | 3.8 / 3.9 |
| ultralytics / gensim / optuna / evaluate | 8.4 / 4.4 / 5.1 / 0.4 |

Ноутбуки модулів 1–2 і 5 також працюють із новішими pandas 3.x і scikit-learn 1.9. Образ Kaggle збирається на
основі образу Colab, тому набір бібліотек там майже такий самий, але версії можуть відставати на кілька тижнів.

## Відтворюваність результатів

Більшість ноутбуків навчає моделі з випадковими початковими вагами й випадковим порядком даних, а на GPU ще й різні
відеокарти виконують обчислення з трохи різним округленням. Тому числа у вашому запуску можуть дещо відрізнятися від
збережених у ноутбуках і наведених у конспектах, і це нормально. Орієнтуйтеся на порядок значень і загальну динаміку
навчання: функція втрат спадає, метрики зростають, висновки збігаються.

- **Ті самі числа при кожному запуску** дають Теми 2, 3 і 9: там фіксоване розбиття даних і детерміновані моделі.
- **Помітний розкид** буває там, де тестова вибірка невелика: наприклад, у Темі 4 точність на тестовій вибірці в
  різних запусках становила від 87 до 95 %, а в Темі 5 одне зображення з 120 тестових змінює точність майже на
  1 відсотковий пункт.
- **Word2Vec і Doc2Vec** (Тема 10) навчаються в кілька потоків, тому списки схожих слів для моделі, навченої з
  нуля, щоразу трохи інші; ROC-AUC Doc2Vec у різних запусках — 0,876–0,883. Результати попередньо навчених векторів
  від запуску не залежать.
- **Optuna** (Тема 14) щоразу перебирає інші комбінації гіперпараметрів, тож найкраща спроба буде іншою.
- **YOLO** (Тема 7) використовує фіксований seed, але результат залежить і від відеокарти, і від версії
  `ultralytics`, яку ноутбук встановлює.

## Типові проблеми

| Симптом | Причина й розв'язання |
|---|---|
| `torch.cuda.is_available()` повертає `False`, навчання дуже повільне | Прискорювач не увімкнено. Colab: *Runtime → Change runtime type → T4 GPU*; Kaggle: *Accelerator → GPU T4 x2*. |
| На Kaggle: `CUDA error: no kernel image is available for execution on the device` | Обрано GPU P100, яку поточна збірка PyTorch не підтримує. Оберіть GPU T4 x2. |
| На Kaggle не вдається увімкнути GPU або *Internet* | Обліковий запис не підтверджено номером телефону. |
| Ядро завершує роботу через нестачу пам'яті в `Module_5_Lecture_10_Class` | Вектори Google News займають кілька гігабайтів оперативної пам'яті. У ноутбуці позначено місце, де варто перезапустити ядро й повторно виконати клітинки до вказаної частини. |
| `gdown` не може завантажити SIGNS у `Module_3_Lecture_5_Class` | Google Drive тимчасово обмежує кількість завантажень файлу. Спробуйте пізніше або завантажте архів вручну за посиланням над клітинкою завантаження й розпакуйте теки `train_signs` і `test_signs` у `data/Module_3_Lecture_1_SIGNS_dataset/`. |
| `CUDA out of memory` | Перезапустіть ядро, щоб звільнити відеопам'ять. Якщо не допомагає, зменшіть розмір батча (для YOLO — `BATCH_SIZE` у класі `CFG`). |
| Локально на Windows або macOS: `AttributeError: Can't get attribute ... on <module '__main__'>` під час ітерації `DataLoader` | Клас `Dataset`, оголошений у ноутбуці, не передається в процеси-воркери. Встановіть `num_workers=0` у відповідному `DataLoader`. |
| Попередження про `HF_TOKEN` | Його можна ігнорувати: моделі й датасети Hugging Face завантажуються й без токена, а токен лише пришвидшує завантаження. |

Якщо ноутбук не виконується з іншої причини, повідомте викладача або ментора курсу: назву ноутбука, клітинку, повний
текст помилки, середовище (Colab, Kaggle чи локально) і обраний прискорювач.

## Структура репозиторію

```
.
├── data/                                          # CSV-файли для ноутбуків модулів 1–2
│   ├── Module_1_Lecture_2_Class_Spaceship_Titanic.csv
│   ├── Module_2_Lecture_2_Class_bigmart_data.csv
│   └── Module_2_Lecture_2_Class_penguins.csv
├── notebooks/                                     # ноутбуки занять: Module_<модуль>_Lecture_<тема>_Class*.ipynb
└── README.md
```

Під час виконання ноутбуки створюють поруч із собою (у Colab — у `/content`):

| Шлях | Ноутбук | Вміст |
|---|---|---|
| `data/` | більшість ноутбуків | завантажені датасети |
| `pretrained_models/`, `saved_models/` | `Module_5_Lecture_10_Class` | попередньо навчені вектори й власна модель Word2Vec |
| `runs/detect/` | `Module_4_Lecture_7_Class*` | ваги, графіки й метрики навчання YOLO |
| `bilstmtagger.pt` | `Module_6_Lecture_11_Class` | найкращі ваги моделі BiLSTM |
| `saved_models/` | `Module_6_Lecture_12_Class` | найкращі ваги моделі Seq2Seq |
| `bert-finetuned-squad/` | `Module_7_Lecture_13_Class_kaggle` | донавчена модель BERT і токенізатор |
| `results-t5-finetuned/` | `Module_7_Lecture_13_Class_summarization_kaggle` | донавчена модель T5 і токенізатор |
