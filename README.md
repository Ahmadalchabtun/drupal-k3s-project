# Drupal k3s Platform

Dit is een schaalbaar en veilig platform voor Drupal-websites, draaiend op Kubernetes (k3s).

## Hoe te starten

1. Clone deze repository: `git clone https://github.com/Ahmadalchabtun/drupal-k3s-project.git`
2. Ga naar de map: `cd drupal-k3s-project`
3. Deploy de applicatie op je k3s-cluster (zie de Kubernetes-configuraties in deze repository).
4. Ga naar  om de Drupal-site te zien.

## Services

- **Drupal**: De website (draait op node1).
- **MySQL**: Database (draait op node2).
- **Nginx Ingress**: Webserver voor externe toegang.

## Beveiliging

- **Trivy**: Gebruikt om container-images te scannen op kwetsbaarheden.
- **Falco**: Bewaakt verdacht gedrag in containers tijdens runtime.

## CI/CD

- **GitHub Actions**: Automatische pipeline die bij elke push naar de main-branch:
  - de k3s-deployments bijwerkt
  - test of de Drupal-site bereikbaar is
  - eventueel opruimt

Workflow-bestand: `.github/workflows/ci.yml`
