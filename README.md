# Hospital-Patient-Records
This is my second java project
<br>import java.util.ArrayList;
import java.util.Scanner;

class Patient {
    int id;
    String name;
    int age;
    String disease;

    Patient(int id, String name, int age, String disease) {
        this.id = id;
        this.name = name;
        this.age = age;
        this.disease = disease;
    }

    void display() {
        System.out.println("Patient ID: " + id);
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Disease: " + disease);
    }
}

class Doctor extends Patient {
    String doctorName;

    Doctor(int id, String name, int age, String disease,
            String doctorName) {
        super(id, name, age, disease);
        this.doctorName = doctorName;
    }

    @Override
    void display() {
        super.display();
        System.out.println("Doctor: " + doctorName);
    }
}
