# Check-in/Check-out and Visitor Log Service

**Cloud-Based Visitor Management System – Group 9**

**Owner:** Mostafa Raafat Mohamed

## 1. Overview

This repository contains my contribution to the Cloud-Based Visitor Management System. It focuses on managing visitor check-in and check-out operations, maintaining visitor logs, monitoring on-site visitors, and generating activity reports.

The complete application is available in the [Main Group 9 Repository](https://github.com/RawyAliSalim/Cloud-Based-Visitor-Management-System-Group-9).

## 2. Main Features

- Visitor check-in and check-out management.
- Visit status management and validation.
- Atomic status updates to prevent concurrent check-in conflicts.
- Visitor status history and timestamps.
- On-site visitor monitoring.
- Visit duration and overstay detection.
- Date-based visitor log filtering.
- Activity reports and attendance statistics.
- CSV visitor log exports.
- Application logging and error handling.

## 3. Business Rules

The service uses four visit statuses:

- Expected
- Checked-in
- Checked-out
- Cancelled

It validates permitted state transitions and enforces check-in rules, including arrival time restrictions, host availability, and preventing visitors from having multiple active visits.

The service records who performed check-in and check-out operations and maintains a history of status changes.

## 4. Technologies

- Node.js
- Express.js
- MongoDB
- React
- Docker and Docker Compose
- Vercel
- AWS CLI v2
- Floci (local AWS emulator)

## 5. AWS Services

The project uses AWS-compatible services through Floci:

**AWS Secrets Manager**
- Stores application secrets.
- Supports secure secret retrieval and rotation.

**Amazon S3**
- Stores compressed MongoDB backups.
- Uses encryption, versioning, blocked public access, and checksum verification.

Floci runs locally through Docker and emulates AWS services for development and testing.

## 6. Deployment

The project uses Docker and Docker Compose for its local development environment, Floci for local AWS emulation, and Vercel for production deployment.

MongoDB Atlas is used for the production database.

## 7. Logging and Monitoring

The service includes:
- Application logging.
- Request logging middleware.
- Centralized error-handling middleware.

These components help with monitoring application behaviour and troubleshooting errors.

## 8. Testing

Integration tests cover:
- Check-in and check-out operations.
- Invalid visit transitions.
- Concurrent check-in requests.
- Arrival time restrictions.
- Host availability.
- Visitor already on-site validation.
- Status history.
- Overstay detection.
- Date filters.
- Activity reports.
- CSV export validation.

## 9. Repository Structure

```text
api/
client/
docker/
docs/
scripts/
server/
tests/
Dockerfile
docker-compose.yml
vercel.json
README.md
```

This repository contains my assigned service files and the shared deployment, logging, and monitoring components I worked on.