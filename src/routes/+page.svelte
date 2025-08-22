<script lang="ts">
    import ContactForm from '$lib/components/ContactForm.svelte';
</script>

<section id="hero">
    <div>
        <h1>Un puente entre las empresas y la tecnología</h1>
        <h2>Donde la estrategia financiera se encuentra con la innovación digital.</h2>
        <p>Bienvenido. Soy Marco Gómez, y mi trabajo es tender un puente entre tus metas financieras y las soluciones tecnológicas que las hacen posibles. Como Contador Público con alma de programador, no solo entiendo tus desafíos de negocio, sino que construyo las herramientas digitales a medida para resolverlos.</p>
        <div class="cta-buttons">
            <a href="#services" class="button primary">Conoce mis Servicios</a>
            <a href="#work" class="button secondary">Ver Proyectos</a>
        </div>
    </div>
</section>

<section id="about">
    <div>
        <h2>Acerca de Mí</h2>
        <p>Mi carrera comenzó en el mundo de la contabilidad, donde la lógica, la precisión y la responsabilidad son pilares fundamentales. Como Contador Público, me especialicé en auditoría y en la gestión de proyectos de implementación de sistemas ERP, lo que me permitió comprender a fondo el corazón de las empresas: sus finanzas y sus procesos.</p>
        <p>Sin embargo, a medida que avanzaba, noté una brecha recurrente: las herramientas tecnológicas a menudo no se adaptaban a las necesidades reales del negocio o eran demasiado complejas para ser eficientes. Fue esa necesidad de crear soluciones más inteligentes y a medida lo que me llevó a la programación. Lo que empezó como una curiosidad, rápidamente se convirtió en mi mayor herramienta de crecimiento profesional.</p>
        <p>Hoy, combino mi sólida base financiera con mi habilidad para desarrollar software, creando un puente único entre la estrategia de negocio y la tecnología. Ese fue mi momento de claridad: entendí que no se trataba solo de encontrar problemas, sino de tener el poder de construir la solución. Y eso es lo que ofrezco.</p>
        
        <h3>Logros Clave:</h3>
        <ul>
            <li>Auditoría y Control de Gestión: Amplia experiencia garantizando la integridad financiera y optimizando procesos internos.</li>
            <li>Gestión de Proyectos ERP: Liderazgo en la implementación de sistemas de planificación de recursos empresariales, asegurando una transición exitosa y una mejora medible en la eficiencia.</li>
            <li>Desarrollo de Soluciones a Medida: Creación de aplicaciones y herramientas personalizadas para resolver desafíos específicos de negocio.</li>
        </ul>
    </div>
</section>

<section id="services">
    <div>
        <h2>Consultoría Financiera y de Procesos</h2>
        <h3>Gestión de Proyectos Tecnológicos</h3>
        
        <div>
            <h4>Optimización de Procesos y Estrategia Financiera</h4>
            <p>Ofrezco un análisis profundo de tus procesos contables y financieros para identificar áreas de mejora, optimizar flujos de trabajo y asegurar que tu negocio opere con la máxima eficiencia. El objetivo es simple: transformar tus desafíos en oportunidades de crecimiento a través de una estrategia clara y bien estructurada.</p>
            <p><strong>Beneficio Clave:</strong> Obtendrás una hoja de ruta clara para fortalecer tu control financiero, reducir costos operativos y tomar decisiones más informadas.</p>
        </div>

        <div>
            <h4>Desarrollo de Soluciones Tecnológicas a Medida</h4>
            <p>Lidero proyectos de implementación de software y desarrollo de herramientas digitales desde la concepción hasta la puesta en marcha. Mi enfoque combina la rigurosidad de la gestión de proyectos con un profundo entendimiento de las necesidades del negocio, asegurando que la tecnología trabaje para ti, y no al revés.</p>
            <p><strong>Beneficio Clave:</strong> Tendrás la certeza de que tu inversión tecnológica se traducirá en resultados tangibles, con soluciones robustas, seguras y perfectamente alineadas a tus objetivos.</p>
        </div>
    </div>
</section>

<section id="work">
    <div>
        <h2>Proyectos</h2>
        <h3>Caso de Estudio: Página Web de Control de Inventarios</h3>
        
        <div>
            <h4>Problema:</h4>
            <p>Una empresa cliente gestionaba su inventario a través de hojas de cálculo complejas y propensas a errores humanos. Este método no solo consumía una cantidad significativa de tiempo del equipo, sino que también generaba discrepancias en las auditorías, creando un riesgo financiero y operativo.</p>
        </div>

        <div>
            <h4>Mi Enfoque:</h4>
            <p>Analicé el flujo de trabajo existente y diseñé una solución lógica basada en una aplicación web centralizada. El proceso incluyó el mapeo de los procesos clave (entradas, salidas, ajustes), el diseño de una base de datos relacional para garantizar la integridad de los datos y el desarrollo de una interfaz de usuario intuitiva y fácil de usar para el equipo.</p>
        </div>

        <div>
            <h4>Solución y Resultados:</h4>
            <p>Desarrollé una página web a medida que automatiza el registro y seguimiento del inventario en tiempo real. La solución eliminó por completo el uso de hojas de cálculo, redujo los errores de registro en un 99% y disminuyó el tiempo dedicado a la gestión de stock en más de 15 horas semanales. Además, la empresa ahora cuenta con datos precisos y fiables para sus auditorías, fortaleciendo su control interno.</p>
        </div>

        <p>¿Tienes un desafío similar? <a href="#contact">Hablemos de cómo podemos crear una solución para ti.</a></p>
    </div>
</section>

<section id="contact">
    <div>
        <h2>Contacto</h2>
        <p>Si estás buscando un socio estratégico que entienda tanto de números como de código, estoy aquí para ayudarte. Hablemos sobre cómo podemos llevar tu negocio al siguiente nivel.</p>
        <ul>
            <li><strong>Correo:</strong> <a href="mailto:marco.gomez@email.com">marco.gomez@email.com</a></li>
            <li><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/marcogomez" target="_blank" rel="noopener noreferrer">linkedin.com/in/marcogomez</a></li>
        </ul>
        <ContactForm />
    </div>
</section>
