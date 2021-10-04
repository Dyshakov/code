Пример кода.

<?php

$collatorRu = new Collator('ru_RU');
$result = $collatorRu->compare("Ель", "Ёлка");
var_dump($result); // 1, Ель > Ёлка

$result2 = $collatorRu->compare("Е", "Ё");
var_dump($result2); // -1, Е < Ё

// Немецкий
$collatorDe = new Collator('de_DE');
// Игнорировать различия в написании букв и акценты
$collatorDe->setAttribute(Collator::STRENGTH, Collator::PRIMARY);
$result3 = $collatorDe->compare("ss", "ß");
var_dump($result3); // 0 - строки равны
