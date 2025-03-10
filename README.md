Console.WriteLine("Введите систему счисления из которой переводим (от 2-ой до 9-ой)");
string s2 = Console.ReadLine();
int s1 = Convert.ToInt32(s2);
if (s1 > 9 || s1 < 2)
{
    Console.WriteLine("Неправильная система счисления");
}
else
{
    Console.WriteLine("Система счисления в которую переводим (от 2-ой до 9-ой)");
    string s3 = Console.ReadLine();
    int s4 = Convert.ToInt32(s3);
    if (s4 > 9 || s4 < 2)
    {
        Console.WriteLine("Неправильная система счисления");
    }
    else
    {
        Console.WriteLine("Введите число которое хотите перевести (от 0 до 888888)");
        string num = Console.ReadLine();
        int number = Convert.ToInt32(num);
        if (number > 888888 || number < 0)
        {
            Console.WriteLine("Введите другое число");
        }
        else
        {
            short digitsCount = 0;
            int temp = number;
            if (number > 100000)
            {
                while (temp > 0)
                {
                    digitsCount++;
                    temp /= 10;
                }
                int[] digits = new int[digitsCount];
                for (int i = digitsCount - 1; i >= 0; i--)
                {
                    digits[i] = number % 10;
                    number /= 10;
                }
                int a = digits[0];
                int b = digits[1];
                int c = digits[2];
                int d = digits[3];
                int e = digits[4];
                int f = digits[5];
                if (a < s1 && b < s1 && c < s1 && d < s1 && e < s1 && f < s1)
                {
                    double res1 = a * (s1 * s1 * s1 * s1 * s1) + b * (s1 * s1 * s1 * s1) + c * (s1 * s1 * s1) + d * (s1 * s1) + e * s1 + f * 1;
                    int res2 = Convert.ToInt32(res1);
                    int digitsCount2 = 0;
                    int temp2 = res2;
                    while (temp2 > 0)
                    {
                        digitsCount2++;
                        temp2 /= s4;
                    }
                    if (digitsCount2 == 0) digitsCount2 = 1;
                    int[] digits2 = new int[digitsCount2];
                    temp2 = res2;
                    for (int i = digitsCount2 - 1; i >= 0; i--)
                    {
                        digits2[i] = temp2 % s4;
                        temp2 /= s4;
                    }
                    string resultat = "";
                    for (int i = 0; i < digitsCount2; i++)
                    {
                        resultat += digits2[i].ToString();
                    }
                    Console.WriteLine(resultat);
                }
                else
                {
                    Console.WriteLine("Число не находится в системе счисления заданой вами");
                }
            }
            else if (number < 100000 && number > 10000)
            {
                while (temp > 0)
                {
                    digitsCount++;
                    temp /= 10;
                }
                int[] digits = new int[digitsCount];
                for (int i = digitsCount - 1; i >= 0; i--)
                {
                    digits[i] = number % 10;
                    number /= 10;
                }
                int a = digits[0];
                int b = digits[1];
                int c = digits[2];
                int d = digits[3];
                int e = digits[4];
                if (a < s1 && b < s1 && c < s1 && d < s1 && e < s1)
                {
                    double res = a * (s1 * s1 * s1 * s1) + b * (s1 * s1 * s1) + c * (s1 * s1) + d * s1 + e * 1;
                    int res2 = Convert.ToInt32(res);
                    int digitsCount2 = 0;
                    int temp2 = res2;
                    while (temp2 > 0)
                    {
                        digitsCount2++;
                        temp2 /= s4;
                    }
                    if (digitsCount2 == 0) digitsCount2 = 1;
                    int[] digits2 = new int[digitsCount2];
                    temp2 = res2;
                    for (int i = digitsCount2 - 1; i >= 0; i--)
                    {
                        digits2[i] = temp2 % s4;
                        temp2 /= s4;
                    }
                    string resultat = "";
                    for (int i = 0; i < digitsCount2; i++)
                    {
                        resultat += digits2[i].ToString();
                    }
                    Console.WriteLine(resultat);
                }
                else
                {
                    Console.WriteLine("Число не находится в системе счисления заданой вами");
                }
            }
            else if (number < 10000 && number > 1000)
            {
                while (temp > 0)
                {
                    digitsCount++;
                    temp /= 10;
                }
                int[] digits = new int[digitsCount];
                for (int i = digitsCount - 1; i >= 0; i--)
                {
                    digits[i] = number % 10;
                    number /= 10;
                }
                int a = digits[0];
                int b = digits[1];
                int c = digits[2];
                int d = digits[3];
                if (a < s1 && b < s1 && c < s1 && d < s1)
                {
                    double res = a * (s1 * s1 * s1) + b * (s1 * s1) + c * s1 + d * 1;
                    int res2 = Convert.ToInt32(res);
                    int digitsCount2 = 0;
                    int temp2 = res2;
                    while (temp2 > 0)
                    {
                        digitsCount2++;
                        temp2 /= s4;
                    }
                    if (digitsCount2 == 0) digitsCount2 = 1;
                    int[] digits2 = new int[digitsCount2];
                    temp2 = res2;
                    for (int i = digitsCount2 - 1; i >= 0; i--)
                    {
                        digits2[i] = temp2 % s4;
                        temp2 /= s4;
                    }
                    string resultat = "";
                    for (int i = 0; i < digitsCount2; i++)
                    {
                        resultat += digits2[i].ToString();
                    }
                    Console.WriteLine(resultat);
                }
                else
                {
                    Console.WriteLine("Число не находится в системе счисления заданой вами");
                }
            }
            else if (number < 1000 && number > 100)
            {
                while (temp > 0)
                {
                    digitsCount++;
                    temp /= 10;
                }
                int[] digits = new int[digitsCount];
                for (int i = digitsCount - 1; i >= 0; i--)
                {
                    digits[i] = number % 10;
                    number /= 10;
                }
                int a = digits[0];
                int b = digits[1];
                int c = digits[2];
                if (a < s1 && b < s1 && c < s1)
                {
                    double res = a * (s1 * s1) + b * s1 + c * 1;
                    int res2 = Convert.ToInt32(res);
                    int digitsCount2 = 0;
                    int temp2 = res2;
                    while (temp2 > 0)
                    {
                        digitsCount2++;
                        temp2 /= s4;
                    }
                    if (digitsCount2 == 0) digitsCount2 = 1;
                    int[] digits2 = new int[digitsCount2];
                    temp2 = res2;
                    for (int i = digitsCount2 - 1; i >= 0; i--)
                    {
                        digits2[i] = temp2 % s4;
                        temp2 /= s4;
                    }
                    string resultat = "";
                    for (int i = 0; i < digitsCount2; i++)
                    {
                        resultat += digits2[i].ToString();
                    }
                    Console.WriteLine(resultat);
                }
                else
                {
                    Console.WriteLine("Число не находится в системе счисления заданой вами");
                }
            }
            else if (number < 100 && number > 10)
            {
                while (temp > 0)
                {
                    digitsCount++;
                    temp /= 10;
                }
                int[] digits = new int[digitsCount];
                for (int i = digitsCount - 1; i >= 0; i--)
                {
                    digits[i] = number % 10;
                    number /= 10;
                }
                int a = digits[0];
                int b = digits[1];
                if (a < s1 && b < s1)
                {
                    double res = a * s1 + b * 1;
                    int res2 = Convert.ToInt32(res);
                    int digitsCount2 = 0;
                    int temp2 = res2;
                    while (temp2 > 0)
                    {
                        digitsCount2++;
                        temp2 /= s4;
                    }
                    if (digitsCount2 == 0) digitsCount2 = 1;
                    int[] digits2 = new int[digitsCount2];
                    temp2 = res2;
                    for (int i = digitsCount2 - 1; i >= 0; i--)
                    {
                        digits2[i] = temp2 % s4;
                        temp2 /= s4;
                    }
                    string resultat = "";
                    for (int i = 0; i < digitsCount2; i++)
                    {
                        resultat += digits2[i].ToString();
                    }
                    Console.WriteLine(resultat);
                }
                else
                {
                    Console.WriteLine("Число не находится в системе счисления заданой вами");
                }
            }
            else if (number < 10 && number > 0)
            {
                int a = number;
                if (a < s1)
                {
                    int res2 = a;
                    int digitsCount2 = 0;
                    int temp2 = res2;
                    while (temp2 > 0)
                    {
                        digitsCount2++;
                        temp2 /= s4;
                    }
                    if (digitsCount2 == 0) digitsCount2 = 1;
                    int[] digits2 = new int[digitsCount2];
                    temp2 = res2;
                    for (int i = digitsCount2 - 1; i >= 0; i--)
                    {
                        digits2[i] = temp2 % s4;
                        temp2 /= s4;
                    }
                    string resultat = "";
                    for (int i = 0; i < digitsCount2; i++)
                    {
                        resultat += digits2[i].ToString();
                    }
                    Console.WriteLine(resultat);
                }
                else
                {
                    Console.WriteLine("Число не находится в системе счисления заданой вами");
                }
            }
        }
    }
}
