# LVM backup made easy

This wrapper script creates temporary snapshot of a logical volume, sends it to
borg backup repository and finally destroys the snapshot.
The snapshot is automatically mounted before backup and unmounted after.

This script should be run as root (or via sudo, or possibly via sudo -E).

# USAGE:

    lvm2borg [--progress] my_vg/lv_name [fstype]

See configuration variables inside the script.

# EXAMPLE:

    lvm2borg pve1/root ext4
