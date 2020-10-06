## 5. Markdown Cheat Sheet

This list is incomplete by far but you will get the idea. :smile: :smiley:

On the Internet, you can find a number of extensive Markdown cheat sheets:

- [Azure DevOps Markdown cheat sheet](https://go.microsoft.com/fwlink/?linkid=851652)
- [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Azure DevOps Markdown cheat sheet](https://go.microsoft.com/fwlink/?linkid=851652)

### Basic Elements

| Element       | You type                                        | You get                                                | Comment                                                                                 |
| ------------- | ----------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| Headings      | `# Bla`<br/>`## Bla`<br/>`...`<br/>`###### Bla` | 6 heading levels                                       |
| Bold          | `__Bold__`                                      | __Bold__                                               | `**Bold**` will also work                                                               |
| Italic        | `_Italic_`                                      | _Italic_                                               | `*Italic*` will also work                                                               |
| Unorderd list | `- item 1`<br/>`- item 2`<br/>`- item 2`        | <ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | also works with `*` instead of `-`                                                      |
| Orderd list   | `1. item 1`<br/>`1. item 2`<br/>`5. item 2`     | <ol><li>item 1</li><li>item 2</li><li>item 3</li></ol> | the value of numbers does not matter                                                    |
| Text buttons  | `<kbd>Jump!</kbd>`                              | <kbd>Jump!</kbd>                                       | can look better than `Jump!` (depends on MD implementation)                             |
| Line break    | `Line 1<br/>Line 2`                             | Line 1<br/>Line 2                                      | can sometimes come in handy                                                             |
| Blockquotes   | `> Line 1`<br/>`> Line 1`                       | <blockquote>Line 1<br/>Line 2</blockquote>             | put a blank line between blockquoted lines to separate them into two blockquoted blocks |

### Horizontal Rule

Type three or more of `-`, `*` or `_`. E.g. `---` produces a full length horizontal line:

---

### Links

You type `[Some nice text to describe the URL](https://blabla.com/some-bla-uri)` and that produces this link: [Some nice text to describe the URL](https://blabla.com/some-bla-uri).

If you don't want to hide the link by some description, just enclose it in angle brackets. E.g. type `<http://localhost:3000>` to see this: <http://localhost:3000>.

### Images

#### If working locally

Place an image, e.g., `repo-link.png` to some subfolder, e.g., `images` relative to your markdown file. Then type `![repo link](images/repo-link.png)` and you get to see this:

![repo link](images/repo-link.png)

#### If working with Azure DevOps Wikipages

Just copy the image and paste it inside your wiki text (or drag it onto the page). This will produce this kind of link with an auto-generated hash string:

`![diagram-FCM.png](/.attachments/diagram-FCM-c99c33b9-2d44-40a0-b153-273c338873a3.png)`

#### An image can be a link in itself

Just use the image link as the description for the link: `[![repo link](images/repo-link.png)](http://madrus4u.com/demo-markdown/)`. You get to see this:

[![repo link](images/repo-link.png)](http://madrus4u.com/demo-markdown/)

Try to hover over the image and you will see the URL appear at the left bottom. If you click on the link, it will open the URL in your default browser.

### Code highlighting

Code highlighting is very important for IT-people. The nice thing about Markdown is that it can produce language syntax highlighting. For that backticks are used: `` ` ``.

#### Inline code with no syntax highlighting

If you want to include a short string of code inside a text line, include the code string in single backticks, like this: `` `using System;` ``. Markdown will be translated into `using System;` string.

#### Code blocks with syntax highlighting

If you wish to include a beautiful piece of code inside your Markdown document, use __fences__, i.e. triple backticks `` ``` ``  and specify the language of the code snippet you are using. Markdown understands almost any language out there, e.g. `C#/CSharp`, `PowerShell`. `SQL`, `JavaScript`, `TypeScript`, `Yaml`, `Markdown`, `Bash`, `JSON`, `XML`, etc. Use `text` or `none` if you want plain text without any syntax highlighting, e.g. for log snippets. Use `bash` for `Bash` and `CMD`.

It is a tradition to insert one space between fences and the language name and the name is lowercase.

Here is the full C# snippet example (see the source markdown file for the exact syntax):

``` csharp
using Microsoft.AspNetCore;
using Microsoft.AspNetCore.Hosting;

namespace Fh.Xxx.Yyy.Lmb
{
    /// <summary>
    /// The Main function can be used to run the ASP.NET Core application locally using the Kestrel webserver.
    /// </summary>
    public class LocalEntryPoint
    {
        public static void Main(string[] args)
        {
            BuildWebHost(args).Run();
        }

        public static IWebHost BuildWebHost(string[] args) =>
            WebHost.CreateDefaultBuilder(args)
                .UseStartup<Startup>()
                .Build();
    }
}
```

### Some more advanced Markdown elements

#### Inline HTML

It it often possible to place raw HTML code inside the Markdown file. It is just not 100% format safe. Do that at your own risk.

#### Tables

This file uses a table syntax. It is quite tedious work to get the rows and columns right. I have left explanation of that out of the demo.
