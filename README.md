class MyClass{
private int a;
public MyClass(){
System.out.println("Default Constructor");
}
public MyClass(int value){
a = value;
System.out.println("Parameterized Constructor and value is "+a);
}
public MyClass(MyClass other){
a = other.a;
System.out.println("Copy Constructor and value is "+a);
}}
public class Pr{
public static void main(String[] args){
MyClass obj1 = new MyClass();
MyClass obj2 = new MyClass(7);
MyClass obj3 = new MyClass(obj2);
}}


class OperOver{
public int add(int a, int b){
return a+b;
}
public int add(int a, int b, int c){
return a+b+c;
}
}
public class Pr1b{
public static void main(String[] args){
OperOver obj = new OperOver();
int sum1 = obj.add(13,14);
int sum2 = obj.add(13,14,18);
System.out.println("Sum of two integers: "+sum1);
System.out.println("Sum of three integers: "+sum2);
}}

class DemoStaticMethods{
public static int add(int a, int b){
return a+b;
}
public static int subtract(int a, int b){
return a-b;
}}
public class Pr1c{
public static void main(String[] args){
int sum = DemoStaticMethods.add(14,13);
int difference = DemoStaticMethods.subtract(29,15);
System.out.println("Sum: "+sum);
System.out.println("Difference: "+difference);
}}

class A{
void show(){
System.out.println("Base Class");
}}
class B extends A{
void show(){
System.out.println("Derived Class");
}}
class Pr2a{
public static void main(String args[]){
B s = new B();
s.show();
}}


abstract class Shape{
public abstract double area();
}
class Circle extends Shape{
private double radius;
public Circle(double radius){
this.radius = radius;
}
@Override
public double area(){
return Math.PI*radius*radius;
}}
public class Pr2b{
public static void main(String[] args){
Circle circle = new Circle(20.0);
System.out.println("Circle Area: "+circle.area());
}}


import javax.swing.*;
import java.awt.*;
public class DemoFlowLayout{
	public static void main(String[] args){
		JFrame frame = new JFrame("FlowLayout Example");
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setSize(300, 100);

		JPanel panel = new JPanel(new FlowLayout(FlowLayout.RIGHT));

		JButton button1 = new JButton("Button 1");
		JButton button2 = new JButton("Button 2");
		JButton button3 = new JButton("Button 3");

		panel.add(button1);
		panel.add(button2);
		panel.add(button3);

		frame.add(panel);
		frame.setVisible(true);
}}


import javax.swing.*;
import java.awt.*;
public class DemoGridLayout{
	public static void main(String[] args){
		JFrame frame = new JFrame("GridLayout Example");
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setSize(300, 100);
		JPanel panel = new JPanel(new GridLayout(2, 3));
		JButton button1 = new JButton("Button 1");
		JButton button2 = new JButton("Button 2");
		JButton button3 = new JButton("Button 3");
		JButton button4 = new JButton("Button 4");
		JButton button5 = new JButton("Button 5");
		JButton button6 = new JButton("Button 6");
		panel.add(button1);
		panel.add(button2);
		panel.add(button3);
		panel.add(button4);
		panel.add(button5);
		panel.add(button6);
		frame.add(panel);
		frame.setVisible(true);
}}


import javax.swing.*;
import java.awt.*;
public class DemoBorderLayout{
	public static void main(String[] args){
		JFrame frame = new JFrame("BorderLayout Example");
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setSize(300, 100);
		JButton northButton = new JButton("North");
		JButton southButton = new JButton("South");
		JButton eastButton = new JButton("East");
		JButton westButton = new JButton("West");
		JButton centerButton = new JButton("Center");
		Container contentPane = frame.getContentPane();
		contentPane.setLayout(new BorderLayout());
		contentPane.add(northButton, BorderLayout.NORTH);
		contentPane.add(southButton, BorderLayout.SOUTH);
		contentPane.add(eastButton, BorderLayout.EAST);
		contentPane.add(westButton, BorderLayout.WEST);
		contentPane.add(centerButton, BorderLayout.CENTER);
		frame.setVisible(true);
}}


import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class BtnClkDemo{
public static void main(String[] args){
JFrame frame=new JFrame("S037 Abhay Sharma");
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
JButton button=new JButton("Click Me");
button.addActionListener(new ActionListener(){
@Override
public void actionPerformed(ActionEvent e){
JOptionPane.showMessageDialog(frame,"Button Clicked");
}});
frame.getContentPane().add(button);
frame.pack();
frame.setVisible(true);
}}


import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class MenuItmClk{
public static void main(String[] args){
JFrame frame=new JFrame("S037 Abhay Sharma");
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
JMenuBar menuBar=new JMenuBar();
JMenu fileMenu=new JMenu("File");
JMenuItem openItem=new JMenuItem("Open");
openItem.addActionListener(new ActionListener(){
@Override
public void actionPerformed(ActionEvent e){
JOptionPane.showMessageDialog(frame,"File->Open Clicked!");
}});
fileMenu.add(openItem);
menuBar.add(fileMenu);
frame.setJMenuBar(menuBar);
frame.setSize(400,300);
frame.setVisible(true);
}}


import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class TxtEnterKey{
public static void main(String[] args){
JFrame frame=new JFrame("S037 Abhay Sharma");
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
JTextField textField=new JTextField(20);
textField.addActionListener(new ActionListener(){
@Override
public void actionPerformed(ActionEvent e){
JOptionPane.showMessageDialog(frame,"Enter key pressed in text field");
}});
frame.getContentPane().add(textField);
frame.pack();
frame.setVisible(true);
}}
