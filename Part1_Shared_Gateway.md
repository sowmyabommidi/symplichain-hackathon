# Part 1: Shared Gateway Problem

Architecture:
Django → Redis Queue → Celery Worker → Rate limiter → External API

Fairness:
- Customer specific queues
- Round robin dispatcher
- Prevents starvation

Retry Strategy:
- Exponential backoff
