# PULL REQUEST

Les pull requests sont un moyen essentiel de gérer les contributions  collaboratives et de maintenir un code source propre et de haute qualité. Elles permettent de suivre les modifications apportées au code,de discuter des implications et des avantages potentiels de ces  modifications, et de s'assurer que les modifications sont compatibles 
avec le reste du code avant leur fusion dans la branche principale.

Une pull request est essentiellement une proposition de modification du code source d'un projet. Voici comment cela fonctionne généralement :

1. Un développeur crée une branche (une copie distincte du code) à partir de la branche principale (généralement appelée "master" ou "main") pour travailler sur une nouvelle fonctionnalité, une correction de bogue ou toute autre modification.

2. Le développeur fait les modifications nécessaires dans sa branche et les enregistre.

3. Une fois que le développeur est satisfait de ses modifications, il crée une pull request en demandant que les changements de sa branche soient "tirés" (merged) dans la branche principale.

4. Les autres membres de l'équipe ou les collaborateurs potentiels peuvent alors examiner la pull request, discuter des modifications proposées, poser des questions ou suggérer des améliorations. Cela favorise la collaboration et la révision du code.

5. Si la pull request est approuvée et les révisions nécessaires sont effectuées, les changements sont fusionnés dans la branche principale, intégrant ainsi les modifications dans le code de base.

6. La pull request est ensuite fermée.

#### PRATIQUE DU PULL REQUEST

1. Fork the project:
- Click the gray Fork button at the top right of this page.
   This creates your copy of the project and saves it as a new repository 
  in your GitHub account
2. Create a New Branch:
- On your new repository's page, click the gray main button in the upper left to reveal a dropdown menu.
- Enter the name of your new branch in the text box. (Branch names 
  usually refer to what is being changed. Example: nameAdd).
  -Click on Create branch , which will automatically take you to your new 
  branch. You can make edits on the main branch, but this may cause issues
   down the line. The best practice is to create a new branch for each 
  separate issue you work on. That way your main branch remains in sync 
  with Organisation's main branch.
3. Clone the create branch and make your modifications

4. Raise a Pull Request:
- Click `Pull Requests` (which is the third option at the top of this page after the options `Code` and `Issues`).
- Click the green New Pull Request button.
- Click on your head repository's `compare` dropdown, and switch branches from your 'main' branch to `<new-branch-name>`.
- Finally, click the green `Create Pull Request` button. Great job! You did it!

## ISSUES

Un "issue" sur GitHub est une fonctionnalité qui permet aux utilisateurs de suivre et de gérer des tâches, des bogues, des améliorations ou tout autre type de travail lié à un projet logiciel ou à un référentiel. GitHub est une plateforme populaire pour la gestion de versions et la collaboration entre les développeurs de logiciels, et les issues sont une partie essentielle du flux de travail pour la gestion de projet et la communication au sein d'un référentiel GitHub.

Voici les principales caractéristiques et utilisations des issues sur GitHub :

1. **Suivi des tâches :** Les issues sont utilisées pour suivre diverses tâches, telles que la correction de bogues, les demandes de fonctionnalités, les mises à jour de la documentation ou des tâches à faire. Chaque issue est essentiellement une unité de travail qui doit être traitée.

2. **Communication :** Les utilisateurs peuvent créer des issues et y ajouter des commentaires, ce qui permet la discussion et la collaboration entre les membres de l'équipe et les contributeurs. Les conversations peuvent inclure des extraits de code, des liens et des images, en faisant un outil de communication polyvalent.

3. **Étiquettes et attributions :** Les issues peuvent être catégorisées et organisées à l'aide d'étiquettes, ce qui facilite l'identification de leur type, de leur priorité ou de leur état. Des attributions peuvent être désignées pour indiquer qui est responsable de travailler sur l'issue.

4. **Jalons (Milestones) :** Les jalons servent à regrouper des issues connexes, représentant souvent une version spécifique du projet ou une publication. Cela aide à la planification du projet et au suivi de la progression.

5. **Références :** Les issues peuvent faire référence à d'autres issues, des pull requests ou des commits. Cela permet de lier et de faire des renvois croisés vers des travaux connexes.

6. **Recherche et filtrage :** GitHub propose des options de recherche et de filtrage pour les issues, ce qui facilite la recherche et le tri des issues en fonction de différents critères.

7. **Notifications :** Les utilisateurs peuvent recevoir des notifications lorsqu'il y a des mises à jour ou des modifications des issues auxquelles ils participent, ce qui garantit qu'ils restent informés de l'avancement des tâches.

8. **Intégration :** Les issues peuvent être intégrées avec d'autres fonctionnalités de GitHub, comme les pull requests, permettant une meilleure coordination entre les modifications de code et la résolution des issues.

Les issues de GitHub servent d'outil polyvalent pour la gestion de projet et la collaboration, que vous travailliez sur des logiciels open source, des projets privés ou même des tâches non liées au logiciel. Ils aident les équipes à suivre le travail, à prioriser les tâches et à maintenir la transparence dans le développement du projet.

# Quickstart for GitHub Issues

[Quickstart for GitHub Issues - GitHub Docs](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart) 

## [Introduction](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#introduction)

This guide demonstrates how to use GitHub Issues to plan and track a 
piece of work. In this guide, you will create a new issue and add a task
 list to track sub-tasks. You'll also learn how to add labels, 
