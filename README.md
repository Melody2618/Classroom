# Classroom

public class Classroom{
  

  public static void printArray2DRC(String[][] arr){
    for(int row = 0; row < arr.length; row++){
        for (int col = 0; col < arr[row].length; col++){
            System.out.print(arr[row][col] + "\t");
        }
        System.out.println();
    }
           System.out.println(); 
  }
  
    public static void printArray(String[] arr){ 
    for (int i = 0; i < arr.length; i++){
        System.out.print(arr[i] + " ");
        }   
    }

  public static void main ( String[] args ) {
    int numRows = Integer.parseInt(args[0]); 
    int numCols = Integer.parseInt(args[1]); 
    String[] studentLine = new String[numRows*numCols]; 
    String[][] room = new String[numRows][numCols];  
    int numStudents = studentLine.length; 

    for (int count = 0; count < numStudents; count++ ) { 
        studentLine[count] = args[count + 2]; 
    }
    System.out.print("Students:   "); 
    for(String s: studentLine){
        System.out.print(s+" ");
    }
    System.out.println();
    System.out.println();

    
    System.out.println("classroom");
    int  count = 0;        
    for (int row = 0; row < room.length; row++){
        for (int col = 0; col < room[row].length; col ++){
            room[row][col] = studentLine[count];
            count++;
        }
    }
   
    for (int row = 0; row < room.length; row++){
        for (int col = 0; col < room[row].length; col ++){
            System.out.print(room[row][col] + "\t");
        System.out.println();
    }
      
        count = 0;
   
        for (int col = 0; col < room[0].length; col ++){ 
            for (int row = 0; row < room.length; row++){
              studentLine[count]=room[row][col];
              count++;
            }
        }

       
        System.out.print("students leaving room by column: ");
        for (int i = 0; i < studentLine.length; i++){
                System.out.print(studentLine[i] + " ");
            }
            StdOut.println();
    }
}
}
