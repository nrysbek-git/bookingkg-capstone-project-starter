# BookingKG — Student Project

**Язык:** Русский · [English](README_EN.md)

Это стартовый репозиторий итогового DevOps capstone.

Студент получает готовый application layer:

- `frontend/` — React-интерфейс BookingKG;
- `backend/` — Node.js/Express API;
- `database/init.sql` — начальная схема PostgreSQL;
- [ASSIGNMENT.md](ASSIGNMENT.md) — полное задание ([English](ASSIGNMENT_EN.md));
- [PREREQUISITES.md](PREREQUISITES.md) — требования ([English](PREREQUISITES_EN.md));
- [GRADING_RUBRIC.md](GRADING_RUBRIC.md) — оценивание ([English](GRADING_RUBRIC_EN.md));
- [TROUBLESHOOTING.md](TROUBLESHOOTING.md) — диагностика ([English](TROUBLESHOOTING_EN.md));
- [COST_AND_CLEANUP.md](COST_AND_CLEANUP.md) — бюджет ([English](COST_AND_CLEANUP_EN.md));
- [NOTICE.md](NOTICE.md) — авторство ([English](NOTICE_EN.md));
- [MODIFICATIONS.md](MODIFICATIONS.md) — состав редакции ([English](MODIFICATIONS_EN.md)).

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
