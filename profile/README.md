# Organization Purpose

This organization contains forks of all my (dynamic) templates
(repository starting with `template-` in [my personal space](https://github.com/fletort)).

The goal of theses forks is to can be able to run [depandabot](https://docs.github.com/en/code-security/dependabot)
on the final content of such dynamic templates.

The original version of the template does not always contains workflow in the correct branch
(usage of the `$.github` directory) and dependencies files with the correct extension
(j2 template is often use). See my [init-repo-action](https://github.com/fletort/init-repo-action)
to understand how theses dynamic templates are managed.

To can be able to have:
- a resolution of the dynamic template (init workflow must be runned)
- a main branch contening the template resolution (to have also dependabot security patches)
- a possible way to redirect dependabot security/update PR to the original template repo (repo must be a fork of the original repo).

 We have here repositories that are :
- fork of the original repo template
- template resolution is done on itself
- dependaboot PR should be targeting the original template repo (_automatic feature in progress_)
- short-living: as soon as a PR is merged to the original repo, the forked repo must be created (updated?) again by same process (fork/auto-update)
