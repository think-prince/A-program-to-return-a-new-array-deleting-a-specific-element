# A-program-to-return-a-new-array-deleting-a-specific-element
Java code for deleting specific element in an array

public class DeleteElementInArray {

    public int[] deleteElement(int[] arr, int x){

        int i=0;
        int k=0;
        int count=0;
        for (int j = 0; j < arr.length; j++) {
            if(x==arr[j]){
                count++;
            }
        }
        int[] newArr = new int[arr.length-count];
        while(i<arr.length){
            if(x==arr[i]){
                i++;
            }
            else {
                newArr[k] = arr[i];
                k++;
                i++;
            }
        }
        return newArr;
    }
}

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        System.out.println("Enter size of the Array");
        Scanner input = new Scanner(System.in);
        int size = input.nextInt();
        System.out.println("Enter Elements");
        int[] arr1 = InputArrays.Input(size);

        System.out.println("Enter number to search for: ");
        int num = input.nextInt();

        DeleteElementInArray d1 = new DeleteElementInArray();
        int [] finalArr= d1.deleteElement(arr1,num);
        System.out.print("Final Array: ");
        for (int i = 0; i < finalArr.length; i++) {
            System.out.print(finalArr[i]+" ");
        }
    }
}
