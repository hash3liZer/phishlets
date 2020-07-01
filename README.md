# Phishlets
Phishlets are the configuration files in **YAML** syntax for proxying a legitimate website into a phishing website. They are the building blocks of the tool named `evilginx2`. https://github.com/kgretzky/evilginx2. 

## Usage
These phishlets are added in support of some issues in evilginx2 which needs some consideration. All the phishlets here are tested and built on the modified version of evilginx2: [https://github.com/hash3liZer/evilginx2](https://github.com/hash3liZer/evilginx2). If you find any problem regarding the current version or with any phishlet, make sure to report the issue on github. 

### Google
These are some precautions you need to take while setting up google phishlet. 
<ul>
    <li>Make sure Your Server is located in United States (US)</li>
    <li>Make sure you are using this version of evilginx: <a href="https://github.com/hash3liZer/evilginx2">https://github.com/hash3liZer/evilginx2</a></li>
    <li>If you server is in a country other than United States, manually add the `accounts.gooogle.[country code]` entry in proxy_hosts section, like this: </li>
</ul>

```
{phish_sub: 'accounts-pk', orig_sub: 'accounts', domain: 'google.pk', session: true, is_landing: false, auto_filter: false}
```

### Buggy Phishlets
The following sites have built-in support and protections against MITM frameworks. Hence, there phishlets will prove to be buggy at some point. 
<ul>
    <li>Google</li>
    <li>ICloud</li>
</ul>
If you beleive you have a solution, open a pull request. 

## Contribution
<ul>
    <li>Report Bugs.</li>
    <li>Use the phishlets in your projects.</li>
    <li>Give new ideas of the phishlets.</li>
    <li>Fork it!</li>
</ul>
