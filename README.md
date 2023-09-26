# SayiTahminOyunu

-----------------------------------

namespace ConsoleApp1;

internal class Program
{
    static void Main(string[] args)
    {

        Random rnd = new Random();

        int number = rnd.Next(1,10);
        int hak = 3;
        string strSayi;

        int ConvertResponse;
        bool isConvertSuccess;

        Console.WriteLine("Sayı Tahmin Oyunu");
        do
        {
            hak -= 1;
            Console.WriteLine("Lütfen Sayıyı Tahmin Edin");
            Console.WriteLine("Sayı 1 ila 10 arasında olacak");
            Console.WriteLine($"Sayı : {number}");
            strSayi = Console.ReadLine();
            isConvertSuccess = int.TryParse(strSayi, out ConvertResponse);
            if (isConvertSuccess != true)
            {
                Console.WriteLine("Lütfen Numaratik Deger Giriniz");
                Console.WriteLine();
            }
            if (hak == 0)
            {
                Console.WriteLine("Hakkınız Bitti Kazanamadınız :(");
                return;
            }
        } while (ConvertResponse != number);

        Console.WriteLine("Tebrikler Dogru Tahmin :)");

        Console.ReadLine();
    }
}
