
# Run any version of R interactively on GitHub Actions

Uses the [evercran container images](
https://github.com/r-hub/evercran#readme).

## Requirements

You need an SSH client to connect.

## Usage

0.  Add your public SSH key to GitHub, at
    <https://github.com/settings/keys>. If you don’t have an SSH
    key-pair, first generate one using your SSH client.
1.  Fork this repository.
2.  In the ‘Actions’ menu of your fork enable GitHub Actions.
3.  Click on ‘All workflows’ on the left, and select ‘Run any R version’.
4.  Click the ‘Run workflow’ dropdown menu on the right side.
5.  Enter the R version you like. See the list of R versions
    in the [evercran README](
	https://github.com/r-hub/evercran#list-of-all-containers).
6.  Click on the ‘Run workflow’ button.
7.  Wait a few seconds for the workflow to start running.
8.  Click on running workflow’s name (‘Run any R version’).
9.  Click on the ‘evercran’ job.
10. Wait a couple of seconds, until you see the ‘ssh connection’ banner
    in the output. Under this you'll see the SSH command to connect.
11. Copy the SSH command and paste it into a terminal window. Or,
    if you use an SSH app, copy the connection URL and use it in the
    app. You’ll need your SSH key to authenticate, the one that
	corresponds to the public key you added in step 0.

The R session runs in a Docker container, in a tmate session. To open a new
shell in the container use `CTRL-b c` (press `CTRL` + `b` together, let
them go, then press `c`). 

Type `R` in the shell to open another R session if you like. 

Use `CTRL-b n` to switch between your shells.

In the shell you can use `apt-get` to install Debian packages.

In R you can use `install.packages()` to install R packages from
the appropriate evercran CRAN snapshot.

When you quit from all shells, the container stops and the workflow
terminates.

## License

See https://www.r-project.org/Licenses/ for the R licenses.
The evercran tools are licensed under the MIT License.

© [Gábor Csárdi](https://github.com/gaborcsardi), 
  [Posit Software, PBC](https://posit.co/)
