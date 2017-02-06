/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package firstpartialexercises;

/**
 *
 * @author jaime
 */
public class MyPoint {
      //Declration of atributes
    private int x;
    private int y;
    //Initialize atributes
    public MyPoint(){ //default vaules 
        this.x = 0; 
        this.y = 0; 
    }
    public MyPoint(int x, int y){
        this.x = x;
        this.y = y;
    }
    //Getters and setters
    public int getX(){
        return this.x;
    }
    public void setX(int x){
        this.x = x;
    }
    public int getY(){
        return this.y;
    }
    public void setY(int y){
        this.y = y;
    }
    public int[] getXY(){ //create an array (x,y)
        int[] XY = new int[2];
        XY[0]=this.x;
        XY[1]=this.y;
        return XY;
    }
    public void setXY(int x, int y){
        this.x = x;
        this.y = y;
    }
    @Override
    public String toString(){ //return String
        return "{" + this.x + "," + this.y + "}";
    }
    public double distance(int x, int y){ 
        return Math.sqrt((Math.pow(this.x-x,2))+(Math.pow(this.y-y,2)));
    }
    public double distance(MyPoint another){ 
        return Math.sqrt((Math.pow(this.x-another.getX(),2))+(Math.pow(this.y-another.getY(),2)));
    }
    public double distance(){ 
        return Math.sqrt((Math.pow(this.x,2))+(Math.pow(this.y,2)));
    }
}
