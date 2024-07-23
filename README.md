import java.util.Scanner;
import java.io.File;
import java.io.FileNotFoundException;

public class JobApplication {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Say Hello
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Hello, " + name + "!");

        // Simulate uploading a resume
        System.out.print("Enter the path to your resume: ");
        String resumePath = scanner.nextLine();
        
        File resume = new File(resumePath);
        if (resume.exists() && !resume.isDirectory()) {
            System.out.println("Resume found at: " + resumePath);
            // Simulate the process of uploading the resume
            uploadResume(resume);
            System.out.println("Resume uploaded successfully!");
        } else {
            System.out.println("Resume not found at: " + resumePath);
        }
        
        scanner.close();
    }

    public static void uploadResume(File resume) {
        // In a real application, you would add code to upload the file to a server.
        // This is just a simulation.
        System.out.println("Uploading resume...");
    }
}
