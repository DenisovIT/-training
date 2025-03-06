import java.util.Random;

public class RandomArrayStatistics {
    public static void main(String[] args) {
        int size = 10; 
        double[] randomNumbers = new double[size];

        for (int i = 0; i < size; i++) {
            randomNumbers[i] = Math.random(); 
        }
        System.out.println(); 
        for (double num : randomNumbers) {
            System.out.printf("%.4f ", num);
        }
        System.out.println();

        double max = randomNumbers[0];
        double min = randomNumbers[0];
        double sum = 0;

        for (double num : randomNumbers) {
            if (num > max) {
                max = num; 
            }
            if (num < min) {
                min = num; 
            }
            sum += num; 
        }

        double average = sum / size;

        System.out.printf("Max: %.4f%n", max);
        System.out.printf("Min: %.4f%n", min);
        System.out.printf("Average: %.4f%n", average);
    }
}
