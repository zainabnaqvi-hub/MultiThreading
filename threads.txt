/*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */
package multithreading;

import java.util.logging.Level;
import java.util.logging.Logger;

/**
 *
 * @author DELL
 */
    class A extends Thread
    {
      
        @Override
       public void run()
      
          //     try {
             {
           for(int i= 0; i<5;i++)
           {
                 try {
               System.out.print("Mehdi Hassan");
                   sleep(1000);
               } catch (InterruptedException ex) {
                   Logger.getLogger(A.class.getName()).log(Level.SEVERE, null, ex);
               }
           }
       }
    }
public class MultiThreading {

    /**
     * @param args the command line arguments
     */

  
    public static void main(String[] args) throws InterruptedException  {
        // TODO code application logic here
        A t =new A();
        t.start();
        for(int i = 1; i<5;i++)
        {
            System.out.print("Kazmi");
            sleep(1000);
        }
    }

    private static void sleep(int i) {
        throw new UnsupportedOperationException("Not yet implemented");
    }
}
