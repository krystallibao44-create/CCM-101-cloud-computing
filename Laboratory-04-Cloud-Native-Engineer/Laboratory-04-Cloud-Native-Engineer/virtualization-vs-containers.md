# Virtual Machines vs. Containers

Laboratory Activity 4 — Mission 4: The Cloud-Native Engineer
Comparing traditional virtualization to containerization technology.

## Comparison Table

| Category | Virtual Machines (VMs) | Containers |
|---|---|---|
| **Architecture** | Each VM runs its own Guest OS on top of a hypervisor | Containers share the Host OS kernel |
| **Boot Time** | Minutes — needs to boot a full OS | Seconds — just starts the app process |
| **Resource Efficiency** | Heavy — high RAM/CPU usage per VM | Lightweight — low RAM, shares host resources |
| **Isolation Level** | Hardware-level (very strong, separate kernel) | Process-level (namespaces/cgroups) |

## Why Containers?

Para sa client, mas makatuwiran ang containers kumpara sa VMs dahil wala nang kailangang buong OS per instance — kaya ilang segundo lang, hindi na minuto, ang boot time. Isa pa, dahil parehong container ang gumagamit lang ng iisang host OS kernel, mas mababa ang consumption ng RAM at CPU, kaya mas maraming service ang kasya sa parehong server. Mas flexible din ito sa pag-scale — pwede lang mag-spin up o mag-tanggal ng container kaagad kapag kailangan, hindi tulad ng VM na kailangan pang maghintay ng buong boot process. Kaya kung ang gustong solusyunan ng client ay yung bagal at sayang na resources, malaking tulong ang containers, at sapat na rin naman ang isolation level nito para sa karamihan sa mga pangangailangan nila.

Prepared by Casem, Prince Edrian — BSIT 4-Block M
