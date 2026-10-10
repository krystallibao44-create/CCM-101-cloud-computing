# Laboratory 06: The Cloud Deployment Engineer

**Course:** CCM101 – Cloud Computing (Midterm Laboratory Exam, Mission 6)
**Student:** Prince Edrian Casem
**Platform:** KillerCoda Docker playground

---

```

## Lab Objectives (all completed)

- [x] Describe what a multi-tier application architecture is
- [x] Understand why a `docker-compose.yml` is written the way it is
- [x] Create a configuration file using the `nano` editor
- [x] Deploy a multi-container app (Nextcloud + database) with Docker Compose
- [x] Document the deployment and IaC ideas in Markdown

## Step-by-Step Procedure

1. **Create the working folder** with `mkdir nextcloud-deployment`, then enter it with `cd nextcloud-deployment`.
2. **Write the Compose file** by running `nano docker-compose.yml` and typing the two services (see the guide for the full file).
3. **Start the stack** with `docker-compose up -d`. Docker pulled both images and launched the containers in detached mode.
4. **Verify** with `docker-compose ps`. Both services showed an `Up` status.
5. **Open Nextcloud** through the KillerCoda Traffic / Ports tab on port 8080 and reached the setup page.
6. **Clean up** with `docker-compose down`, which removed the containers and the network created for the stack.

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Evidence

| # | What the screenshot shows | File |
|---|---|---|
| 1 | Creating the folder and launching nano | `screenshots/01-project-setup.png` |
| 2 | The finished `docker-compose.yml` | `screenshots/02-compose-file.png` |
| 3 | Images being pulled by `docker-compose up -d` | `screenshots/03-compose-up-pulling.png` |
| 4 | Both containers running | `screenshots/compose-deployment.png` |
| 5 | Nextcloud setup page in the browser | `screenshots/nextcloud-web.png` |
| 6 | Stack removed with `docker-compose down` | `screenshots/compose-teardown.png` |

## What I Took Away From This Lab

- A whole application can be declared in YAML, and indentation is part of the syntax.
- Compose lets containers talk to each other by service name, so no IP addresses are needed.
- Environment variables are how credentials and settings get into a container at startup.
- `8080:80` means host port 8080 forwards to port 80 inside the container.
- Splitting an app into tiers and writing it as code makes a deployment easier to repeat and explain.

## Other Files in This Submission

- [multi-tier-architecture.md](multi-tier-architecture.md): the two-tier design and the reason for separating the tiers
- [docker-compose-guide.md](docker-compose-guide.md): line-by-line explanation of the Compose file and a comparison with `docker run`
- [reflection.md](reflection.md): my personal reflection

## Folder Layout

```text
Laboratory-06-Cloud-Deployment-Engineer/
├── README.md
├── multi-tier-architecture.md
├── docker-compose-guide.md
├── reflection.md
└── screenshots/
```
