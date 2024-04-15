# The-waste-classification-system_Pabitra-Singha-Sagor
The waste classification system is a Java-based project designed to assist in sustainable waste management by categorizing waste items into recyclable, organic, or non-recyclable groups based on user-provided characteristics. This system serves as a foundational tool to promote efficient recycling practices and reduce environmental impact.

// Java script
import java.util.Scanner;

public class WasteClassificationSystem {
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter characteristics of waste (e.g., type, material, etc.):");
        String wasteCharacteristics = scanner.nextLine();

        String classification = classifyWaste(wasteCharacteristics);
        System.out.println("The waste is classified as: " + classification);

        scanner.close();
    }

    public static String classifyWaste(String characteristics) {
        // Decision rules for waste classification
        if (characteristics.contains("plastic")) {
            return "Recyclable";
        } else if (characteristics.contains("organic")) {
            return "Organic";
        } else if (characteristics.contains("glass")) {
            return "Recyclable";
        } else {
            return "Non-recyclable";
        }
    }
}
