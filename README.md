# Gentoo overlay

## Install as local overlay

Use the following command:

```bash
sudo tee /etc/portage/repos.conf/andrew-aladev.conf << END
[andrew-aladev]
location = /var/db/repos/andrew-aladev
sync-type = git
sync-uri = https://github.com/andrew-aladev/overlay.git
END
```

## Install as layman overlay

Use the following command:

```bash
sudo layman -o https://raw.githubusercontent.com/andrew-aladev/overlay/master/repositories.xml -f -a andrew-aladev
```

## Usage

Overlay will be updated during global sync.

```bash
emerge --sync
```

Than you can install some package:

```bash
emerge -v category/name
```

## License

MIT license, see LICENSE and AUTHORS.
