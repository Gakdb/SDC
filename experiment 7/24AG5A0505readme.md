// Define a package named Program-7
// A package is used to group related classes and interfaces.
package Program-7;

// Define a public class named LoginServlet
// This class will handle login functionality using servlets.
public class LoginServlet {

    // Importing necessary Java packages
    
    // java.io is used for input/output classes like PrintWriter
    import java.io.*;

    // javax.servlet is a package that contains classes and interfaces
    // for handling HTTP requests and responses in web applications
    import javax.servlet.*;

    // javax.servlet.http contains classes like HttpServlet, HttpServletRequest,
    // HttpServletResponse, Cookie, and HttpSession which are used to build web apps.
    import javax.servlet.http.*;

    // java.sql is used for database-related classes (not used directly in this snippet)
    import java.sql.*;

    // Define the LoginServlet class that extends HttpServlet
    // HttpServlet is a class provided by Java to handle HTTP-specific services
    public class LoginServlet extends HttpServlet {

        // This method will be automatically called when a POST request is sent to this servlet
        protected void doPost(HttpServletRequest request, HttpServletResponse response)
                throws ServletException, IOException {

            // Get the username parameter submitted through the HTML form
            // request.getParameter() is used to retrieve input field values from the form
            String username = request.getParameter("username");

            // Create a new session or get the existing one
            // A session is used to store information (like login info) across multiple requests
            HttpSession session = request.getSession(); // Starts or retrieves the session

            // Store the username in the session object
            // This allows the server to remember the user's identity during the session
            session.setAttribute("username", username);

            // Create a cookie to store the username in the client's browser
            // A cookie is a small piece of data stored on the client's side to maintain state
            Cookie userCookie = new Cookie("user", username); // Create cookie named "user" with value of username

            // Set the cookie's expiration time to 1 hour (in seconds)
            userCookie.setMaxAge(60 * 60); // 60 seconds * 60 minutes = 1 hour

            // Add the cookie to the response so it is sent back to the browser
            response.addCookie(userCookie);

            // Get a writer object to write HTML response back to the client
            PrintWriter out = response.getWriter(); // Used to write text-based output

            // Set the content type of the response to "text/html"
            // This tells the browser to interpret the response as HTML
            response.setContentType("text/html");

            // Write a personalized welcome message in HTML
            out.println("<h3>Welcome, " + username + "</h3>");

            // Provide a link to another servlet, TransactionServlet
            // This would take the user to their transaction history page
            out.println("<a href='TransactionServlet'>View Transaction History</a>");

            // End of doPost method
        }

        // End of LoginServlet class
    }

    // End of outer LoginServlet class (which is incorrectly enclosing everything)
}
