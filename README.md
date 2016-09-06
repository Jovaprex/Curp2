# Curp2
1er Programa


/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package curp;

import java.util.Date;
import java.util.Scanner;

/**
 *
 * @author PROGRAMAR
 */
public class Curp2 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
    
    Scanner leer = new Scanner (System.in);
    
    String CURP, nombre;                                          //String normal no vector.
    int diferencia = 0, fecha = 2016, ingresos=0, prestamo=0, probabilidad=0;
    long cuenta;                                              //Variable
    java.util.Date hoy = new Date();                         //libreria para introducir fecha actual, no se usa todavia...
    
    
        System.out.println("Ingresar nombre:    ");
        nombre=leer.nextLine();
        System.out.println("Ingresar ingresos:  ");
        ingresos=leer.nextInt();
        System.out.println("Ingresar cuenta:    ");
        cuenta=leer.nextLong();
        System.out.println("Ingresar la CURP");         
        CURP = leer.next();
        
        prestamo = ingresos*2;
    
        if (CURP.length() == 18) {                           //validacion de curp
            System.out.println("***CURP valida***");
        }else{
            System.out.println("---CURP no valida---");
            System.exit(0);
        }
        
        String datos = CURP.substring(4, 10);               //guardar valor de datos
        String anio = datos.substring(0, 2);                // guardar año
        String mes = datos.substring(2, 4);                 //guardar mes
        String dia = datos.substring(4, 6);                 //guardar dia
        String sexo = CURP.substring(10,11);                //guardar sexo
        String nacimiento = CURP.substring(11, 12);         //guardar nacimiento
       
        int año = Integer.valueOf(anio);                    //conversion String a entero
        int mess = Integer.valueOf(mes);                    // mess = valor entero  // mes = String
        Integer diia = Integer.valueOf(dia);            
        
        if (año <= 16) {                                    //validar el rango de edad
            año = 2000+año;
        }else{
            año=1900+año;
        }
        
        
        
        if (año < 24) {
            
            System.out.println("Tu edad no cumple con el requisito de edad");
        
        }
        if (año >= 24 && año <=30) {
            
            probabilidad = 40;
            
        }
        if (año >= 31 && año <=40) {
         
            probabilidad = 30;
            
        }
         if (año >= 31 && año <=40) {
            
             probabilidad = 65;
             
        }
         if (año >= 41 && año <=50) {
            probabilidad=80;
        }
         if (año >50) {
            
             System.out.println("No se concede el credito");
        }
         
        if (sexo == "h" && sexo == "H") {                   //No cambia el h * hombre
            
           sexo = "Hombre";
           
        }else{
            if (sexo == "m" && sexo == "M") {
                
                sexo = "Mujer";
                
            }
        }
        
        switch (mess) {                                     //Opcion 1
            case 1:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "enero";
                break;
            case 2:
                if ( diia<=28 ) {
                    diia= diia;
                }
                mes = "febrero";
                break;
            case 3:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "marzo";
                break;
            case 4:
                if ( diia<=30 ) {
                    diia= diia;
                }
                mes = "abril";
                break;
            case 5:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "mayo";
                break;
            case 6:
                if ( diia<=30) {
                    diia= diia;
                }
                mes = "junio";
                break;
            case 7:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "julio";
                break;
            case 8:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "agosto";
                break;
            case 9:
                if ( diia<=30 ) {
                    diia= diia;
                }
                mes = "septiembre";
                break;
            case 10:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "octubre";
                break;
            case 11:
                if ( diia<=30) {
                    diia= diia;
                }
                mes = "nombiembre";
                break;
            case 12:
                if ( diia<=31 ) {
                    diia= diia;
                }
                mes = "diciembre";
                break;
            default:
                throw new AssertionError("Mes erroneo");
                
        }
        
        int acdia =  03
          , acmes =  8, 
            acaño=   2016,
            diferencia2=1;
       
        diferencia = fecha - año;   //Operacion de edad = 20
        
        if (mess <= acmes) {
            
        }else{
            if (mess >= acmes) {
                diferencia= diferencia-diferencia2;
            }
        }
        
        
        System.out.println("Nombre: "+nombre);
        System.out.println("Edad:   "+diferencia);
        System.out.println("Mes:    "+mes);
        System.out.println("Dia:    "+diia);
        System.out.println("Sexo:   "+sexo);
        System.out.println("Ingresos:   "+ingresos);
        System.out.println("Cuenta: "+cuenta);
        
        
        
    }
}  

    
