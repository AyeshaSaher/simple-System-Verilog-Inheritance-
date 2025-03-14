# simple-System-Verilog-Inheritance-example


// What is inheritance?
// Inhertance is concept that allows to the extend a child (sub/derived) class from parent (super) class
// and child class will have the access to all the properties and methods (Members) of the original class
// (parent class/super class) from the oobject of child/inherited/sub class.


class parent;
	int a;
	
	function void disp();
		$display("Parent : - class");
	endfunction: disp

endclass: parent

class child extends parent;
		
	function void print;
		$display("child:- class");
    endfunction: print
endclass: child

module test();
      initial begin 
	child c1;				// object of child class
	c1 = new();				// memory allocation to the child class object
	
	c1.print();				// calling the child class method using child class object
	c1.disp();				// calling parent class method 
	c1.a=10;
	
	$display("value of a =%d", c1.a);
       end
endmodule: test




https://edaplayground.com/x/YnSZ
