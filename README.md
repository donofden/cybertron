[![HitCount](http://hits.dwyl.io/donofden/cybertron.svg)](http://hits.dwyl.io/donofden/cybertron)

# cybertron

This is MY VM where Im playing around with Ansible and understand the IT automation deploy.

Ref for more information: https://docs.ansible.com/ansible/ https://www.ansible.com/

## So why i named my VM as Cybertron?

Cybertron is the home planet of the Transformers and (usually) the body of their creator, Primus. Cybertron is (almost always) a shining metal, technological world; a planet of towering future cities without end and vast metallic plains, spiraling metal mountains and bottomless neon-lit chasms.

By the words of it, you might have understood, VM is Cybertron, Primus is ME {:D}, My repos and other stuffs installed in cybertron are shining metal, technological world

## The Goal

The idea is to run achieve the following:

- Install Ubuntu and required dependencies for all my repos
- Install Jenkins and configure jobs
- Build code from Git

Can get Jenkins Admin password After successful completion:

```bash
 ______________________________________________ 
< TASK [jenkins : Print init password Jenkins] >
 ---------------------------------------------- 
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||

ok: [default] => {
    "result.stdout": "1f65adace245428b9ef61c198d9eb57e"
}
 _____
```