milestones, assignees, and projects to communicate metadata about your 
issue.

## [Prerequisites](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#prerequisites)

To create an issue, you need a repository. You can use an existing 
repository that you have write access to, or you can create a new 
repository. The repository must have issues enabled. For more 
information about creating a repository, see "[Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)." For more information about enabling issues if they are disabled in your repository, see "[Disabling issues](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/disabling-issues)."

## [Opening a blank issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#opening-a-blank-issue)

First, create an issue. There are multiple ways to create an issue; 
you can choose the most convenient method for your workflow. This 
example will use the GitHub UI. For more information about other ways to
 create an issue, see "[Creating an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue)."

1. On GitHub.com, navigate to the main page of the repository.

2. Under your repository name, click

3. **Issues**.
   
   ![Screenshot of the main page of a repository. In the horizontal navigation bar, a tab, labeled "Issues," is outlined in dark orange.](https://docs.github.com/assets/cb-52119/images/help/repository/repo-tabs-issues.png)

4. Click **New issue**.

5. In this example, we will start with a blank issue. Your repository 
   may use issue templates and issue forms to encourage contributors to 
   provide specific information. If your repository uses issue templates, 
   click **Open a blank issue**.

## [Filling in information](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#filling-in-information)

Give your issue a descriptive title. The title should convey at a glance what the issue is about.

Add a description that explains the purpose of the issue, including 
any details that might help resolve the issue. For example, if this is a
 bug report, describe the steps to reproduce the bug, the expected 
result, and the actual result.

You can use markdown to add formatting, links, emojis, and more. For more information, see "[Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github)."

![Screenshot of the new issue form, with a title and body filled in.](https://docs.github.com/assets/cb-66899/images/help/issues/issue-title-body.png)

## [Adding a task list](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#adding-a-task-list)

It can be helpful to break large issues into smaller tasks, or to 
track multiple related issues in a single larger issue. Add a task list 
to your issue by prefacing list items with `[ ]`. Reference 
existing issues by issue number or URL. You can use plain text to track 
tasks that don't have a corresponding issue and convert them to issues 
later. For more information, see "[About task lists](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-task-lists)."

![Screenshot of the new issue form, with the title and body filled in. The body includes the Markdown for a task list.](https://docs.github.com/assets/cb-80079/images/help/issues/issue-task-list-raw.png)

## [Adding labels](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#adding-labels)

Add a label to categorize your issue. For example, you might use a `bug` label and a `good first issue` label to indicate that an issue is a bug that a first-time contributor 
could pick up. Users can filter issues by label to find all issues that 
have a specific label.

You can use the default labels, or you can create a new label. For more information, see "[Managing labels](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/managing-labels)."

![Screenshot of the new issue form. In the right sidebar, the "Labels" section is outlined in dark orange.](https://docs.github.com/assets/cb-120199/images/help/issues/issue-with-label.png)

## [Adding milestones](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#adding-milestones)

You can add a milestone to track the issue as part of a date based 
target. A milestone will show the progress of the issues as the target 
date approaches. For more information, see "[About milestones](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/about-milestones)."

![Screenshot of the new issue form. In the right sidebar, the "Milestone" section is outlined in dark orange.](https://docs.github.com/assets/cb-120131/images/help/issues/issue-milestone.png)

## [Assigning the issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#assigning-the-issue)

To communicate responsibility, you can assign the issue to a member of your organization. For more information, see "[Assigning issues and pull requests to other GitHub users](https://docs.github.com/en/issues/tracking-your-work-with-issues/assigning-issues-and-pull-requests-to-other-github-users)."

![Screenshot of the new issue form. In the right sidebar, the "Assignees" section is outlined in a dark orange.](https://docs.github.com/assets/cb-119863/images/help/issues/issue-assignees.png)

## [Adding the issue to a project](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#adding-the-issue-to-a-project)

You can add the issue to an existing project and populate metadata for the project. For more information about projects, see "[About Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)."

![Screenshot of the new issue form. In the right sidebar, the "Projects" section is outlined in dark orange.](https://docs.github.com/assets/cb-120014/images/help/issues/issue-project.png)

## [Submitting your issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#submitting-your-issue)

Click **Submit new issue** to create your issue. You can
 edit any of the above fields after creating the issue. Your issue has a
 unique URL that you can share with team members, or reference in other 
issues or pull requests.

## [Communicating](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#communicating)

After your issue is created, continue the conversation by adding 
comments to the issue. You can @mention collaborators or teams to draw 
their attention to a comment. To link related issues in the same 
repository, you can type `#` followed by part of the issue title and then clicking the issue that you want to link. For more information, see "[Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github)."

![Screenshot of an issue comment. The header says "octocat commented now" and the body says "@hubot Do we also need to update the rocket logic?"](https://docs.github.com/assets/cb-24024/images/help/issues/issue-comment.png)

## [Next steps](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart#next-steps)

You can use issues for a wide range of purposes. For example:

- Tracking ideas
- Collecting feedback
- Planning tasks
- Reporting bugs

Here are some helpful resources for taking your next steps with GitHub Issues:

- To learn more about issues, see "[About issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues)."
- To learn more about how projects can help you with planning and tracking, see "[About Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)."
- To learn more about using issue templates and issue forms to encourage contributors to provide specific information, see "[Using templates to encourage useful issues and pull requests](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests)."
