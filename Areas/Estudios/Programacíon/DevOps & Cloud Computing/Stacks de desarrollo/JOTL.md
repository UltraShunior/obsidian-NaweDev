En el mercado también es muy popular el stack de la empresa Oracle JOTL (Java, Oracle, Tomcat, Linux) dado el soporte y la fama que tiene Oracle de tener el sistema de base de datos más robusto, y esto sumado con Java que es un lenguaje de programación multiplataforma: funciona para hacer aplicaciones de escritorio, aplicaciones web, aplicaciones móviles para Android, etc.

Estas son las formas más comunes para desplegar una aplicación JOTL.

- Usar una plataforma como servicio: Se puede utilizar una PaaS - Platform As A Service, como es el caso de heroku, que se encarga del despliegue de la aplicación y se puede hacer un despliegue más rápido, pero se pierde el control sobre el servidor.
    
- Usar una Infraestructura como servicio: IaaS o Infrastructure As a Service, son empresas como AWS de Amazon, Cloud Platform de Google, Azure de microsoft o incluso IBM cloud, estas ofrecen un control mayor sobre la infraestructura, desde los servidores VPS, red, Backups, disponibilidad, escalabilidad, seguridad entre otras ventajas, sin embargo requieren de un conocimiento en manejo de infraestructuras para poder configurar todas estas opciones.
    
- Usar infraestructura propia: Algunas empresas prefieren disponer de una infraestructura propia, esto se conoce como on-premises, entre la razones y ventajas para este tipo de infraestructura están:  
    Privacidad del código fuente o aplicación, ya que este se encontrará local y no en servidores en una nube a los que terceros podrían acceder.
    
    La segunda razón es por latencia, dado que un datacenter en la misma ciudad podrá ofrecer mejores tiempos de respuesta que uno en otro País o continente.
    
    Finalmente por control, ya que las empresas que adoptan esto, tienen control total sobre la infraestructura física (no sólo la lógica como ocurre con las IaaS).
    
    Como desventajas principales están: Disponibilidad física, si el lugar donde está el datacenter sufre un incendio, terremoto o cualquier situación que afecte el lugar, podría perderse el acceso físico a la información y/o a la red.
    
    Costo, mientras la computación en la nube ofrece precios competitivos por horas, escalamiento dinámico y otros temas que parecen casi automáticos, en los entornos on-premise los costos pueden ser mayores dado que se debe costear servidores, racks de almacenamiento, el datacenter donde se almacenará la información, la energía, internet, seguridad, y demás costos asociados.
    
    Existen muchas opciones para desplegar aplicaciones de este tipo, cada una tiene ventajas y desventajas, depende del tipo de proyecto la opción a seleccionar.
    
    Nota: En el Stack de Java y Oracle también se puede intercambiar Apache Tomcat con GlassFish u otros, incluso en la parte de sistema operativo, cambiando Linux por Windows server.