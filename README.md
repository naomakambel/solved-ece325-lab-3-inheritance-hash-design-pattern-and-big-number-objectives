Download Link: https://assignmentchef.com/product/solved-ece325-lab-3-inheritance-hash-design-pattern-and-big-number-objectives
<br>
Inheritance, Hash, Design Pattern and Big Number Objectives

1.1 Inheritance in Java

<table width="42">

 <tbody>

  <tr>

   <td width="42">Person</td>

  </tr>

 </tbody>

</table>

Different kinds of objects often have a certain amount in common with each other. Employees, customers, and managers, for example, all share the characteristics of a person (name, etc.). Yet each also defines additional features that make it different. Object-oriented programming allows such different classes to inherit commonly used state and behavior from other classes. In this example,  is the superclass of

Employee and Customer; Employee is the super class ofSwEngineer and HwEngineer; SwEngineer is the superclass of <sub>ProjectManager</sub>.

In Java, each class is allowed to <strong>have and only have one direct superclass</strong>, and each superclass has the potential for an unlimited number of subclasses. A subclass contains all the methods (functions) and attributes (variables) defined in the superclass plus the subclass’s own methods and variables.

<table width="48">

 <tbody>

  <tr>

   <td width="48">extends</td>

  </tr>

 </tbody>

</table>

Java implements inheritance through the  keyword.

Example: a software engineer has all the attributes of an employee plus attributes picked up from a person, which means the software engineer is an employee, and an employee is a person, and therefore the software engineer is also a person. In Java we would represent this as:

<strong>class</strong> <strong>SwEngineer</strong> <strong>extends</strong> Employee <strong>class</strong> <strong>Employee</strong> <strong>extends</strong> Person

<table width="569">

 <tbody>

  <tr>

   <td width="68">SwEngineer</td>

   <td width="293"> gets all the attributes and methods defined in:</td>

   <td width="68">SwEngineer</td>

   <td width="10">,</td>

   <td width="55">Employee</td>

   <td width="34"> and</td>

   <td width="42">Person</td>

  </tr>

 </tbody>

</table>

By doing so, .

<table width="292">

 <tbody>

  <tr>

   <td width="42">public</td>

   <td width="6"><u>/</u></td>

   <td width="48">private</td>

   <td width="147">. An attribute is usually</td>

   <td width="48">private</td>

  </tr>

 </tbody>

</table>

NOTE: A method is usually , meaning that it cannot be

directly accessed outside of the class. A “getter” and “setter” method enables such access. For example:

Person person <strong>=</strong> <strong>new</strong> Person<strong>();</strong> person<strong>.</strong>setName<strong>(</strong>“John Doe”<strong>);</strong> <strong>int</strong> age <strong>=</strong> person<strong>.</strong>getAge<strong>();</strong>

<h2>1.2  Interface</h2>

Interfaces define a standardized set of commands that a class will obey. The commands are a set of methods. The interface definition states: the names of the methods; the return types; and the signatures (argument lists). There is no executable body for any method. The body is left to each class to implement.

A class can implement <strong>multiple interfaces</strong>. Once a class implements an interface, you are able to invoke the corresponding method. That is, implementing an interface enables a class to be “plugged in” to any situation that requires a specific behavior (manifested through the set of methods).

<table width="691">

 <tbody>

  <tr>

   <td width="255">Java implements interface through the</td>

   <td width="68">implements</td>

   <td width="367"> keyword.</td>

  </tr>

  <tr>

   <td colspan="3" width="691"><strong>interface</strong> <strong>SalaryRaisable</strong> <strong>{</strong>     <strong>public</strong> <strong>double</strong> <strong>RaiseSalary</strong><strong>();</strong><strong>}</strong><strong>class</strong> <strong>Employee</strong> <strong>implements</strong> SalaryRaisable <strong>{</strong>     <strong>double</strong> baseSalary<strong>;</strong>@Override<strong>public</strong> <strong>double</strong> <strong>RaiseSalary</strong><strong>()</strong> <strong>{</strong>         <strong>return</strong> baseSalary <strong>*=</strong> 1.2<strong>;</strong><strong>}</strong><strong>}</strong></td>

  </tr>

 </tbody>

</table>

<h1>2  Deliverable 1 — Inheritance and Interfaces</h1>

In this part you will write a program to represent people who are involved in a software production company (name, department, related projects…), as mentioned at the beginning of this lab.

<em>Step 1: create classes </em>

