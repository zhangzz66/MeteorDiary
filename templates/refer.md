## 🏷 **链接“ {{.title}}”的内容**{: style="background-image: linear-gradient(to right, var(--b3-theme-primary), var(--b3-theme-error)); -webkit-background-clip: text; color: transparent;"}
{: id="20210129211237-b25zmo0"}

!{{SELECT * FROM blocks WHERE markdown LIKE '%{{.id}}%' and root_id != '{{.id}}'}}
{: id="20210129211237-jh17cgr" updated="20210222212835"}

## 🏷 **提及“ {{.title}}”的内容**{: style="background-image: linear-gradient(to right, var(--b3-theme-primary), var(--b3-theme-error)); -webkit-background-clip: text; color: transparent;"}
{: id="20210117201946-iesarol"}

!{{SELECT * FROM blocks WHERE content LIKE '%{{.title}}%' and root_id != '{{.id}}' and markdown not LIKE '%{{.id}}%'}}
{: id="20210129211237-bmqibm2"}

{: id="20210223211359-fj93gtc"}


{: id="20210222101728-4c0hvv9" type="doc"}
