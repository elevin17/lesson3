<?php
//Составить массив, ключами в котором будут названия континентов (на английском - Africa), значениями — массивы из латинских названий зверей (например, Mammuthus columbi – можно найти в карточке статистики о животном справа). Найдите различных зверей и составьте массив так, чтобы для ключа Africa у вас значением был бы массив из зверей, там обитавших или обитающих

$continents = ['Africa', 'Antarctica', 'Asia',  'Australia', 'Europe', 'North America', 'South America']; 



//print_r($continents);


$Africa_animals = ['Massospondylus','Panthera leo', 'Loxodonta africana','Panthera pardus', 'Lemuridae', 'Hapalemur', 'Okapia johnstoni', 'Giraffa camelopardalis', 'Equus burchelli', 'Crocodylia', 'Crocodylus niloticus'];

$Antarctica_animals = ['Belgica antarctica','Euphausia superba','Alaskozetes antarcticus','Cryptopygus antarcticus','Belgica antarctica','Aptenodytes forsteri','Pygoscelis adeliae','Lagenorhynchus cruciger','Stereotydeus villosus','Nanorchtestes antarcticus','Tydeus tilbrooki'];

$Asia_animals = ['Gordius fulgur','Gordius zwicki','Hypselotriton wolterstorffi','Tylototriton verrucosus', 'Tylototriton','Tylototriton asperrimus','Tylototriton broadoridgus','Tylototriton dabienicus','Tylototriton hainanensis','Tylototriton liuyangensis','Tylototriton notialis'];

$Australia_animals = ['Macropus agilis','Macropus eugenii','Macropus giganteus','Macropus rufus','Phascolarctos cinereus','Sarcophilus harrisii','Tachyglossus aculeatus','Trichosurus vulpecula','Vombatus ursinus','Zaglossus bruijni','Ornithorhynchus anatinus'];

$Europe_animals = ['Alytes obstetricans','Proteus anguinus','Calotriton arnoldi','Lyciasalamandra','Calotriton asper','Triturus karelinii','Salamandra lanzai','Bufo calamita','Salamandrina','Bombina bombina'];

$North_America_animals = ['Adelobasileus cromptoni','Aepycamelus','Aepycamelus bradyi','Aepycamelus elrodi','Aepycamelus giraffinus','Aepycamelus major','Aepycamelus priscus','Aepycamelus procerus','Aepycamelus robustus','Aepycamelus_stocki'];

$South_America_animals = ['Anhanguera','Acdestodon bonapartei','Araripesaurus','Aetodactylus','Aerotitan','Alamodactylus','Alanqa','Allkaruen','Amblydectes','Angustinaripterus','Anhanguera'];



$continents_animals = [
			$continents[0]=>$Africa_animals,
			$continents[1]=>$Antarctica_animals,
			$continents[2]=>$Asia_animals,
			$continents[3]=>$Australia_animals,
			$continents[4]=>$Europe_animals,
			$continents[5]=>$North_America_animals,
			$continents[6]=>$South_America_animals
			];

echo'<pre>Выведем массив из континентов и животных<br>';
print_r($continents_animals);
echo'</pre>';


// Выберите только один континент для каждого животного. Пусть у вас получится 10-15 зверей.

echo'<p>Считаем животных для каждого континента<br>';
foreach($continents_animals as $k=>$v){
	print_r($k . '<br>'.'количество животных '.count($v).'<br>');
}
echo'</p>';

//Теперь найдите всех зверей, название которых состоит из двух слов. Составьте из них новый массив.

$new_animals_array=array();
foreach ($continents_animals as $k=>$v){
	foreach($v as $animals){
		if (!in_array($animals,$new_animals_array) && strpos($animals, ' ')){       //Если еще не в еще массиве и состоит из двух слов
			$new_animals_array[]=$animals;
			
		}
	}
}
echo'<pre>Выведем новый массив животных из 2-х слов<br>';
print_r($new_animals_array);
echo'</pre>';


//Случайно перемешайте между собой первые и вторые слова названий животных так, чтобы на выходе мы получили выдуманных, фантазийных животных. Название фантазийного животного должно начинаться с первого слова реального названия животного. Важно, чтобы каждый кусочек был использован и не повторялся более одного раза. Ничего страшного, если в результате перемешивания иногда будут получаться реальные животные. Вывести этих животных на экран.

$k_first=array();
$k_second=array();
foreach ($new_animals_array as $k){
	$k_first[]=explode(' ' ,$k)[0];
	$k_second[]=explode(' ' ,$k)[1];
	
}

$fantasy_animal=array();

$k_first_placed=array();

$k_second_placed=array();

while($j=rand(0,count($k_second))){
	if(!in_array($k_second[$j], $k_second_placed)){
		for ($i=0; $i<count($k_first); $i++){
			if(!in_array($k_first[$i], $k_first_placed)){
				$fantasy_animal[]=$k_first[$i].' '.$k_second[$j];
				$k_second_placed[]=$k_second[$j];
				$k_first_placed[]=$k_first[$i];
			}
			}
		}
	}

	



echo'<pre>Выведем фантазийных животных<br>';
print_r($fantasy_animal);
echo'</pre>';
?>
