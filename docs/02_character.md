# Персонаж и мир

## Monolith

| | |
|-|-|
| **Кто** | Бетонный блок, антрацитово-серый, размером примерно с собаку. Большие выразительные глаза, густые «бетонные» брови, тонкие чёрные ручки и ножки. Оранжевая строительная каска, слегка поцарапанная |
| **Характер** | Перфекционист-ворчун. Физически не переносит кривые швы. Ленивый до 7:00 и после 16:00, но в рабочее время одержим идеальностью. Добрый внутри |
| **Голос** | Не говорит. Ворчит, бурчит, вздыхает, издаёт «хмпф». Тяжёлые шаги — «тук-тук» |
| **Фирменный жест** | Достаёт строительный уровень и проверяет всё подряд |
| **Слабость** | Кривая плитка → падает в обморок / начинает трястись |

## Напарник (с эпизода 3): Kachel

Маленькая белая квадратная плитка с глазами-точками. Восторженный стажёр, всё делает не так. Простая форма — тоже держится стабильно.

## Мир

Мультяшная стройка в стиле 3D-анимации: тёплый утренний свет, фургон, леса, мешки с клеем, ванная в процессе ремонта. **Никаких реальных брендов и логотипов** на мешках, фургоне, инструментах.

## Визуальный стиль (вставлять в каждый промпт)

```
STYLE: high-quality 3D animated short film style, soft global illumination, warm cinematic lighting,
slightly exaggerated cartoon proportions, clean shapes, rich textures (rough concrete, glossy ceramic),
shallow depth of field, vertical 9:16 frame. No text, no logos, no watermarks.
```

```
CHARACTER: Monolith — a small anthracite-grey concrete block character (cinder-block shape, rough porous texture),
big expressive cartoon eyes, thick concrete eyebrows, thin black stick arms and legs, wearing a scratched
bright orange construction hard hat. Grumpy but lovable expression.
```

Эти два блока — **«конституция» сериала**. Не перефразировать, вставлять копипастом. Любое изменение формулировки = персонаж начнёт плыть.

## Шаг 1. Лист персонажа (ChatGPT, делается один раз)

**Промпт 1 — поиск образа** (сгенерировать 4–6 вариантов, выбрать один):
```
Character design for an animated short series. [CHARACTER]. [STYLE].
Full body, neutral pose, plain light grey background.
```

**Промпт 2 — turnaround** (с выбранной картинкой как референсом):
```
Using this exact character, create a character turnaround sheet: front view, 3/4 view, side view, back view,
same scale, same lighting, plain light grey background. Keep every detail identical.
```

**Промпт 3 — эмоции:**
```
Using this exact character, create an expression sheet with 6 poses: grumpy, shocked, fainting,
proud, sleepy, furious. Plain light grey background. Keep the design identical.
```

Сохранить в `00_character/`:
- `monolith_master.png` — главный референс, прикладывается к **каждой** генерации
- `monolith_turnaround.png`
- `monolith_expressions.png`
- то же для Kachel

## Правила консистентности

1. Каждая генерация = **референс-картинка + блок CHARACTER + блок STYLE**.
2. Не просить в одном кадре сложные действия руками — у ИИ руки всегда слабое место.
3. 1 клип = 1 действие. «Monolith смотрит на плитку и падает в обморок» — ок. «Входит, берёт уровень, проверяет, роняет, ловит, падает» — нет, развалится.
4. Если персонаж поплыл в клипе — выбрасываем, не «и так сойдёт». Серия держится на узнаваемости.
