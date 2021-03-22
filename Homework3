using System;
using System.IO;
using System.Text;
using System.Threading.Tasks;

namespace homework_3
{
    class Program
    {
        static void Main(string[] args)
        {
            //Create file
            
            string path = @"C:\temp\Text.txt";
            // создаем каталог для файла
            
            DirectoryInfo dirInfo = new DirectoryInfo(path);
            
            Console.WriteLine("Введите строку для записи в файл:");
            string text = Console.ReadLine();

            // запись в файл
            Console.WriteLine();
            File.AppendAllText(path, text+"\n");

            // чтение из файла
            using (FileStream fstream = File.OpenRead($"{path}"))
            {
                // преобразуем строку в байты
                byte[] array = new byte[fstream.Length];
                // считываем данные
                fstream.Read(array, 0, array.Length);
                // декодируем байты в строку
                string textFromFile = System.Text.Encoding.Default.GetString(array);
                Console.WriteLine($"Текст из файла: {textFromFile}");
            }

            Console.ReadLine();

            
        }
        
    }
}
