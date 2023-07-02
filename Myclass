package project1;

import java.sql.*;

import java.util.Scanner;



public class Myclass{

    public static void main(String args[]) {

    	Scanner sc = new Scanner(System.in);

        try{

            Connection connect = DriverManager.getConnection("jdbc:mysql://localhost:3306/shizu", "root", "root");

            Statement st = connect.createStatement();

            System.out.println("Database Configure:");

            System.out.println("Enter your Option:\n1.Update\n2.Delete\n3.Insert\n4.show\nAny other choice to exit");

            int Option = sc.nextInt();

            while(Option == 1 || Option == 2 || Option ==3 || Option == 4) {

                switch(Option) {

                    case 1:

                        System.out.println("Choose the column to update:\n1.Admit_no\n2.NAME\n3.Doj\n4.Blood_group\n5.Ward\n6.Gender\n7.Result\nAny other choice to complete your update");

                        int Option1 = sc.nextInt();

                        while (Option1 == 1 || Option1 == 2 || Option1 == 3||Option1 == 4||Option1==5||Option1==6||Option1==7) {

                            switch (Option1) {

                                case 1:

                                    System.out.println("Enter the value;");

                                    int a = sc.nextInt();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int b = sc.nextInt();

                                    st.executeUpdate("update patient set Admit_no = " + a + " where Admit_no = " + b);

                                    break;

                                case 2:

                                    System.out.println("Enter the value");

                                    sc.nextLine();

                                    String c = sc.nextLine();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int d = sc.nextInt();

                                    st.executeUpdate("update  patient set NAME = '" + c + "' where Admit_no = " + d);

                                    break;

                                case 3:

                                    System.out.println("Enter the value;");

                                    sc.nextLine();

                                    String e = sc.nextLine();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int f = sc.nextInt();

                                    st.executeUpdate("update  patient set Doj = '" + e + "' where Admit_no = " + f);

                                    break;

                                      case 4:

                                    System.out.println("Enter the value;");

                                    sc.nextLine();

                                    String g = sc.nextLine();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int h = sc.nextInt();

                                    st.executeUpdate("update  patient set Blood_group = '" + g + "' where Admit_no = " + h);

                                    break;

                                      case 5:

                                    System.out.println("Enter the value;");

                                    sc.nextLine();

                                    String i = sc.nextLine();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int j = sc.nextInt();

                                    st.executeUpdate("update  patient set Ward = '" + i + "' where Admit_no = " + j);

                                    break;

                                      case 6:

                                    System.out.println("Enter the value;");

                                    sc.nextLine();

                                    String k = sc.nextLine();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int l = sc.nextInt();

                                    st.executeUpdate("update  patient set Gender = '" + k + "' where Admit_no = " + l);

                                    break;

                                      case 7:

                                    System.out.println("Enter the value;");

                                    sc.nextLine();

                                    String m = sc.nextLine();

                                    System.out.println("Where you want to update(Admit_no)");

                                    int n = sc.nextInt();

                                    st.executeUpdate("update  patient set Result = '" + m + "' where Admit_no = " + n);

                                    break;

                            }

                            System.out.println("Updated Successfully");

                            System.out.println("Choose the column to update:\n1.Admit_no\n2.NAME\n3.Doj\n4.Blood_group\n5.Ward\n6.Gender\n7.Result\nAny other choice to complete your update");

                            Option1 = sc.nextInt();

                        }

                        break;

                    case 2:

                        System.out.println("Enter the number of Stuart you want to remove");

                        int x = sc.nextInt();

                        st.executeUpdate("delete from  patient where Admit_no = " + x);

                        System.out.println("Row Deleted Successfully");

                        break;

                    case 3:

                        System.out.println("Enter the number of Stuart");

                        int Admit_no1 = sc.nextInt();

                        System.out.println("Enter the name of Stuart");

                        sc.nextLine();

                        String name1 = sc.nextLine();

                        System.out.println("Enter the doj of Stuart");

                        int Doj1 = sc.nextInt();

                        System.out.println("Enter the Blood_group of Stuart");

                        String Blood_group1 = sc.nextLine();

                        System.out.println("Enter the Ward of Stuart");

                        String Ward1 = sc.nextLine();

                        System.out.println("Enter the Gender of Stuart");

                        String Gender1 = sc.nextLine();

                        System.out.println("Enter the Result of Stuart");

                        String Result1 = sc.nextLine();

                        String query = "insert into  patient (ADMIT_NO, NAME, DOJ,BLOOD_GROUP,WARD,GENDER,RESULT) values (" + Admit_no1 + ", '" + name1 + "','" + Doj1 + ",'" + Blood_group1 +",'" +  Ward1 +",'" + Gender1 +",'"+ Result1 + "')";

                        st.executeUpdate(query);

                        System.out.println("Successfully Inserted");

                        break;

                    case 4:

                        ResultSet rs = st.executeQuery("select * from  patient");

                       // System.out.println(rs);

                       System.out.println("ADMIT_NO     NAME        DOJ      BLOOD_GROUP     WARD     GENDER     RESULT");

                        while(rs.next()) {

                        int admit_no = rs.getInt("ADMIT_NO");

                        String name = rs.getString("NAME");

                        String doj = rs.getString("DOJ");

                        String blood_group = rs.getString("BLOOD_GROUP");

                        String ward = rs.getString("WARD");

                        String gender = rs.getString("GENDER");

                        String result = rs.getString("RESULT");

                        System.out.println(admit_no + "      " + name + "      " + doj+"        "+blood_group+"      "+ward+"         "+gender+"       "+result+"     ");

                        }

                        break;

                }

                System.out.println("Enter your choice:\n1.Update\n2.Delete\n3.Insert\n4.Show\nAny other choice to exit");

                Option = sc.nextInt();

            }

            connect.close();

            st.close();

        }

        catch (Exception e) {

            System.out.println(e.toString());

        }

    }

} 
