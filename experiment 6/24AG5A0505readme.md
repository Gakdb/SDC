 <%@ page import="java.sql.*" %>  
 <database visuals ![Alt Text](C:\Users\Haji\Pictures\Saved Pictures)
>
<%-- Importing the java.sql package to use JDBC classes like ResultSet, Connection, etc. --%>

<h2>Product Catalog</h2>  
<%-- Heading for the page that displays the product catalog --%>

<table border="1">  
<%-- Creating an HTML table with borders to display product data --%>

<tr><th>ID</th><th>Name</th><th>Price</th><th>Add</th></tr>  
<%-- Table header row with 4 columns: ID, Name, Price, and Add to Cart option --%>

<%  
  // Getting the ResultSet object from the request attributes  
  // This ResultSet contains the list of products fetched from the database  
  ResultSet rs = (ResultSet) request.getAttribute("products");  

  // Iterating over each row of the ResultSet  
  while(rs.next()) {  
%>

<tr>  
  <%-- Starting a new table row for each product --%>

  <td><%= rs.getInt("id") %></td>  
  <%-- Displaying the product ID from the ResultSet using getInt() --%>

  <td><%= rs.getString("name") %></td>  
  <%-- Displaying the product name using getString() --%>

  <td><%= rs.getDouble("price") %></td>  
  <%-- Displaying the product price using getDouble() --%>

  <td>  
    <%-- Creating a form for the 'Add to Cart' button inside this cell --%>

    <form action="AppController" method="post">  
    <%-- When the user clicks submit, the form data is sent to "AppController" servlet using POST method --%>

      <input type="hidden" name="action" value="addToCart">  
      <%-- Hidden field that sends the action to be performed (addToCart) --%>

      <input type="hidden" name="userId" value="1">  
      <%-- Hidden field for user ID; here it's hardcoded as "1" for demonstration purposes --%>
      <%-- In a real application, this should be dynamic (from session or login data) --%>

      <input type="hidden" name="productId" value="<%= rs.getInt("id") %>">  
      <%-- Hidden field that sends the current product's ID to the controller --%>

      <input type="submit" value="Add to Cart">  
      <%-- Submit button labeled "Add to Cart" --%>

    </form>  

  </td>  
</tr>  
<%  
  // Closing the while loop - after displaying one product row, move to the next
  }  
%>

</table>  
<%-- Closing the HTML table --%>
