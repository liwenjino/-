using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        // 
        static void Main(string[] args)
        {
            int[] ArrayInt = new int[] { 0, 1, 2, 3, 4, 6, 7, 8, 9 };
            Console.WriteLine("原数组元素：");
            foreach (int i in ArrayInt)
            {
                Console.Write(i + " ");
            }
            Console.WriteLine();
            ArrayInt = AddArray(ArrayInt, 4, 5);
            Console.WriteLine("插入之后的数组元素：");
            foreach (int i in ArrayInt)
            {
                 Console.Write(i + " ");
            }
            Console.ReadLine();
        }
        static int[] AddArray(int[] ArrayBorn, int Index, int Value) {
            if (Index >= (ArrayBorn.Length))
                Index = ArrayBorn.Length - 1;
            int[] TemArray = new int[ArrayBorn.Length + 1];
            for (int i = 0; i < TemArray.Length; i++)
            {
                if (Index >= 0)
                {
                    if (i < (Index+1))
                    
                        TemArray[i] = ArrayBorn[i];
                    
                    else if (i == (Index + 1))
                    
                        TemArray[i] = Value;
                    
                    else
                    
                        TemArray[i] = ArrayBorn[i - 1];
                    
                }
                else {
                    if (i == 0)
                    
                        TemArray[i] = Value;
                    
                    else 
                        TemArray[i] = ArrayBorn[i - 1];
                    
                }
            } 
            return TemArray; 
        }


    }
}
