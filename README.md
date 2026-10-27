package com.pakagehospitalmanegment;


    class Patient {
        int id;
        int age;
        String name;

        Patient(int id, String name, int age) {
            this.id = id;
            this.name = name;
            this.age = age;

        }

        void display() {
            System.out.println("id:" + id);
            System.out.println("name:" + name);
            System.out.println("age:" + age);
        }

        double bill() {
            return 500;
        }

    }


