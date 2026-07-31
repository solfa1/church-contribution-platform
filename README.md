Church Contribution Platform

A web application for monitoring church contribution campaigns.

The platform allows a church to create a contribution campaign with a financial target and display the current progress towards that goal. As contributions are received, the platform calculates the total amount contributed, the remaining balance and the overall completion percentage.

The application is being built with a production-first mindset using modern DevOps practices and will eventually support automatic payment verification through a payment provider.

Technology

Frontend

* Next.js
* TypeScript
* Tailwind CSS

Backend

* Next.js Route Handlers
* Prisma ORM
* Zod

Database

* PostgreSQL

Development

* Docker
* Docker Compose

Infrastructure

* AWS ECS Fargate
* Amazon RDS
* Amazon ECR
* Terraform
* GitHub Actions
* Application Load Balancer
* CloudWatch

Project Structure

```text
app/
components/
prisma/
public/
terraform/
compose.yaml
package.json
```

Requirements

* Node.js 20 or later
* npm
* Git
* Docker
* Docker Compose

Setup

Clone the repository.

```bash
git clone https://github.com/solfa1/church-contribution-platform.git
cd church-contribution-platform
```

Install dependencies.

```bash
npm install
```

Create a `.env` file using the `.env.example` file.

Start PostgreSQL.

```bash
docker compose up -d
```

Run the database migrations.

```bash
npx prisma migrate dev
```

Start the development server.

```bash
npm run dev
```

Open your browser and visit:

```text
http://localhost:3000
```

Useful Commands

Start PostgreSQL

```bash
docker compose up -d
```

Stop PostgreSQL

```bash
docker compose down
```

View PostgreSQL logs

```bash
docker compose logs postgres
```

Open the PostgreSQL shell

Validate the Prisma schema

```bash
npx prisma validate
```

Create a new migration

```bash
npx prisma migrate dev --name <migration-name>
```

Development Workflow

* Create a feature branch.
* Build one feature at a time.
* Test before committing.
* Use meaningful commit messages.
* Push changes regularly.
* Merge completed features into `main`.

