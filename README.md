# Proyecto-TIC-TAC-TOE
Método que permite al usuario jugar tic tac toe
package lab25;

import javax.swing.JOptionPane;

//int m [filas][columnas]

    public class Matrices {
        
    public int sumatoriaMatriz(int p[][]){
        
        int sumatoria=0;

        for(int f=0;f<p.length;f++)
            for(int c=0;c<p[0].length;c++)
                sumatoria+=p[f][c];
        return sumatoria;
    }//Fin sumatoriaMatriz
    
    public double [][] llenoMatriz(){
        
        int cantidadEstudiantes = Integer.parseInt(JOptionPane.showInputDialog("Ingrese los estudiantes a registrar"));
        int cantidadNotas = Integer.parseInt(JOptionPane.showInputDialog("Ingrese las notas a registrar"));
        
        double notas [][] = new double[cantidadEstudiantes][cantidadNotas+1];
        
        for(int f=0; f<notas.length;f++)
            for(int c=0; c<notas[0].length-1;c++)
        notas[f][c]=Double.parseDouble(JOptionPane.showInputDialog("Ingrese nota " + (c+1) + " del estudiante" + (f+1)));
        
        return notas;

    }//Fin llenoMatriz
    
    public String imprimeMatriz (double m [][]){
        
        String salida="";
        for(int f=0; f<m.length;f++){
            salida+="Las notas del estudiante " + (f+1) + " son ";
            for(int c=0; c<m[0].length-1;c++)
                salida+=m[f][c]+ " ";       
                
            salida+="\n y el promedio del estudiante es : " +m[f][m[0].length-1]+"\n";
        }//Fin for
        
        return salida;
    }//Fin imprimeMatriz
    
    public double [][] promedioEstud (double a[][]){
        double suma, promedio=0; 
        for (int f=0; f<a.length; f++){
            suma=0;
            for (int c=0; c<a[0].length-1; c++)
                suma+=a[f][c];
            promedio=suma/(a[0].length-1);
            a[f][a[0].length-1]=promedio;

        }//Fin for
        
            return a;
        
    }//Fin promedioEstud
    
}//Fin Matrices
