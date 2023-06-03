#include <iostream>
#include <string>
int main() {
	
	setlocale(LC_ALL, "RU");
	
	using std::cout;
	using std::cin;
	using std::endl;
	using std::string;

	const int GOLD_PIECES = 900;
	int adventurers, killed, survivors;

	string leader;
	cout << "Добро пожаловать в Lost Fortune\n\n";
	cout << "Пожалуйста, введите следующие значения для вашего личного приключения\n";
	
	cout << "Введите колчество героев которое отправиться за кладом: ";
	cin >> adventurers;
	
	cout << "Введите число меньше первого: ";
	cin >> killed;
	
	survivors = adventurers - killed;

	cout << "Введите ваше имя: ";
	cin >> leader;

	//Сюжет
	cout << "\nОтважная группа из " << adventurers << " человек отправилась на поиски ";
	cout << "утраченного сокровища Древних Гномов. ";
	cout << "Группой руководил это легендарный разбойник " << leader << ".\n";
	cout << "\nОни прошли долгий путь, а банда мародеров-людоедов напала на отряд из засады. ";
	cout << "Все они храбро сражались под командованием " << leader;
	cout << ", и огры были побеждены, но какой ценой. ";
	cout << "Из искателей приключений, " << killed << " были побеждены, ";
	cout << "уходя осталось " << survivors << " людей в группе.\n";
	cout << "\nПуть был близок к тому, чтобы потерять всякую надежду. ";
	cout << "Но во время погребения усопшего, ";
	cout << "они наткнулись на зарытое сокровище. ";
	cout << "Итак, авантюристы разделили " << GOLD_PIECES << " золотых монет. ";
	cout << leader << " забрал лишнее " << (GOLD_PIECES % survivors);
	cout << ", чтобы все было честно, конечно.\n";
	
	return 0;
}
