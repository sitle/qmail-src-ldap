Install qmail-ldap from source on Debian 7 or Ubuntu 14.04

## Initial configuration

```bash
mkdir -p /var/qmail/alias
groupadd nofiles
useradd -g nofiles -d /var/qmail/alias alias
useradd -g nofiles -d /var/qmail qmaild
useradd -g nofiles -d /var/qmail qmaill
useradd -g nofiles -d /var/qmail qmailp
groupadd qmail
useradd -g qmail -d /var/qmail qmailq
useradd -g qmail -d /var/qmail qmailr
useradd -g qmail -d /var/qmail qmails
groupadd vgroup
useradd -g vgroup vuser
```

## Dependencies

```bash
apt-get install -y libldap2-dev libssl-dev
```

## To compile

```bash
git clone https://github.com/sitle/qmail-src.git
cd qmail-src
make setup check
```