Please refer to the following <a href="https://en.wikipedia.org/wiki/Class_diagram"><em>UML class diagram</em></a><a href="https://en.wikipedia.org/wiki/Class_diagram">.</a> Your program will <strong>only</strong> have the classes and interfaces

<table width="253">

 <tbody>

  <tr>

   <td width="253">public static void main(String[] args)</td>

  </tr>

 </tbody>

</table>

mentioned in the diagram (you can put the main entry  and test

<table width="669">

 <tbody>

  <tr>

   <td rowspan="2" width="324">cases anywhere you like), where the two interfacesAlso, your classes will <strong>only</strong> have the attributes and methods menti</td>

   <td width="61">


    <table width="59">

     <tbody>

      <tr>

       <td width="59">Printable</td>

      </tr>

     </tbody>

    </table></td>

   <td rowspan="2" width="34"> and</td>

   <td width="94">


    <table width="92">

     <tbody>

      <tr>

       <td width="92">SalaryRaisable</td>

      </tr>

     </tbody>

    </table></td>

   <td rowspan="2" width="156"> are already provided. </td>

  </tr>

  <tr>

   <td width="61"> </td>

   <td width="94">oned in the diagram.</td>

  </tr>

 </tbody>

</table>

<table width="35">

 <tbody>

  <tr>

   <td width="35">super</td>

  </tr>

 </tbody>

</table>

<strong>HINT</strong>: You can use  to call the constructor of the super class.

<table width="74">

 <tbody>

  <tr>

   <td width="74">RaiseSalary</td>

  </tr>

 </tbody>

</table>

The  method raises the salary in a certain rate and returns the raised salary amount:

<strong>Role                                                                                   Rate </strong>

<table width="68">

 <tbody>

  <tr>

   <td width="68">HwEngineer</td>

  </tr>

 </tbody>

</table>

0.18

<table width="75">

 <tbody>

  <tr>

   <td width="75">ProjManager</td>

  </tr>

 </tbody>

</table>

0.24

<table width="430">

 <tbody>

  <tr>

   <td width="68">HwEngineer</td>

   <td width="287"> with base salary of $3000, and an instance of</td>

   <td width="75">ProjManager</td>

  </tr>

 </tbody>

</table>

Create an instance of  with base salary of $6000. Display their final (raised) salaries — they should be different.




