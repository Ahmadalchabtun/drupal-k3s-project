# Drupal k3s Platform
Dit is een schaalbaar en veilig platform voor Drupal-websites, draaiend op Kubernetes (k3s).

Hoe te starten
Clone deze repository: cd drupal-k3s-project om de Drupal-site te zien.
Services
Drupal: De website (draait op node1).
MySQL: Database (draait op node2).
Nginx Ingress: Webserver voor externe toegang.
Beveiliging
Trivy: Gebruikt om container-images te scannen op kwetsbaarheden.
Falco: Bewaakt verdacht gedrag in containers tijdens runtime.
CI/CD
GitHub Actions: Automatische pipeline die bij elke push naar de main-branch de k3s-deployments bijwerkt, test of de Drupal-site bereikbaar is, en eventueel opruimt.
Workflow-bestand:  
