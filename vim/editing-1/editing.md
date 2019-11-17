# Find / Replace

### Remove all lines that contain a specific string

To remove any lines that contain a string you will want to use the global search `:g` and the `d` flag for delete.

```text
:g/<string>/d
```

{% hint style="info" %}
This will remove the entire line not just the string passed.
{% endhint %}

#### Example

I often see where people use the -p flag with the password passed directly into the command when doing mysql queries on servers. This is something that you shouldn't do. I don't want the passwords in the bash history so I remove them.

{% code title="~/.bash\_history" %}
```text
ls -la
cat ~/.zshrc
mysql -u root -p TeHpASSword
tar -zcf dump.tar.gz dump.sql
mysql -u root -p TeHpASSword
```
{% endcode %}

After opening in VIM I would do the following:

```text
:g/mysql/d
```

Which would result in the file contents being:

{% code title="~/.bash\_history" %}
```text
ls -la
cat ~/.zshrc
tar -zcf dump.tar.gz dump.sql
```
{% endcode %}

Now you can just save and close with `:wq` and now the mysql references are no longer in the history.

{% hint style="info" %}
You will need to close and reopen terminal for it to take place and if you are using zsh you will want to check the ~/.zsh\_history file.
{% endhint %}



