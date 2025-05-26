```mermaid
graph TD
    subgraph "genai_project (Main Project)"
        Settings["settings.py"]
        MainURLs["urls.py"]
        WSGI["wsgi.py"]
        ASGI["asgi.py"]
    end
    
    subgraph "query_analyzer (Django App)"
        Models["models.py"]
        Views["views.py"]
        AppURLs["urls.py"]
        Forms["forms.py"]
        Admin["admin.py"]
        Apps["apps.py"]
    end
    
    subgraph "Templates"
        Base["base.html"]
        Home["home.html"]
        SignUp["signup.html"]
        SignIn["signin.html"]
    end
    
    subgraph "Utils Package"
        LLMConn["llm_connector.py"]
        DBConn["db_connector.py"]
        SQLOpt["sql_optimizer.py"]
    end
    
    subgraph "Static Files"
        CSS["styles.css"]
        JS["main.js"]
    end
    
    Settings --> Models
    MainURLs --> AppURLs
    AppURLs --> Views
    Views --> Models
    Views --> Forms
    Views --> LLMConn
    Views --> DBConn
    Views --> SQLOpt
    Views --> Base
    Base --> Home
    Base --> SignUp
    Base --> SignIn
    Home --> CSS
    Home --> JS