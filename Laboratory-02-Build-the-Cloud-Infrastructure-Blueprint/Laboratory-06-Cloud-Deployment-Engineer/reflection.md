# Reflection: Mission 6

Going into this lab, my habit was to start containers individually using long `docker run` commands and trying to remember every option. Compose showed me a cleaner way. I wrote the whole setup into one file and brought it up with `docker-compose up -d`. The time saved is nice, but the real benefit is consistency. Anyone who has the file gets the same result, and it can be stored in GitHub and reviewed like normal code. This is how I now understand Infrastructure as Code.

The lab also taught me how unforgiving YAML is. Indentation must use spaces, and a single Tab character makes the file invalid, so Compose reports an error and starts nothing. Even a wrong number of spaces can push a key under the wrong parent and silently change the meaning. Because of this, I now check the alignment in nano before I save.

Environment variables were another important idea. Values like `MYSQL_PASSWORD` are supplied when the container starts, not stored in the image. MariaDB reads them to create its user and database, and Nextcloud reads the same values to log in, so the two containers always agree. It also means I can change a credential without rebuilding an image. At the same time, I recognize that writing passwords directly into a file that goes to GitHub is not safe in real projects. A `.env` file or a secrets manager would be the proper approach there.

The best moment was seeing both services marked `Up` in `docker-compose ps` and then loading the Nextcloud setup page in the browser. A private storage service came out of roughly twenty lines of YAML and two commands in only a few minutes.

My idea of cloud computing has also shifted since the first mission. Before, I thought it was just renting a computer from somebody else. Now I think of it as designing systems in layers, describing them in code, and being able to deploy them the same way every time.
