# SortNumbersToDown

package MyPrograms;

import java.io.BufferedReader;
import java.io.InputStreamReader;

/**
 * Created by Дима on 12.03.2015.
 */
public class SortNumb {

Написать программу, которая вводит с клавиатуры 20 чисел и выводит их в убывающем порядке.
*/
        public static void main(String[] args) throws Exception
        {
            BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
            int[] array = new int[20];
            for (int i = 0; i < 20; i++)
            {
                array[i] = Integer.parseInt(reader.readLine());
            }

            sort(array);

            for (int x : array)
            {
                System.out.println(x);
            }
        }

        public static void sort(int[] array)
        {
            int m=0;
            int mi=0;
            for (int i = 0; i < array.length; i++) {
                m=array[i];
                mi=i;
                for (int j = i+1; j < array.length; j++) {
                    if (array[j]>m) {
                        m = array[j];
                        mi = j;
                    }
                }
                if (i!=mi){
                    int tmp=array[i];
                    array[i]=array[mi];
                    array[mi]=tmp;
                }
            }
            //Напишите тут ваш код
        }
    }

