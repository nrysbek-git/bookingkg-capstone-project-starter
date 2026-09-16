# BookingKG — Student Project

Это стартовый репозиторий итогового DevOps capstone.

Студент получает готовый application layer:

- `frontend/` — React-интерфейс BookingKG;
- `backend/` — Node.js/Express API;
- `database/init.sql` — начальная схема PostgreSQL;
- [ASSIGNMENT.md](ASSIGNMENT.md) — полное техническое задание;
- материалы по требованиям, оцениванию, диагностике и AWS cleanup.

Приложение поддерживает регистрацию, каталог, избранное, проверку свободных
дат, дополнительные услуги, бронирования, отмену и ваучер.

Студент самостоятельно создаёт:

- Dockerfile для frontend и backend;
- Docker Compose для локального запуска;
- Kubernetes manifests для Amazon EKS;
- Terraform для VPC, EKS, ECR, RDS и IAM;
- GitHub Actions CI/CD через OIDC;
- документацию, evidence и cleanup-инструкцию.

В student repository намеренно отсутствуют готовые Docker, Kubernetes, Terraform и CI/CD
реализации. Не добавляйте в Git пароли, AWS keys, `.env`, kubeconfig или
Terraform state.

Начните с [полного задания](ASSIGNMENT.md).
