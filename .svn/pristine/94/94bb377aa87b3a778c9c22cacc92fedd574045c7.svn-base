package com.wilson.servlets;

import java.io.IOException;
import java.util.List;

import javax.ejb.EJB;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

import com.wilson.beans.MeuPrimeiroBeanLocal;
import com.wilson.model.Person;

/**
 * Servlet implementation class MeuServlet
 */
@WebServlet("/MeuServlet")
public class MeuServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
	
	@EJB
    private MeuPrimeiroBeanLocal meuBean;
       
    /**
     * @see HttpServlet#HttpServlet()
     */
    public MeuServlet() {
        super();
        // TODO Auto-generated constructor stub
    }

	/**
	 * @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response)
	 */
    @Override
	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
    	meuBean.helloWorld();
    	List<Person> lista =  meuBean.listPersons();
		for (Person p: lista) {
			System.out.println("ID: " +p.getId());
			System.out.println("Name: " +p.getName());
			System.out.println("Country: " +p.getCountry());
			System.out.println(" / ");
		}
		response.getWriter().append("Served at: ").append(request.getContextPath());
	}

	/**
	 * @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response)
	 */
    @Override
	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
		meuBean.helloWorld();
		List<Person> lista =  meuBean.listPersons();
		for (Person p: lista) {
			System.out.println("ID: " +p.getId());
			System.out.println("Name: " +p.getName());
			System.out.println("Country: " +p.getCountry());
			System.out.println(" / ");
		}
	}

}
