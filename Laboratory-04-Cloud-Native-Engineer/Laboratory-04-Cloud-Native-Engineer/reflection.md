# Mission Reflection

Sa activity na ito, mas luminaw sa akin kung paano binago ng containerization ang paraan ng pag-deploy sa mga modern application. Malaki talaga ang agwat ng boot time — sa VM, kailangan munang mag-boot ng kumpletong guest operating system kaya minuto ang aabutin, samantalang sa container, isang process lang ang tatakbo gamit ang shared kernel ng host kaya ilang segundo lang. Dito ko mas naappreciate kung bakit mas maganda ang container pagdating sa mabilis na pag-scale ng mga web app.

Importante rin ang port mapping (`-p 8080:80`) dahil by default, naka-isolate ang internal network ng container mula sa host machine. Kung walang explicit mapping, hindi maaabot ng external requests — gaya ng ginamit kong `curl` command — ang Nginx server na nasa loob ng container.

Napansin ko rin na kapag na-execute ang `docker rm`, permanenteng nabubura ang data na naka-store sa loob noong container, dahil talagang ephemeral ang disenyo nito. Kaya kung kailangan ng persistent na data, mas praktikal gumamit ng Docker volumes kaysa umasa sa storage ng container mismo, lalo na sa production environment.

Binago rin ng containerization kung paano nagtutulungan ang developers at IT operations. Dahil naka-package na magkasama ang application at lahat ng dependencies nito, nawawala yung common na isyu na "gumagana naman sa computer ko" — kung gumagana ang container locally, malaki ang tsansang gagana rin ito sa production. Ito mismo ang nagpapalakas sa kolaborasyon ng development at operations teams, na siyang pundasyon ng DevOps culture.

Sa huli, patuloy na lumalago ang GitHub portfolio ko sa bawat laboratory activity — kasama na ngayon ang hands-on na dokumentasyon ng cloud infrastructure concepts at container deployment. Napahusay ng mission na ito ang practical skills ko gamit ang Docker CLI, pati na rin ang kakayahan kong mag-dokumento ng technical process gamit ang Markdown.
