# Conditionals & Wishes · EnglishPRO

App de práctica de las **oraciones condicionales y los deseos** en inglés (ESO / Bachillerato), hecha con el mismo motor y el mismo sistema de corrección que [relative-clauses](https://github.com/nuriacalvo-teacher/relative-clauses), modals y reported speech.

**9 módulos × 3 niveles, con 10 ejercicios por nivel (270 en total):**

1. Zero & First Conditional (verdades generales, futuro posible, imperativo, when / as soon as + presente)
2. Second Conditional (irreal en el presente, If I were you…, could / might)
3. Third Conditional (pasado irreal: had done → would have done)
4. Mixed Conditionals (pasado → presente y presente → pasado)
5. Unless, As Long As, In Case… (unless, as long as, provided / providing that, on condition that, in case, even if, otherwise / or, suppose / supposing, what if) + inversión (Should you…, Were I…, Had I…)
6. Wishes & Regrets (I wish / If only + past simple, could, past perfect y would para quejas; wish ≠ hope)
7. Would Rather, It's Time & Inversion (I'd rather + infinitivo / sujeto + past, it's (high) time + past, as if / as though, condicionales con inversión)
8. Rephrasing (situación real → condicional / wish / unless / in case…, empezando por las palabras dadas, tipo examen)
9. Review of Conditionals & Wishes

- **Level 1:** opción múltiple (hace falta un 90 % para aprobar)
- **Level 2:** rellenar huecos (80 %)
- **Level 3:** traducción del español al inglés (80 %). En el módulo 8 se reescribe una frase en inglés empezando por las palabras entre paréntesis.

En **cada lista de 10 ejercicios** hay 5 frases afirmativas (50 %), 3 preguntas (30 %) y 2 negativas (20 %).

## Corrección

- **Level 2:** si valen varias respuestas (*were / was*, *would / could*, *as long as / provided that*…), se acepta cualquiera. Las contracciones y las mayúsculas no cuentan.
- **Level 3:** se aceptan todas las respuestas correctas: los dos órdenes (*If it rains, we'll stay* / *We'll stay if it rains*), *were* o *was*, *I wish / If only*, las conjunciones equivalentes, sinónimos, contracciones (*I'd = I would = I had*) y ortografía británica y americana.
- Se marcan como error: *will* o *would* detrás de *if / unless / as long as / in case*, el tiempo equivocado (*If I knew, I would have told you*), el pasado en lugar del participio (*would have went*), la doble negación con *unless*, *in case* en lugar de *if* (y al revés), *I wish I would*, *I'd rather you come*, etc.

Si hay que añadir una alternativa, se escribe en el campo `pat` de la frase: `(a|b)` = vale a o b, `[x]` = opcional, `@grupo` = grupo de sinónimos.

## Tests

```
node tests/level3.test.js    # corrector del nivel 3: 90 frases, respuestas buenas y malas
node tests/content.test.js   # 10 ejercicios por nivel y reparto 50/30/20
```

## ⚠️ Firebase: hay que hacer una cosa una sola vez

Esta app guarda los resultados en su propio nodo, **`conditionals_wishes_v1`**, para que las notas de las apps no se mezclen.

En la consola de Firebase (proyecto *goya-english*): Realtime Database → **Reglas**. Duplica el bloque de `relative_clauses_v1`, cambia el nombre a `conditionals_wishes_v1` y publica.

Hasta que no lo hagas, el modo invitado funciona, pero la entrada con código de clase mostrará "Wrong class code".

## Publicarla

Settings → Pages → Deploy from a branch → `main` / root.
