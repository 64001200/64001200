- 👋 Hi, I’m @64001200
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
64001200/64001200 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Random;
import java.util.Set;

public class UniqueDataSets {
    public static void main(String[] args) {
        List<String> uniqueNames = generateUniqueNames(10);
        System.out.println("Unique Names:");
        for (String name : uniqueNames) {
            System.out.println(name);
        }

        System.out.println();

        List<Integer> uniqueNumbers = generateUniqueNumbers(10, 1, 100);
        System.out.println("Unique Numbers:");
        for (int number : uniqueNumbers) {
            System.out.println(number);
        }
    }

    private static List<String> generateUniqueNames(int count) {
        List<String> names = new ArrayList<>();
        Set<String> uniqueNames = new HashSet<>();

        while (uniqueNames.size() < count) {
            String name = generateRandomName();
            uniqueNames.add(name);
        }

        names.addAll(uniqueNames);
        return names;
    }

    private static String generateRandomName() {
        String[] names = { "Alice", "Bob", "Charlie", "David", "Eve", "Frank", "Grace", "Henry", "Ivy", "Jack", "Kate",
                "Luke", "Megan", "Nathan", "Olivia", "Peter", "Quincy", "Rachel", "Samuel", "Tara", "Uma", "Victor",
                "Wendy", "Xavier", "Yara", "Zane" };
        Random random = new Random();
        int index = random.nextInt(names.length);
        return names[index];
    }

    private static List<Integer> generateUniqueNumbers(int count, int min, int max) {
        List<Integer> numbers = new ArrayList<>();
        Set<Integer> uniqueNumbers = new HashSet<>();

        while (uniqueNumbers.size() < count) {
            int number = generateRandomNumber(min, max);
            uniqueNumbers.add(number);
        }

        numbers.addAll(uniqueNumbers);
        return numbers;
    }

    private static int generateRandomNumber(int min, int max) {
        Random random = new Random();
        return random.nextInt(max - min + 1) + min;
    }
}
