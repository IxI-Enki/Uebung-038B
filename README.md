# Uebung-xxx -- Palindrom


```c#
namespace numberPalindrom
{
  internal class Program
  {
    static void Main()
    {
      string userInput;
      int num;
      int placeValue;
      int revNum = 0;
      int originNum;
      bool isPalindrom;

      Console.Clear();

      Console.Write("\n Geben Sie eine Zahl ein: ");
      userInput = Console.ReadLine();

      Console.Write("\n Sie haben eine " + (int.TryParse(userInput, out num) ? "gültige" : "ungültige") + " Zahl eingegeben.");

      originNum = num;
      do
      {                                      /*                 1     2      3       */
        placeValue = num % 10;               ///   placeValue:  1     2      1

        revNum = revNum * 10 + placeValue;   ///   revNum:      1     12    121    

        num = num / 10;                      ///   num:        12      1     0   

      } while (num > 0);                     ///   while      true   true   false      

      isPalindrom = (originNum == revNum) ? true : false;

      Console.Write($"\n Ihre Zahl ist {(isPalindrom ? "ein" : "kein")} Palindrom.");
      Console

    }
  }
}

```
