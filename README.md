# -Latex-Boilerplate_Paper / Poster

A quite nice Boilerplate/Template together with some Macros and ready-to-use set up surroundings for LaTeX. Document-Type "Article-Level", i.e. no "Book".<br/>
Fit for writing an Article-alike Manuscript (like scientific poster) or a Poster.

This one here is quite sophisticated. A simplified one can be found:<br/>
> [https://github.com/DenKrysos/-Latex-Boilerplate-Paper-Modest](https://github.com/DenKrysos/-Latex-Boilerplate-Paper-Modest "DenKr Latex Paper-Boilerplate Modest")
<br/>

Just saying, there is also another Boilerplate for Book-type Documents:<br/>
> [https://github.com/DenKrysos/-Latex-Boilerplate-Book](https://github.com/DenKrysos/-Latex-Boilerplate-Book "DenKr Latex Book-Boilerplate")

## Description
* Layout and Skeleton Setup is well separated from the content
  * Layout can be easily swapped by changing only a configuration-value inside the file "2ProjectSetup.tex"
  * Various different Layouts are already prepared ready-to-use. (Each in an own folder inside "./0organization/2layout/")
  * The same way, additional layouts can be used: Create a new directory there, mimic the file-tree of one existing layout and then use the name of your layout-folder as value for "\DenKrLayout"
* Paper or Poster
  * Provides required layout Set-up for Papers (Multiple different layouts for manuscripts)
  * But also for a Poster (One dedicated framework for typesetting a Poster)
* Set up for Biblatex
* Set up for glossaries (requires external builder, pretty easy to configure)
* The File "2ProjectSetup.tex" is interesting in general. Has various Values for configuration.
* All the layout-regarding stuff is inside "0organization"
  * There, mostly only one thing has to be touched: Choose your preferred Author-Format (different Files for different Formats) and also write the correct Authors themselves there
* "2ProjectSetup.tex" has some Makros set-up to unify directory-references. For easy use, just leave it as is and use the Macros when e.g. including files out of the set folders.
* The structuring of your Project Skeleton starts from "3Disposition.tex". The rest happens inside the directory "4chapter".
  * I suggest to just leave "3Disposition.tex" as is and work inside "4chapter". But if you prefer, changing "3Disposition.tex" is fine as well.


## Some Features:
* DenKr_Comments: I've created an own Feature for colorful Comments during Working-State, e.g. for communicating with co-authors on collaborative work or to just leave notes, remarks, ToDo-Marks.
  * Adjustment of the Comments (Adapting to participating People; changing the displayed Name-Abbreviation or the color; changing the Macro-Name; or just adding more Comment-Macros) is performed in the File "./1supply/DenKr_commetnts.tex". Adjust to your needs, the existing entrys may well serve as template for how to do this.
  * Showing these comments in the compiled document can be turned on and off. For that the Value "\DenKrCommentsUsage" inside the "./2ProjectSetup.tex" is responsible.
  * After finishing writing, set this to 0 and you can be sure that none are left over in the final document.

* Macro to automatically include a "standalone tikz picture" with the best options.
  * Ensures, that the picture does not exceed the page/environment size on any side
  * Allows several options, like rotate, crop, insert as plain-text (render together with main file) or as pre-rendered pdf-picture.
  * If desired the pictures can be included as "buildnew". Means: They are only rendered new, if they changed. Saves a lot of compilation time.
  * Allows explicit scaling and positioning
* tikz:
  * Some 3-Dimensional Graphic Generation done in tikz
  * Flow Graph Toolset

* For sure some more features I can't quite recall. That thing is huge...


### Templates, Examples
Inside the Directory "./0rganization/1main/8templates/example_chapter/" are some files that show examples on how things can be done.
1. One for a Article/Paper
    * Syntax e.g. for inputting Standalone-TikZ Pictures
2. One for a Poster
    * Syntax for placing the Boxes
<br/>

A File that provides Templates for proper Bibtex-Entry-Definition is
  > "./0organization/1main/8templates/literature_1Template.tex"


## Modus Operandi, Nodes, Tipps, Tricks

### Preprint
"When to use and when not"<br/>

This again also connects back to this *preprint* issue.<br/>
There are conferences/journals/... for which I have proper layouts prepared and others for which I haven't. Sometimes they only want a compiled .pdf; sometimes they want the editable source submitted; sometimes the source-project shall even follow a certain file-structure, which then mostly means having everything inside one File.<br/>

Nonetheless, I am doing it the following way: I do always write manuscripts using this, my sophisticated Boilerplate. Because then, I am flexible in doing everything. Here again it comes in handy that with this Boilerplate, the content and all the LaTeX Overhead are well separated.
So when finished with the manuscript, I can easily compile a preprint and a version for submission. Even when the submission requires a certain file-structure, then I create a second Project, set this up for the submission guidelines and copy the content over (which is quick and easy, because it is in this separate files in the "4chapter"-Directory).<br/>
That might be not the most elegant solution, conceivable in principle, because then you have two distinct copies of your content, but in such a case that cannot be avoided anyways. Because a preprint has to be done and this cannot be performed within the submission-project. Hence, one may as well directly start with the "preprint-Version", which can be done through my Boilerplate and then only for final submission, the two Projects diverge.<br/>
When then coming back for revising the manuscript after review, I do prepare the follow-up version again in the preprint-document and then update the submission-version.


## Project Divergence
A lot of Files in here are linked from other Projects.<br/>
When working "Git-based", this won't be an issue anytime, because then already distinct standalone copies of these files are created.<br/>

But when working with an Overleaf-Project that you created as a Copy of this Overleaf-Project directly inside Overleaf, the files are still links. This is partly cool, because then you always have updates right at hand, whenever I perform such. But on the other hand, sometimes you might want to change things, like Package-Options. And it appears like that's not possible, because you can't modify linked files.<br/>
In that case, create the project divergence yourself: Go into the file in question (e.g. "./0organization/1main/2includes/packages/figure_subfigure_caption.tex"), copy its content, remove (delete) the linked file, create a new one with the same file-name and paste the content into. Then adjust to your needs (e.g. modify the caption formatting).


### Recommendation
Actually, for most cases, I would recommend performing a "Deep Copy" of the Project. I.e. not taking over the links referring to files in other projects, but having own duplicates so that the new Project works fully standalone.<br/>

You can achieve this for example via downloading the Project as .zip from the GitHub-Repository, then in Overleaf choose "New Project -> Upload Project" and give the downloaded .zip.

#### Deep Copy'd Overleaf-Project
Now it might become a little confusing, but bear with me, it actually makes it easier for all of us, including you. Above, I talked about stuff like "originating Overleaf Project" and "linked to GitHub" and "linked Files".<br/>
Actually, all that stuff hasn't to concern you at all. I found a solution to make it most easy for third users of my Boilerplate. I created yet another Overleaf-Project!<br/>
That means, nobody beside me has access to actual source of this Boilerplate (which is the Overleaf Project in first instance). A second Overleaf-Project now originates form the GitHub-Repo (which in turn is a Fork of the actual origin) and has the Name-Suffix "-DC" (for Deep-Copy).<br/>
So it is a uni-directional Sequence of Pull-instances, where one depends on the previous that looks like
> [Overleaf-Origin-Project] -> [GitHub-Repository] -> [Overleaf-Project-DeepCopy]

By this, the Overleaf-Project for access by others has just ordinary hard-copies of the initially linked files, i.e. works standalone and after fork is independent of things I might be doing sometime later on.<br/>
The ReadOnly-Link to the Overleaf-Project for further Use:<br/>
> [https://www.overleaf.com/read/qfpqgxzmryqt](https://www.overleaf.com/read/qfpqgxzmryqt "DenKr Latex Paper/Poster-Boilerplate - Overleaf ReadOnly-Link to Deep-Copy'd Project")
<br/>

> What we are now all doing, is either:
> 1. Work with the GitHub-Repository: Download and work locally with your own LaTeX Editor or Download as .zip and use this with "Upload Project" to create an Overleaf-Project
> 2. Take the ReadOnly-Link to the Deep-Copy Overleaf-Project. By that, this Project is added to your Account (as Read-Only). And then just copy this Project to have a a detached standalone new one, fully free to your disposal.
<br/>

Note to myself: The Deep-Copy Project is to only be pulled, never make changes inside that project or push from it. Only copy


## Overleaf
The Basis for this is actually an Overleaf Project. This is linked with a GitHub-Repository and every now and then synchronized to this. So the Git-Repo is actually "only" a fork of the Overleaf-Project.

The TikZ-relating Files are actually not residing within this Overleaf-Project ("3settings", "8templates", "2layout/tikz_standalone") but inside an own, disjoint Project. These files from another Project are then linked to the Boilerplate.<br/>
So inside the Overleaf-Project, these files are links. But when synchronizing to the GitHub-Repo, copies are created that are then factually existing own files.