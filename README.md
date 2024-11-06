import java.util.List;

public class ReplaceListValues {

    public static void replaceWithValue(int value, List<Integer> list) {
        // Проходим по всем элементам списка и заменяем их на значение value
        for (int i = 0; i < list.size(); i++) {
            list.set(i, value);  // Заменяем элемент на указанный value
        }
    }

    public static void main(String[] args) {
        // Пример использования метода
        List<Integer> numbers = List.of(1, 2, 3, 4, 5); // Список, который хотим изменить
        
        // Создаем изменяемый список, так как List.of создает неизменяемый список
        List<Integer> mutableNumbers = new ArrayList<>(numbers);
        
        System.out.println("До замены: " + mutableNumbers);
        
        // Заменяем все элементы списка на 10
        replaceWithValue(10, mutableNumbers);
        
        System.out.println("После замены: " + mutableNumbers);
    }
}
До замены: [1, 2, 3, 4, 5]
После замены: [10, 10, 10, 10, 10]