<table width="691">

 <tbody>

  <tr>

   <td width="691">                    <strong>————————–</strong><strong>|</strong>        Person          <strong>|</strong><strong>————————–</strong><strong>|</strong> <strong>–</strong> name<strong>:</strong> String         <strong>|</strong><strong>|————————-</strong><strong>|</strong> <strong>+</strong> Person<strong>(</strong>name<strong>:</strong> String<strong>)</strong> <strong>|</strong><strong>|</strong> <strong>+</strong> getName<strong>():</strong> String    <strong>|</strong><strong>————————–</strong><strong>^</strong>     <strong>^</strong><strong>extends</strong>  <strong>|</strong>     <strong>|</strong>   <strong>extends</strong>                 <strong>+————-</strong>     <strong>————-+</strong><strong>|</strong>                               <strong>|</strong><strong>—————————–</strong>    <strong>—————————-</strong>  <strong>implements</strong>   <strong>——————–</strong><strong>|</strong>         Employee          <strong>|</strong>    <strong>|</strong>         Customer         <strong>|</strong> <strong>————&gt;</strong> <strong>|</strong>   <strong>&lt;&lt;</strong>interface<strong>&gt;&gt;</strong>  <strong>|</strong><strong>—————————–</strong>    <strong>—————————-</strong>               <strong>|</strong>    Printable     <strong>|</strong><strong>|</strong> <strong>–</strong> baseSalary<strong>:</strong> <strong>double</strong>      <strong>|</strong>    <strong>|</strong> <strong>–</strong> projPrice<strong>:</strong> <strong>double</strong>      <strong>|</strong>   <strong>+———&gt;</strong> <strong>——————–</strong><strong>|—————————|</strong>    <strong>—————————-</strong>   <strong>|</strong>           <strong>|</strong> <strong>+</strong> PrintInfo<strong>():</strong>   <strong>|</strong><strong>|</strong> <strong>+</strong> Employee<strong>(</strong>               <strong>|</strong>    <strong>|</strong> <strong>+</strong> Customer<strong>(</strong>              <strong>|</strong>   <strong>|</strong>           <strong>|</strong>     String       <strong>|</strong><strong>|</strong>     name<strong>:</strong> String<strong>,</strong>         <strong>|</strong>    <strong>|</strong>     name<strong>:</strong> String<strong>,</strong>        <strong>|</strong>   <strong>|</strong>           <strong>——————–</strong><strong>|</strong>     baseSalary<strong>:</strong> <strong>double</strong><strong>)</strong>   <strong>|</strong>    <strong>|</strong>     projPrice<strong>:</strong> <strong>double</strong><strong>)</strong>   <strong>|</strong>   <strong>|</strong><strong>|</strong> <strong>+</strong> getBaseSalary<strong>():</strong> <strong>double</strong> <strong>|</strong>    <strong>|</strong> <strong>+</strong> getProjPrice<strong>():</strong> <strong>double</strong> <strong>|</strong>   <strong>|</strong><strong>—————————–</strong>    <strong>—————————-</strong>   <strong>|</strong>             <strong>^</strong>     <strong>^</strong>                                               <strong>|</strong>     <strong>extends</strong> <strong>|</strong>     <strong>|</strong>          <strong>extends</strong>                              <strong>|</strong>             <strong>|</strong>     <strong>+—————————–+</strong>                 <strong>|</strong><strong>|</strong>                                   <strong>|</strong>                 <strong>|</strong><strong>—————————–</strong>    <strong>—————————-</strong>   <strong>|</strong><strong>|</strong>         SwEngineer        <strong>|</strong>    <strong>|</strong>        HwEngineer        <strong>|</strong> <strong>——+</strong><strong>—————————–</strong>    <strong>—————————-</strong>   <strong>|</strong>   <strong>|</strong><strong>|</strong> <strong>–</strong> projName<strong>:</strong> String        <strong>|</strong>    <strong>|</strong>                          <strong>|</strong>   <strong>|</strong>   <strong>|</strong><strong>|—————————|</strong>    <strong>—————————-</strong>   <strong>|</strong>   <strong>|</strong><strong>|</strong> <strong>+</strong> SwEngineer<strong>(</strong>             <strong>|</strong>    <strong>|</strong> <strong>+</strong> HwEngineer<strong>(</strong>            <strong>|</strong>   <strong>|</strong>   <strong>|</strong><strong>|</strong>     name<strong>:</strong> String<strong>,</strong>         <strong>|</strong>    <strong>|</strong>     name<strong>:</strong> String<strong>,</strong>        <strong>|</strong>   <strong>|</strong>   <strong>|</strong> <strong>implements</strong><strong>|</strong>     baseSalary<strong>:</strong> <strong>double</strong><strong>,</strong>   <strong>|</strong>    <strong>|</strong>     baseSalary<strong>:</strong> <strong>double</strong><strong>)</strong>  <strong>|</strong>   <strong>|</strong>   <strong>|</strong><strong>|</strong>     projName<strong>:</strong> String<strong>)</strong>     <strong>|</strong>    <strong>|</strong>                          <strong>|</strong>   <strong>|</strong>   <strong>|</strong><strong>|</strong> <strong>+</strong> getProjName<strong>():</strong> String   <strong>|</strong>    <strong>|</strong>                          <strong>|</strong>   <strong>|</strong>   <strong>|</strong><strong>—————————–</strong>    <strong>—————————-</strong>   <strong>|</strong>   <strong>|</strong><strong>^</strong>                                                     <strong>|</strong>   <strong>|</strong><strong>|</strong> <strong>extends</strong>                                             <strong>|</strong>   <strong>|</strong><strong>—————————–</strong>             <strong>implements</strong>            <strong>|</strong>   <strong>|</strong>       <strong>——————–</strong><strong>|</strong>        ProjManager        <strong>|</strong> <strong>———————————-+</strong>   <strong>+—–&gt;</strong> <strong>|</strong>  <strong>&lt;&lt;</strong>interface<strong>&gt;&gt;</strong>   <strong>|</strong><strong>—————————–</strong>                                               <strong>|</strong>  SalaryRaisable  <strong>|</strong><strong>|</strong> <strong>–</strong> projDeadline<strong>:</strong> Date      <strong>|</strong> <strong>——————————————–&gt;</strong> <strong>——————–</strong><strong>|—————————|</strong>             <strong>implements</strong>                        <strong>|</strong> <strong>+</strong> RaiseSalary<strong>():</strong> <strong>|</strong><strong>|</strong> <strong>+</strong> ProjManager<strong>(</strong>            <strong>|</strong>                                               <strong>|</strong>     <strong>double</strong>       <strong>|</strong>   <strong>|</strong>     name<strong>:</strong> String<strong>,</strong>         <strong>|</strong>                                               <strong>——————–</strong><strong>|</strong>     baseSalary<strong>:</strong> <strong>double</strong><strong>,</strong>   <strong>|</strong><strong>|</strong>     projName<strong>:</strong> String<strong>,</strong>     <strong>|</strong><strong>|</strong>     projDeadline<strong>:</strong> Date<strong>)</strong>   <strong>|</strong><strong>|</strong> <strong>+</strong> getProjDeadline<strong>():</strong> Date <strong>|</strong><strong>—————————–</strong></td>

  </tr>

 </tbody>

