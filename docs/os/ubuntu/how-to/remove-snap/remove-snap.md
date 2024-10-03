# How to Remove Snap in Ubuntu

## Disclaimer

Removing `Snap` is perfectly safe as of 22.04 but may lead to unwanted behaviour.

## Steps

* First, list down the installed snaps in the system

```bash
snap list
```

* For each Snap listed, remove and purge it

```bash
snap remove --purge <<snap>>
```

* Finally remove the `snapd`

```bash
apt remove --purge snapd
```

* Updating Ubuntu may enable snap again. To disable it run the following command.

```bash
apt-mark hold snapd
```

* Delete the snap directory in all home directories

```bash
rm -rf /home/*/snap
```

* Some daemons have files in their home directories too. Use find and delete.

```bash
find / -type d -name snap
```

## References

1. <https://www.reddit.com/r/Ubuntu/comments/1chilj4/completely_remove_snap_from_ubuntu_2404>
