# Assignment
#java code
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package topsecret;

import java.io.BufferedReader;
import java.io.File;
import java.io.FileInputStream;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.util.Scanner;
import javax.swing.JOptionPane;

/**
 *
 * @author NivethaKrishnan
 */
public class TopSecret {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        // String filepath ="C:\\Users\\NivethaKrishnan\\Documents\\NetBeansProjects\\dire.txt";
        String f1 = "Secret";
        String f2 = "Top secret";
        String f3 = "Public";
        String f4 = "folder11";

        treedata();
        readrecord(f1,f2);
       readrecord1(f1);
       readrecord2 (f2);
       readrecord3(f3);
      // readrecord4(f4,f1,f2);
       

    }
    // For dispalying the id and parent id as key and value.
    public static void treedata()
    {
        try {
            FileInputStream fin = new FileInputStream("C:\\Users\\NivethaKrishnan\\Documents\\NetBeansProjects\\dire.txt");
            BufferedReader b = new BufferedReader(new InputStreamReader(fin));
            String line = "";
            while ((line = b.readLine()) != null) {
                String[] lineArray =line.split(";");
             //   if (lineArray.length == 2) {
               //     {                        
                        System.out.println(lineArray[0] + " " + lineArray[1]);
                          //System.out.println(lineArray.length);
              
                 //   }
            }
            
            fin.close();
    }
          catch (Exception e) {
            e.printStackTrace();
            System.out.println(e);   
         }
        System.out.println("\n\n");
    }
    // for displaying the classification of secret and Top secret
    public static void readrecord(String f1,String f2) {
        try {
            FileInputStream fin = new FileInputStream("C:\\Users\\NivethaKrishnan\\Documents\\NetBeansProjects\\dire.txt");
            BufferedReader b = new BufferedReader(new InputStreamReader(fin));
            String line = "";
            while ((line = b.readLine()) != null) {
                String[] lineArray =line.split(";");
                if (lineArray.length == 7) {
                    if (f1.equals(lineArray[5]) || f2.equals(lineArray[5])) {
                        System.out.println("id = " + lineArray[0] + " , parentid = " + lineArray[1] + " , name = " + lineArray[2] + " , type = " + lineArray[3] + " , size = " + lineArray[4] + " , classification = " + lineArray[5] + " , checksum = " + lineArray[6]);
                    }
                }
            }
            fin.close();
        } catch (Exception e) {
            e.printStackTrace();
            System.out.println(e);
        }
        System .out.println("\n\n");
    }
   
   // for displaying the classification of secret.
     public static void readrecord1(String f1) {
        try {
            FileInputStream fin = new FileInputStream("C:\\Users\\NivethaKrishnan\\Documents\\NetBeansProjects\\dire.txt");
            BufferedReader b = new BufferedReader(new InputStreamReader(fin));
            String line = "";
            while ((line = b.readLine()) != null) {
                String[] lineArray =line.split(";");
                if (lineArray.length == 7) {
                    if (f1.equals(lineArray[5])) {                        
                        System.out.println("id = " + lineArray[0] + " , parentid = " + lineArray[1] + " , name = " + lineArray[2] + " , type = " + lineArray[3] + " , size = " + lineArray[4] + " , classification = " + lineArray[5] + " , checksum = " + lineArray[6]);
                    }
                }
            }
            fin.close();
        } catch (Exception e) {
            e.printStackTrace();
            System.out.println(e);
        }
        System .out.println("\n\n");
    }
     // for disolaying the classification of Top secret.
   public static void readrecord2(String f2) {
        try {
            FileInputStream fin = new FileInputStream("C:\\Users\\NivethaKrishnan\\Documents\\NetBeansProjects\\dire.txt");
            BufferedReader b = new BufferedReader(new InputStreamReader(fin));
            String line = "";
            while ((line = b.readLine()) != null) {
                String[] lineArray =line.split(";");
                if (lineArray.length == 7) {
                    if (f2.equals(lineArray[5])) {                        
                        System.out.println("id = " + lineArray[0] + " , parentid = " + lineArray[1] + " , name = " + lineArray[2] + " , type = " + lineArray[3] + " , size = " + lineArray[4] + " , classification = " + lineArray[5] + " , checksum = " + lineArray[6]);
                    }
                }
            }
            fin.close();
        } catch (Exception e) {
            e.printStackTrace();
            System.out.println(e);
        }
        System .out.println("\n\n");
    }
   // for displaying the classification of public.
    public static void readrecord3(String f3) {
        try {
            FileInputStream fin = new FileInputStream("C:\\Users\\NivethaKrishnan\\Documents\\NetBeansProjects\\dire.txt");
            BufferedReader b = new BufferedReader(new InputStreamReader(fin));
            String line = "";
            while ((line = b.readLine()) != null) {
                String[] lineArray =line.split(";");
                if (lineArray.length == 7) {
                    if (f3.equals(lineArray[5])) {                        
                        System.out.println("id = " + lineArray[0] + " , parentid = " + lineArray[1] + " , name = " + lineArray[2] + " , type = " + lineArray[3] + " , size = " + lineArray[4] + " , classification = " + lineArray[5] + " , checksum = " + lineArray[6]);
                    }
                }
            }
            fin.close();
        } catch (Exception e) {
            e.printStackTrace();
            System.out.println(e);
        }
        System.out.println("\n\n");
    }
}
