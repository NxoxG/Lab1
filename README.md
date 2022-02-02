# Lab1
CSCI1302

package pack;


	public class Box {

	public static void main(String[] args) {
	Box2 myBox2 = new Box2();
	
	Box2 yourBox2 = new Box2();
	Box2 ourBox2 = new Box2(5,7);
	
	ourBox2.printArea();
	ourBox2.square();
	
	java.util.Date date = new java.util.Date();
	
	System.out.println(date.toString());
	System.out.println(myBox2.numberOfBoxes);
	
	Box2 b1 = new Box2();
	
	System.out.println(b1.numberOfBoxes);
	
	Box2 b2 = new Box2();
	
	System.out.println(b2.numberOfBoxes);
	System.out.println(b1.numberOfBoxes);
	
	Box2 b3 = new Box2(2.0,5.0);
	Box2 b4 = new Box2(3.0,6.0);
	
	b4.square();
	b3.setBox(b4);
	b3.printArea();
	
	Box2[] boxArray = new Box2[5];
	
	Box2 b5 = new Box2(2,1);
	Box2 b6 = new Box2();
	Box2 b7 = new Box2();
	Box2 b8 = new Box2();
	Box2 b9 = new Box2();
	
	b5 = boxArray[0];
	b6 = boxArray[1];
	b7 = boxArray[2];
	b8 = boxArray[3];
	b9 = boxArray[4];
	
	System.out.println(boxArray.length);
	
	for (int i=0;i<5;i++) {
		boxArray[i] = new Box2(2,5);
		System.out.println(boxArray[i].length);
		}

	}
}

package pack;

public class Box2 {
	
		double length = 3;
		double width = 4;
		int box;
		static int numberOfBoxes = 0;
		char nameBox;
	Box2() {
		this.length = 5;
		numberOfBoxes ++;
	}
	Box2(double l, double w) {
		this.length = l;
		this.width = w;
	}
	private double getArea() {
		double area = length * width;
		return area;
	}
	public void printArea() {
		System.out.println(getArea());
	}
	public void square() {
		this.length = Math.pow(this.length, 2);
		System.out.println(getArea());
	}
	public void setBox(Box2 b) {
		this.length = b.length;
		this.width = b.width;
	}
}
