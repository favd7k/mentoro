# ❓ Mentoro - Часто Задаваемые Вопросы (FAQ)

## 💰 Финансовые вопросы

### Q1: Сколько денег вы просите?
**A:** Мы ищем **Seed раунд $50K**
- $30K на разработку MVP (улучшение текущей версии)
- $15K на маркетинг и user acquisition
- $5K на операционные расходы (хостинг, инструменты, etc)

**Почему $50K достаточно?**
- MVP уже в 80% готовности
- Команда может работать lean (малобюджетно)
- Используем free/cheap инструменты (Vercel, Supabase free tier)
- Первых 10K пользователей можно получить органически (referrals)

### Q2: Какой потенциальный ROI?
**A:** Консервативно - 10-15x за 3 года

```
Инвестиция: $50K
Year 1 Revenue: $80K (freemium + B2B)
Year 2 Revenue: $750K
Year 3 Revenue: $5M

Profit margin: 40-50%
Break-even: Month 18-24
Profitable: Year 3+

Total Return by Year 3:
- Revenue: $6.5M+
- Profit: ~$2-3M
- ROI on $50K: 40-60x
```

### Q3: Как вы планируете монетизировать?
**A:** Три потока доходов:

1. **Freemium (50% доход)**
   - Бесплатный план: базовый доступ
   - Premium: $5-10/месяц
   - Conversion rate: 10-15% (типично для edtech)

2. **B2B Университеты (40% доход)**
   - Лицензия для университета: $1-10K/год
   - Scalable: +50 университетов = $250K+

3. **Enterprise (10% доход)**
   - Белый лейбл и кастомные интеграции
   - Растущий доход в Year 2-3

### Q4: Какова ваша gross margin?
**A:** Очень высокая для SaaS

```
Revenue: $1M
Cost of Goods Sold:
- Cloud hosting (Vercel): $5K/год
- Database (Supabase): $10K/год
- AI API (OpenAI): $20K/год
- Email/SMS: $2K/год
Total COGS: $37K

Gross Margin: ($1M - $37K) / $1M = 96%

(Типично для SaaS: 80-90%)
```

### Q5: Когда вы выйдите на break-even?
**A:** Месяц 18-24

```
Costs:
- Salaries (3 engineers, 1 designer): $20K/месяц
- Infrastructure: $1K/месяц
- Marketing: $2K/месяц
Total Monthly: $23K

Break-even Revenue: $23K/месяц × 40% = $57.5K/месяц

Timeline:
Month 1-6: 0% → 5% revenue
Month 7-12: 5% → 30% revenue
Month 13-18: 30% → 70% revenue
Month 19-24: 70% → 100%+ revenue (profitable!)
```

---

## 🎯 Рыночные вопросы

### Q6: Размер рынка?
**A:** ОЧЕНЬ БОЛЬШОЙ

```
TAM (Total Addressable Market):
- Студенты университетов: 1M в Казахстане
- Школьники: 500K
- Lifelong learners: 2M
- Total TAM: 3.5M+ × $100/год = $350M+ в регионе

SAM (Serviceable Addressable Market):
- Казахстан: 300K студентов × $30/год = $10M
- Центральная Азия: 1M студентов × $30 = $30M
- Total SAM: $40M

SOM (Serviceable Obtainable Market):
- Year 3 target: 50K paying users × $50/год = $2.5M
- Year 5 target: 500K paying users = $25M
```

### Q7: Кто ваши конкуренты?
**A:** Нет прямых конкурентов, но есть альтернативы:

```
ChatGPT:
- Плюсы: Мощный AI
- Минусы: Не специализирован для образования, нет интеграций
- Mentoro: +50% лучше для студентов благодаря контексту

Quizlet:
- Плюсы: Популярен, большое сообщество
- Минусы: Ручное создание контента, нет AI помощника
- Mentoro: +70% лучше благодаря auto-generation

Google Classroom:
- Плюсы: Интегрирован с Google, много школ используют
- Минусы: Требует учителя, нет AI помощника
- Mentoro: +40% лучше для самостоятельного обучения

Наше преимущество: Единственная платформа, которая комбинирует все четыре!
```

### Q8: Не ли это слишком насыщено (crowded)?
**A:** Нет, потому что:

1. **Категория новая** - AI для образования только начинается (2024)
2. **Первый в регионе** - Mentoro будет first-mover advantage в Казахстане
3. **Локальное преимущество** - Меньше конкуренции от глобальных игроков в казахстане
4. **Network effect** - Чем больше студентов, тем больше ценность для преподавателей

```
Winner-takes-most рынки (как Uber, Airbnb):
- 1st player: 40% рынка
- 2nd player: 30% рынка
- Others: 30% рынка

Mentoro может быть первым в регионе → 40% вероятность!
```

