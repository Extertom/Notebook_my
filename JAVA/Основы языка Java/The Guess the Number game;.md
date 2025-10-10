import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        scannerNumber();
    }

    public static void scannerNumber() {
        try {
            Scanner scanner = new Scanner(System.in);
            while (true) {
                System.out.println("Выберите уровень (1-4):");
                System.out.println("1 - Легкий ");
                System.out.println("2 - Средний ");
                System.out.println("3 - Сложный ");
                System.out.println("4 - Ужасный ");
                System.out.println("5 - Выход ");

                if (!scanner.hasNextInt()) {
                    System.out.println("Ошибка: Нужно ввести число!");
                    scanner.next();
                    continue;
                }
                int input = scanner.nextInt();
                scanner.nextLine();
                if (input == 5) {
                    System.out.println("Выход из программы...");
                    break;
                }
                if (input < 1 || input > 5) {
                    System.out.println("Неверный выбор! Введите число от 1 до 5! ");
                    continue;
                }

                executeMethod(input, scanner);
            }

        } catch (Exception e) {
            System.out.println("Произошла ошибка: Введите целое число! " + e.getMessage());
        }
    }

    public static void caseOne(Scanner scanner) {
        int aiNumbers = new Random().nextInt(10) + 1;
        int attempts = 3;
        System.out.println("Вы выбрали легкий уровень 1");
        System.out.println("Компьютер загадал число от 1 до 10");
        System.out.println("У Вас " + attempts + " попыток ");
        playGame(aiNumbers, attempts, scanner);
    }

    public static void caseTwo(Scanner scanner) {
        int aiNumbers = new Random().nextInt(25) + 1;
        int attempts = 5;
        System.out.println("Вы выбрали средний уровень 2");
        System.out.println("Компьютер загадал число от 1 до 25");
        System.out.println("У Вас " + attempts + " попыток ");
        playGame(aiNumbers, attempts, scanner);
    }

    public static void caseThree(Scanner scanner) {
        int aiNumbers = new Random().nextInt(50) + 1;
        int attempts = 7;
        System.out.println("Вы выбрали сложный уровень 3");
        System.out.println("Компьютер загадал число от 1 до 50");
        System.out.println("У Вас " + attempts + " попыток ");
        playGame(aiNumbers, attempts, scanner);
    }

    public static void caseFour(Scanner scanner) {
        int aiNumbers = new Random().nextInt(100) + 1;
        int attempts = 5;
        System.out.println("Вы выбрали ужасный уровень 4");
        System.out.println("Компьютер загадал число от 1 до 100");
        System.out.println("У Вас " + attempts + " попыток ");
        playGame(aiNumbers, attempts, scanner);
    }

    public static void playGame(int aiNumbers, int maxAttempts, Scanner scanner) {
        int attemptsLeft = maxAttempts;
        while (attemptsLeft > 0) {
            System.out.println("\nПопыток осталось: " + attemptsLeft);
            System.out.print("Введите Ваше число!");

            if (!scanner.hasNextInt()) {
                System.out.println("Ошибка! Нужно ввести число");
                scanner.next();
                continue;
            }
            int userGuess = scanner.nextInt();
            scanner.nextLine();
            if (userGuess == aiNumbers) {
                System.out.println("🎉 Поздравляем! Вы угадали число " + aiNumbers + "!");
                System.out.println("Вы использовали " + (maxAttempts - attemptsLeft + 1) + " попыток");
                return;
            } else if (userGuess < aiNumbers) {
                System.out.println("Загаданное число БОЛЬШЕ Вашего");
            } else {
                System.out.println("Загаданное число МЕНЬШЕ Вашего");
            }
            attemptsLeft--;
            if (attemptsLeft <= 3 && attemptsLeft > 0) {
                System.out.println("💡 Подсказка: число находится в диапазоне ±5 от " + userGuess);
            }

        }
        System.out.println("😞 Вы проиграли! Загаданное число было: " + aiNumbers);
    }

    public static void executeMethod(int input,Scanner scanner) {
        switch (input) {
            case 1:
                caseOne(scanner);
                break;
            case 2:
                caseTwo(scanner);
                break;
            case 3:
                caseThree(scanner);
                break;
            case 4:
                caseFour(scanner);
                break;
        }
        System.out.print("\nХотите сыграть еще раз? (да/нет): ");
        String playAgain = scanner.nextLine();
        if (!playAgain.equalsIgnoreCase("да")) {
            System.out.println("Спасибо за игру! До свидания!");
            System.exit(0);
        }
    }
}


