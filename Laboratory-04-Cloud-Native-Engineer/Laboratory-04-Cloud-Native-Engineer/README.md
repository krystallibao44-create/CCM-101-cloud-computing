# Mission 4: The Cloud-Native Engineer

Laboratory Activity 4 — CloudNova Technologies Cloud-Native Engineering Team

## Mission Overview

As part of the Cloud-Native Engineering Team at CloudNova Technologies, this mission focused on understanding the shift from traditional virtualization (Virtual Machines) to containerization. Using the KillerCoda Playground, I researched the differences between VMs and containers, executed fundamental Docker CLI commands, and deployed a live, containerized Nginx web server.

## Objectives

- Differentiate between traditional Virtual Machines (VMs) and Containers
- Access a Docker-enabled cloud environment using KillerCoda
- Execute fundamental Docker CLI commands
- Pull, run, manage, and terminate a containerized application (Nginx)
- Create professional technical documentation using Markdown
- Continue developing a well-organized GitHub Cloud Computing Portfolio

## Docker Commands Executed

| Command | Purpose |
|---|---|
| `docker --version` | Checked the installed Docker version |
| `docker info` | Verified the current status of the Docker environment |
| `docker pull nginx` | Downloaded the official Nginx image from Docker Hub |
| `docker run -d -p 8080:80 --name my-nginx nginx` | Ran the Nginx container in detached mode, mapping port 8080 to 80 |
| `curl http://localhost:8080` | Verified the web server was running |
| `docker ps` | Listed running containers |
| `docker stop my-nginx` | Stopped the running container |
| `docker ps -a` | Verified the container had stopped |
| `docker rm my-nginx` | Removed the container completely |

## Skills Learned

- Understanding the architectural difference between VMs (Guest OS, hardware-level isolation) and Containers (shared kernel, process-level isolation)
- Verifying and navigating a Docker-enabled Linux environment
- Pulling images from Docker Hub and running containers in detached mode
- Mapping host-to-container ports for network access
- Managing the full container lifecycle: list, stop, verify, remove
- Writing clear technical documentation in Markdown

## Challenges Encountered

Yung pinaka-nakalito sa akin sa umpisa ay yung `-p 8080:80` na port mapping — hindi ko agad na-gets kung alin talaga doon ang para sa host at alin ang para sa loob ng container, kaya ginamit ko yung `curl http://localhost:8080` para ma-confirm kung tama nga yung pagkakaintindi ko. Nahirapan din ako konti sa pag-iingat sa pangalan ng container (`my-nginx`) dahil kapag nagkamali ako ng spelling dito, hindi na magmamatch yung susunod kong `docker stop` o `docker rm`. Dagdag pa rito, since may takdang oras lang ang KillerCoda session, kinailangan ko talagang bilisan yung bawat step para hindi ma-cut off bago ko pa makuha yung mga screenshots. Pero sa kabuuan, dahil sa mga ganitong pagkakamali at pag-aayos, mas naging malinaw sa akin kung paano talaga sumusunod ang Docker sa buong lifecycle ng isang container — mula sa pag-run nito hanggang sa permanenteng pagtanggal.

Prepared by Casem, Prince Edrian — BSIT 4-Block M