---

## 🔧 Технические вопросы

### Q9: Почему Next.js а не другой фреймворк?
**A:** Next.js идеален для Mentoro:

```
Требования Mentoro:
- Полнофункциональное веб-приложение ✓ (React)
- API endpoints ✓ (Built-in)
- Быстрая загрузка ✓ (SSR/SSG)
- Легко масштабировать ✓ (Serverless)
- Одна команда (JS/TS везде) ✓

Альтернативы:
- Django: Мощно, но Python нужна отдельная команда
- Vue.js: Хорошо, но нет встроенных API routes
- Flutter: Хорошо для мобильного, но это web сначала

Next.js победил. Используют все стартапы (Vercel сам это создал).
```

### Q10: Что с масштабируемостью?
**A:** Архитектура масштабируется на миллионы пользователей:

```
Текущее (MVP): 100-1000 пользователей
- Next.js на localhost
- In-memory database
- Good enough for testing

Stage 1 (10K пользователей):
- Vercel serverless (automatic scaling)
- Supabase PostgreSQL
- Redis for caching
- S3 for files
Cost: ~$200/месяц

Stage 2 (100K пользователей):
- Same architecture (Vercel scales)
- Database read replicas
- Advanced caching
- CDN optimization
Cost: ~$2K/месяц

Stage 3 (1M+ пользователей):
- Multi-region deployment
- Database sharding
- Custom infrastructure
- Enterprise support
Cost: ~$20K/месяц
```

### Q11: Как вы обработаете миллионы документов (PDF)?
**A:** Правильная архитектура:

```
Текущее: Локальный PDF parsing
↓
Stage 1: Background workers
- User загружает PDF
- System добавляет в очередь
- Workers обрабатывают асинхронно
- Результаты сохраняются в S3

Stage 2: Векторные базы данных
- Каждый PDF конвертируется в embeddings
- Хранятся в vector DB (Pinecone/Milvus)
- Супер быстрый search (что релевантно для студента)

Результат: Может обрабатывать 1000s PDFs в день, с <100ms поиском
```

---

## 📊 Метрики и аналитика

### Q12: Какие KPI вы будете отслеживать?
**A:** Главные метрики для Mentoro:

```
User Metrics:
- DAU (Daily Active Users) - цель: 40%+ от MAU
- MAU (Monthly Active Users) - цель: 10K к концу года
- Churn rate - цель: <5% в месяц
- Retention (30-day) - цель: >50%

Engagement Metrics:
- Avg quiz per user per week - цель: 2+
- Avg AI chat per user per week - цель: 3+
- Time on platform - цель: 45 мин/день
- Completion rate - цель: 70%+ для начатых квизов

Financial Metrics:
- CAC (Customer Acquisition Cost) - цель: <$5
- LTV (Lifetime Value) - цель: >$100
- CAC Payback - цель: <6 месяцев
- Monthly Recurring Revenue (MRR) - цель: $5K к концу года

Quality Metrics:
- NPS (Net Promoter Score) - цель: >50
- User satisfaction - цель: 4.5/5 звезд
- Bug reports - цель: <1 per 1000 DAU
```

### Q13: Как вы будете расти с ограниченным бюджетом?
**A:** Growth hacking стратегия:

```
Q1 (Beta Launch):
- Замкнутая бета с 100 AITU студентами
- Собрать feedback и кейсы
- Cost: $5K (маркетинг)

Q2 (Viral Growth):
- Referral программа: "Пригласи друга, получи premium месяц"
- Organic: Социальные медиа, YouTube демо
- Press: Статьи о AI в образовании
- Cost: $10K (paid social для начального толчка)

Q3 (B2B Sales):
- Pitch другие университеты
- Partnerships с образовательными платформами
- Cost: $0 (founder talking to customers)

Q4 (Viral Loop):
- Каждый студент может создать курс
- Каждый может делиться квизами
- Социальные функции для обучения в группе
- Cost: $5K (development)

Результат: 10K пользователей с $20K маркетинг бюджета = 2x стандартный CAC
```

---

## 👥 Командные вопросы

### Q14: Кто будет это делать?
**A:** Мы уже начали, нужна команда для масштабирования:

```
Текущее (MVP этап):
- 1 Full-stack developer (ты)
- Работал 2 месяца

Нужно для Scale:
+ 2 еще Full-stack developers
+ 1 UI/UX designer
+ 1 DevOps engineer (part-time)

Зарплаты (казахстан):
- Senior Full-stack: $1500/месяц × 3 = $4500
- Designer: $1000/месяц = $1000
- DevOps: $500/месяц (part-time) = $500
Total: $6000/месяц

Инвестиция $30K = 5 месяцев полной команды → production-ready приложение
```

