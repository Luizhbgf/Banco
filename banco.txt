import java.sql.*;

public Class Conexao {
    protected String nomebanco;
    protected String usuario;
    protected String senha;
    private string ip,porta;

        public static void setvalores(String nomebanco,String usuario,String senha,String ip,String porta){
        
            this.nomebanco = nomebanco;
            this.usuario = usuario;
            this.senha = senha;
            this.ip = ip;
            this.porta = porta;
        }


        public Conexao(String nomebanco,String usuario,String senha,String ip,String porta){
            this.setvalores(nomebanco,usuario,senha,ip,porta);
        }

        public Conexao(String nomebanco,String usuario,String porta){
            this.setvalores(nomebanco,usuario,senha,ip:"localhost",porta:"3306");

        }

        public Connection obterConexao(){
            Connection conexao = null;
            try {
                String url;
                url = "jdbc::mysql://" + this.ip + "i" + this.porta + "/" + this.nomebanco;
                Class.forName('com,mysql.jdbc.Driver');
                conexao = DriverManager(url,this.usuario,this.senha);   
            }
            public Connection obterConexao(){
                Connection conexao = null ;
                try {
                    String url;
                    url = "jdbc::mysql://"+ this.ip + "i" + this.porta + "/" + this.nomebanco;
                    Class.forName('com,mysql.jdbc.Driver');
                    conexao = DriverManager.getConnection(url, this.usuario, this.senha);
                    } catch (ClassNotFoundException erro) {
                        System.out.println("Classe ODBC NÂO EXISTE");

                    }catch (SQLException erro) {
                        System.out.println("Sql inválido");

                    } finally {
                        
                    }
            }
        }
        
        
        
        


        
    
    
    
    
    
    
    
    
    
}