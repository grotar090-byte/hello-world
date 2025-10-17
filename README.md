
class FitnessCenter
{
    static void Main()
    {
        Console.Title = "Фітнес центр";
        Console.ForegroundColor = ConsoleColor.Green;
        Console.WriteLine("=== Ласкаво просимо у Fitness Center ===\n");
        Console.ResetColor();

        // Ціни
        double priceGym = 800;   // грн за місяць
        double priceGroup = 600; // грн за групові заняття
        double priceTrainer = 300; // грн за персональне тренування

        // Ввід даних
        Console.Write("Введіть кількість місяців у тренажерному залі: ");
        int months = Convert.ToInt32(Console.ReadLine());

        Console.Write("Введіть кількість групових абонементів: ");
        int groups = Convert.ToInt32(Console.ReadLine());

        Console.Write("Введіть кількість персональних тренувань: ");
        int trainings = Convert.ToInt32(Console.ReadLine());

        // Розрахунок вартості
        double costGym = months * priceGym;
        double costGroup = groups * priceGroup;
        double costTrainer = trainings * priceTrainer;

        double total = costGym + costGroup + costTrainer;

        // Генерація знижки
        Random rnd = new Random();
        int discount = rnd.Next(5, 21); // від 5% до 20%
        double totalWithDiscount = total * (1 - discount / 100.0);

        // Вивід результатів
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\n--- Ваш чек ---");
        Console.ResetColor();

        Console.WriteLine($"Тренажерний зал: {months} міс × {priceGym} грн = {Math.Round(costGym, 2)} грн");
        Console.WriteLine($"Групові заняття: {groups} × {priceGroup} грн = {Math.Round(costGroup, 2)} грн");
        Console.WriteLine($"Персональні тренування: {trainings} × {priceTrainer} грн = {Math.Round(costTrainer, 2)} грн");

        Console.WriteLine($"\nЗагальна сума: {Math.Round(total, 2)} грн");
        Console.WriteLine($"Знижка: {discount}%");
        Console.ForegroundColor = ConsoleColor.Cyan;
        Console.WriteLine($"До сплати: {Math.Round(totalWithDiscount, 2)} грн");
        Console.ResetColor();

        // Використання Math
        Console.WriteLine($"\nПеревірка: sqrt(144) = {Math.Sqrt(144)}");
        Console.WriteLine($"2^10 = {Math.Pow(2, 10)}");

        Console.WriteLine("\nДякуємо, що обрали наш фітнес центр!");
        Console.ReadKey();
    }
}