### Q15: Как вы наймете лучших людей на ограниченный бюджет?
**A:** Стартап компенсация:

```
Базовая зарплата: 60% от market rate
+ Equity: 0.5-1% за разработчиков
+ Бонус: 20% доход участвуют в команде

Пример:
- Senior dev: $1500 базовая + 0.5% equity + бонусы
- vs full market rate $2500

Привлечение:
- Equity может быть стоит $50K+ (если успешно)
- Миссия: "Революция в образовании"
- Culture: Startup энергия и автономность

Результат: Можно получить талант за 60% от рыночной ставки
```

---

## 🔐 Безопасность и соответствие

### Q16: Что с приватностью студентов и данные?
**A:** Серьезно относимся к безопасности:

```
Соответствие:
- GDPR (Европа) - compliance готово
- CCPA (США) - compliance готово
- КЗ Data Protection Law - compliance планируется

Безопасность:
- JWT tokens для аутентификации
- Bcrypt для пароля хеширования
- HTTPS везде
- Database encryption
- Regular security audits (планируется)

Данные студентов:
- Только то, что необходимо (минимизм)
- Никаких продаж третьим сторонам
- Удаление данных на запрос
- GDPR "right to be forgotten" поддержка

Доверие:
- Прозрачная privacy policy
- Security whitepaper
- Bug bounty программа (планируется)
```

### Q17: Что если AI дает неправильные ответы?
**A:** Это реальный риск, мы управляем это:

```
Меры:
1. Review механизм
   - Преподаватели проверяют AI ответы
   - Флаг неправильных
   - Training улучшает

2. Confidence scoring
   - AI говорит "I'm 85% confident"
   - Низкая confidence → человек должен проверить

3. Human in the loop
   - Сложные вопросы → реальные эксперты
   - Кураторская проверка контента

4. Честность
   - Четко сказать: "Это AI, может ошибиться"
   - Лучше быть честным, чем уверенным неправильно

5. Постоянная улучшение
   - Собирать feedback от пользователей
   - Fine-tune модель на качественных ответах
   - Версионирование и откаты

Результат: Не 100% совершенно, но достаточно хорошо для помощи
```

---

## 🌍 Глобальная экспансия

### Q18: Почему начать с Казахстана?
**A:** Стратегический выбор:

```
Преимущества Казахстана:
✓ Относительно маленький рынок для learn & perfect
✓ Tech-savvy молодежь (особенно в городах)
✓ AITU уже заинтересован (мы в контакте)
✓ English + Local language (Kazakh/Russian)
✓ Lower user acquisition cost
✓ Близко к основателям

Альтернативы:
- Индия: Огромный рынок, но очень конкурентно
- США: Много компетиции, высокие CAC
- Европа: Зрелый рынок, сложно входить

Стратегия:
1. Доминировать в Казахстане (Year 1)
2. Расширить на Центральную Азию (Year 2)
3. Русскоязычный рынок (Year 3)
4. Глобальное расширение (Year 4+)
```

### Q19: Будут ли вы конкурировать с OpenAI, Google, и т.д.?
**A:** Нет, мы будем партнерами:

```
Текущее:
- Используем их AI (LM Studio + OpenAI API)
- Мы не строим собственную модель

Будущее:
- Остаемся на их плечах
- Специализируемся на education layer
- Они строят общие модели, мы специализируем

Аналогия:
- Apple не конкурирует с Samsung (chips)
- Apple использует лучшие чипы для лучших экосистем
- Результат: Apple стоит больше

Mentoro:
- Используем лучшие AI модели
- Специализируем на education
- Результат: Лучше для студентов
```

---

## 📱 Мобильное приложение

### Q20: Когда будет мобильное приложение?
**A:** Фаза 2, не MVP

```
Year 1: Web только (fokus)
Year 2: Mobile Web (responsive - уже есть)
Year 3: React Native приложение (iOS + Android)

Почему сначала web?
- Быстрее разработать
- Не нужны app store approvals
- Desktop + мобильный браузер достаточно для большинства
- Меньше затрат

Mobile later:
- Push notifications улучшат engagement
- Better offline support
- More immersive experience
```

---

## 🎯 Заключение

**Главные выводы:**
1. **Большой рынок** - $350M+ TAM
2. **Реальная потребность** - Студенты реально нуждаются
3. **Простая монетизация** - Freemium + B2B
4. **Светлое будущее** - Break-even в Year 2, прибыль в Year 3
5. **Управляемые риски** - Известные решения для известных проблем

**Инвестируйте в Mentoro - инвестируйте в будущее образования.**

---

*FAQ подготовлен для инвесторов и потенциальных партнеров*
