# Finally или просто код?

[importance 5]

Сравните два фрагмента кода. 

<ol>
<li>Первый использует `finally` для выполнения кода по выходу из `try..catch`:

```js
try {
  начать работу
  работать
} catch(e) {
  обработать ошибку
} finally {
*!*
  финализация: завершить работу 
*/!*
}
```

</li>
<li>Второй фрагмент просто ставит очистку ресурсов за `try..catch`:

```js
try {
  начать работу
} catch(e) {
  обработать ошибку
} 

*!*
финализация: завершить работу
*/!*
```

</li>
</ol>

Нужно, чтобы код финализации всегда выполнялся при выходе из блока `try..catch` и, таким образом, заканчивал начатую работу. Имеет ли здесь `finally` какое-то преимущество или оба фрагмента работают одинаково?

Если имеет, то дайте пример когда код с `finally` работает верно, а без -- неверно.