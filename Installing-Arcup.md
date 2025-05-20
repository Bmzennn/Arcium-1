# Arcup
The ```arcup``` version manager enables easy installation and management of the Arcium Networks' tooling suite, consisting of the Arcium CLI binary, the Arx Node Docker image, the Arcium Callback Server Docker image, and the Postgres Docker image (needed to run the Callback Server).

All the necessary tools can be installed and updated whenever theres a new release. 
```
arcup install # Will install the latest releases of the Arcium components
```
You should see a similar message 👇🏾
![alt text](image.png)

Verify everything was installed correctly with:
```
arcium --version # Should show the latest CLI version
arcup version # Shows the currently installed versions of all of the Arcium components
docker images # Should list the images for the Arx Node, Callback Server, and Postgres
```
Available command for the `arcup` includes 
<pre>
install  Install the latest (or a specific) version of Arcium components (Arx Node, CLI, and Callback Server)
update   Update all Arcium components (Arx Node, CLI, and Callback Server) to the latest version
list     List all installed versions
version  Show currently active version
use      Switch to using a specific installed version
delete   Delete a specific version
help     Print this message or the help of the given subcommand(s)
</pre>