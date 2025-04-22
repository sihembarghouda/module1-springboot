## NOTES.md

### 1. Annotations utilisées
- `@SpringBootApplication` : combine `@Configuration`, `@EnableAutoConfiguration`, `@ComponentScan`
- `@RestController` : indique que c’est un contrôleur REST
- `@GetMapping` : mappe les requêtes HTTP GET
- `@RequestParam` : lit les paramètres de l’URL

### 2. Conversion en JSON
Spring Boot utilise Jackson automatiquement pour transformer les objets Java en JSON via les annotations REST.

### 3. @SpringBootApplication
Elle rend la classe principale auto-configurable et scanne automatiquement les composants.

### 4. Changer le port
Dans `application.properties` :  
`server.port=8081`

### 5. Avantages de Spring Boot
- Démarrage rapide
- Moins de configuration
- Serveur intégré (Tomcat)
- Compatible microservices
- Facile à tester
