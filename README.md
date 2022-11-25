# -Exercise-4.17-Gas.java-Gas-Mileage-Java-How-To-Program-9th-Ed.-Deitel-
Java Program to find Gas Mileage

4.17 (Gas Mileage) Drivers are concerned with the mileage their automobiles get. One driver has
        kept track of several trips by recording the miles driven and gallons used for each tankful.

        Develop a Java application that will input the miles driven and gallons used (both as integers) for each trip.


        The program should calculate and display the miles per gallon obtained for each trip and print the
        combined miles per gallon obtained for all trips up to this point.

        All averaging calculations should
        produce floating-point results.

        Use class Scanner and sentinel-controlled repetition to obtain the
        data from the user.
        
        
        import java.util.Scanner;

public class Main {
    public static void main(String[] args){
  
        Scanner console = new Scanner(System.in);

        int Gallon, Miles, MilesPerGallon, TotalGallons=0, TotalMiles=0;

        System.out.println("Enter Miles Driven: or value less then or equal 0 to quit: ");
        Miles = console.nextInt();

        System.out.println("Enter Gallons Used:  or value less then or equal 0 to Quit ");
        Gallon = console.nextInt();

        while (Miles >= 1 && Gallon >=1 ){
            TotalGallons = TotalGallons+Gallon;
            TotalMiles += Miles;

            System.out.println("Enter Miles Driven: or value less then or equal 0 to quit: ");
            Miles = console.nextInt();

            System.out.println("Enter Gallons Used:  or value less then or equal 0 to Quit ");
            Gallon = console.nextInt();
        }

        if (TotalMiles!=0 && TotalGallons !=0){
            MilesPerGallon= TotalMiles/TotalGallons;
            System.out.println("Mile Per Gallons are: "+ MilesPerGallon);
        }


        System.out.println("Total Gallons are: " + TotalGallons);
        System.out.println("Total Miles are: " + TotalMiles);

        //Final Calculation in Float


        float TotalGallon = TotalGallons;
        float TotalMile = TotalMiles;
        System.out.println("Total Gallons are: " + TotalGallon);
        System.out.println("Total Miles are: " + TotalMile);
    }
}
