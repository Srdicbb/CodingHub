# Linux Deployment

**Phase:** 3 - DevOps
**Status:** [ ] In Progress
**Priority:** Practical / Operational

---

## Current Knowledge

### Deploying a UI App on Linux using NGINX

#### Build on Development PC

**Step 1** – Navigate to the UI project directory and build the project

```bash
cd path/to/UI
npm run build
```

**Step 2** – This sructure is specific to Angular 17+ app. After build completes, the `/dist` folder will look like this:

``` bash
dist/
└── project-name/
	├── browser/ ← this is what you deploy
	├── prerendered-routes/
	└── 3rdpartylibraries/
```

**Step 3** – Copy to USB: For deployment, `index.html` must be in the root of the folder you will copy to Nginx. Copy everithing from project-name folder to USB drive, also keep in mind all files inside `browser/` should be in the root of your USB drive.

#### Deploy on Linux Mini PC (Production)

**Step 1** – Install Nginx *(only needed the first time)*:

```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl status nginx             # check if installed and running
```

**Step 2** – Mount the USB drive and navigate to it:

```bash
lsblk                                   # find the USB disk name
cd /media/tvoj_username/disk name       #location to the USB disk
sudo mount /dev/sdX1 /mnt/usb           # mount it (replace sdX1 with actual disk)
cd /mnt/usb
```

**Step 3** – Copy files to Nginx web root:

```bash
sudo rm -rf /var/www/html/*             # clear old files
sudo cp -r /mnt/usb/* /var/www/html/    # copy new build
sudo systemctl restart nginx            # restart nginx
```

**Step 4** – Allow HTTP traffic through firewall *(only if ufw is enabled)*:

```bash
sudo ufw allow 'Nginx HTTP'
```

---

### Deploying a .NET App on Linux

---

## Examples / Notes

<!-- Commands, config files, service setup, etc. -->

---

## Questions / Confusions

<!-- Anything you're not 100% sure about yet -->
