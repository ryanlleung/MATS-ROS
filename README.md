# MATS-ROS

A small working repository for getting started with ROS2 Humble on Ubuntu 22.04.
It currently contains setup notes for a VirtualBox-based development environment
and a minimal Python test script (`test.py`) for checking that the Python
plotting stack works.

## Repository contents

| File        | Description                                                   |
|-------------|---------------------------------------------------------------|
| `README.md` | This file: overview and installation guide.                   |
| `test.py`   | Minimal NumPy + Matplotlib script that plots a sine curve.    |
| `LICENSE`   | MIT License.                                                  |

## Installation with VirtualBox

These steps set up ROS2 Humble on Ubuntu 22.04.1 running in a VirtualBox VM.

1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
2. Download the [Ubuntu Desktop](https://ubuntu.com/download/desktop) ISO image.
3. Create a new virtual machine in VirtualBox. Manually select the ISO file path
   for both the main Ubuntu installer and the Guest Additions.
4. If `sudo apt update` fails after a fresh installation because your user is
   not in the sudoers file, see
   [this Unix & Linux Stack Exchange answer](https://unix.stackexchange.com/questions/179954/username-is-not-in-the-sudoers-file-this-incident-will-be-reported).
5. Update all packages:

   ```bash
   sudo apt update
   sudo apt upgrade
   ```

6. If the Snap Store needs upgrading:

   ```bash
   sudo killall snap-store
   sudo snap refresh snap-store
   ```

7. Save a VirtualBox snapshot of the VM at this point, so you can roll back if
   a later step goes wrong.
8. Install VS Code from the Snap Store.
9. Install Anaconda (see the [official Linux installation guide](https://docs.anaconda.com/anaconda/install/linux/)).
10. Restart the VM so that Anaconda is picked up by VS Code.

## Running `test.py`

`test.py` creates the integers 0 to 9 with NumPy, computes their sine, and
displays the result as a line plot with Matplotlib. It is a quick way to check
that NumPy, Matplotlib and a graphical display are working in your environment.

Requirements: Python 3 with `numpy` and `matplotlib` installed (both are
included in the default Anaconda distribution).

```bash
python test.py
```

A Matplotlib window showing the sine plot should open. Close it to end the script.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
