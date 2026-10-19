# SUT (Super USB Tool) - Iteration 1

## Required software.

* **YUMI-UEFI-0.0.4.6**
* **PortableApps.com Platform**
* **Rufus**
* **Universal shortcut folder**
* **GodMode**

---

## Execution Steps

### Suggestion Step: Prep the Local Source
1. Create A folder on your desktop and name it something like USB tool.
2. Inside Your folder, make a couple subdirectories to organize the files you're going to download.
   * Set up files.
   * Other files
   * Image files.
3. Download and place executables in Subdirectories:
   * `YUMI-UEFI-0.0.4.6.exe`
   * PortableApps.com Platform Installer
   * Rufus

---

### Step 1: Format Drive & Build Bootable Base
1. Format target USB drive (**Do NOT format inside YUMI.**)as **Large FAT32**, 
    I use Rufus to create a free DOS boot drive And then delete all of the files 
	Rufus creates except for the icon.
2. Launch `YUMI-UEFI-0.0.4.6.exe` 
3. Select target USB drive letter.
4. Leave internal format option **UNCHECKED**.
5. Select target Image
6. Click **Create**.
7. Repeat to add additional Images with format option unchecked.

---

### Step 2: Build Windows Toolbox
1. Launch PortableApps installer
2. Select **Portable Install** and set target to root of USB drive.
3. Launch PortableApps from USB drive and install desired applications.

---

### Step 3: Add Custom Tools
Place non-portable EXEs, scripts, batch files, and standalone utilities in A directory you create the on USB drive.

---

### Step 4: Create Shortcut
1. Add a directory of universal shortcuts.(Instructions to make one are within this GitHub.)
2. Create a folder.Paste this into the folder's name 
   `GodMode.{ED7BA470-8E54-465E-825C-99712043E01C}` and press enter.


---

## SUT Backup (Iteration 2)

### Hardware Specs
* **Drive:** 512GB M.2 2230
* **Enclosure:** Minimal appropriate size SSD aluminum USB A enclosure

### Execution Steps
1. Insert UST.
2. Open Rufus and save image of SUT as an ISO
3. Connect new drive. 
4. Open Rufus select new drive, and flash target **ISO**.
5. Expand primary boot partition to desired size.
6. Format remaining unallocated partition as **NTFS** for RescueZilla backup images.

---

## SUT Large Backup (Iteration 3)

### Hardware Specs
* **Drive:** 1TB M.2 2280 NVMe SSD
* **Docking Station:** Blueendless Model MC403 M.2 SSD Docking Station
* **Enclosure:** Multifunctional USB 3.2 Gen 2 (10Gbps) 4-in-1 M.2 SSD Enclosure (with SD/TF card reader)

### Execution Steps
1. Install 1TB M.2 2280 NVMe SSD into docking station or enclosure.
2. Flash base ISO via Rufus.
3. Enlarge primary utility partition.
4. Format second partition as **NTFS** for RescueZilla backup storage.