</table>

<table width="61">

 <tbody>

  <tr>

   <td width="61"><em>PrintInfo</em></td>

  </tr>

 </tbody>

</table>

<em>Step 3: implement  </em>

The printed information shall be:

<table width="75">

 <tbody>

  <tr>

   <td width="55">Customer</td>

   <td width="20">:</td>

  </tr>

  <tr>

   <td colspan="2" width="75">ProjManager</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>name + project price;</li>

 <li>: name + project name + final salary + project deadline.</li>

</ul>

<strong>DEMO this deliverable to the lab instructor (10 points).</strong>

<h1>3  Deliverable 2 — equals and hashCode</h1>

Comparison is a common activity, hence nearly every class has its own definition of equals and hashCode.

<table width="176">

 <tbody>

  <tr>

   <td width="68">SwEngineer</td>

   <td width="34"> and</td>

   <td width="75">ProjManager</td>

  </tr>

 </tbody>

</table>

Override the two methods for . Your implementations must follow the best practice as discussed in the lecture.

<table width="262">

 <tbody>

  <tr>

   <td width="41">equals</td>

   <td width="166">, you still need to override</td>

   <td width="55">hashCode</td>

  </tr>

 </tbody>

</table>

<strong>Note 1</strong>: even if you only need a customized  — this is important.

<table width="130">

 <tbody>

  <tr>

   <td width="41">equals</td>

   <td width="34"> and</td>

   <td width="55">hashCode</td>

  </tr>

 </tbody>

</table>

<strong>Note 2</strong>: if you override  of a subclass, you may need to override the superclass, too.

This is because the hash code of the subclass relies on that of its superclass.

<strong>DEMO this deliverable to the lab instructor (5 points).</strong>

<h1>4  Deliverable 3 — Java Design Pattern</h1>

Consider the code from <em>JavaDPExample.java</em> and provide answers to these questions (google useful clues if you need):

<ol>

 <li>Why do we use a static method in this situation?</li>

 <li>The code implements a class-level (involving multiple classes) programming “good practice”, commonly these practices are called design patterns in Java. Which design pattern is implemented?</li>

 <li>Explain why this is considered a good practice.</li>

</ol>

<strong>DISCUSS this deliverable with the lab instructor (5 points).</strong>

<h1>5  Deliverable 4 — Big Numbers</h1>

Consider the following piece of C code. What is it doing? Convert it into Java codes.

<strong>uint64_t</strong> <strong>fnv</strong>(<strong>void</strong> <strong>*</strong>b, <strong>int</strong> c) {     <strong>unsigned</strong> <strong>char</strong> <strong>*</strong>p <strong>=</strong> b;

<strong>uint64_t</strong> h <strong>=</strong> 14695981039346656037;     <strong>int</strong> i;

<strong>for</strong> (i <strong>=</strong> 0; i <strong>&lt;</strong> c; i<strong>++</strong>)         h <strong>=</strong> (h <strong>*</strong> 1099511628211) <strong>^</strong> p[i];     <strong>return</strong> h; }

<table width="394">

 <tbody>

  <tr>

   <td width="28">long</td>

   <td width="309">, because Java doesn’t have unsigned version of</td>

   <td width="22">int</td>

   <td width="6"><u>/</u></td>

   <td width="28">long</td>

  </tr>

 </tbody>

</table>

<table width="68">

 <tbody>

  <tr>

   <td width="68">BigInteger</td>

  </tr>

 </tbody>

</table>

<strong>Hint 1</strong>: <sub>h</sub> is too big even for . So you may need .

<strong>Hint 2</strong>: ^ in C is “bitwise XOR”, not Math.pow.

<strong>Hint 3</strong>: Don’t forget the overflow of higher bits, or you may get incredibly large number. Such number is incorrect, and what’s more, it may crash Eclipse.