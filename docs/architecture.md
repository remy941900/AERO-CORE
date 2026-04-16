# AERO-CORE — Architecture logicielle

## Couches logicielles

AC-COCKPIT / AC-ENG / AC-FCS / AC-FMS   ← Applicatif (DAL A/B/C)
AC-MIDDLEWARE                             ← Middleware (DAL B)
AC-RTOS                                   ← RTOS (DAL B)
AC-DRIVERS / AC-BSP                       ← Bas niveau (DAL B/C)
STM32H753ZI Hardware                      ← Matériel

## Configuration Items (CI) — Tableau DAL

| Repo        | Rôle                        | DAL  | Phase |
|-------------|-----------------------------|------|-------|
| AC-BSP      | Board Support Package       | C    | 1     |
| AC-DRIVERS  | Drivers bas niveau          | B/C  | 1     |
| AC-RTOS     | RTOS temps réel             | B    | 2     |
| AC-MIDDLEWARE | Bus de données, monitoring | B    | 3     |
| AC-ENG      | Contrôle moteur             | A/B  | 4     |
| AC-FCS      | Flight Control System       | A    | 4     |
| AC-FMS      | Fault Management System     | A/B  | 4     |
| AC-COCKPIT  | Interface cockpit           | C    | 5     |
| AC-VV       | Vérification & Validation   | B    | ∞     |