This script allows you to mass-delete your Steam profile comments without logging in or any other bullshit.

Script:
<details>
  <summary>Click to expand</summary>
  
    while (true) {

        const comments = document.querySelectorAll(
            '.commentthread_comment_actions .actionlink'
        );

        if (!comments.length) {
            await new Promise(r => setTimeout(r, 2000));
            continue;
        }

        for (const a of comments) {
            try {
                eval(a.href.replace('javascript:', ''));
                await new Promise(r => setTimeout(r, 300));
            } catch(e) {}
        }
    }
} nuke();

</details>

How to use it?
go to your https://steamcommunity.com/my/allcomments
Press f12 if using chrome, open console type "allow pasting" paste the code and there it goes :) 
