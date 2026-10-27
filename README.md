package com.pakagehospitalmanegment;



 class Inpateint extends Patient {
    int day;
    Inpateint(int id , String name ,int age , int day) {
        super(id, name, age);
        this.day = day;

    }
       @Override 
       double bill() {
        return 500 +day*1500;
       }
       @Override 
       void display() {
        super.display();
        System.out.println("Admitted days:" +day);
       }
}


