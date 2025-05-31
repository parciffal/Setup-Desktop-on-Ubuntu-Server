# Setup-Desktop-on-Ubuntu-Server
The way to settup desktop on ubuntut server that worked for me

# How to Install Ubuntu Desktop with VNC Access on Ubuntu Server

Follow these steps to set up an Ubuntu Desktop environment with VNC server access on an Ubuntu Server.

---

## 1. **Install Tasksel and Display Manager**

```bash
sudo apt update
sudo apt install tasksel
sudo apt install slim
```

---

## 2. **Install Ubuntu Desktop Environment**

Launch `tasksel`:

```bash
sudo tasksel
```

* In the list, move to **Ubuntu Desktop** using the arrow keys.
* Press **Space** to select it.
* Press **Tab** to move to `<OK>`, then **Enter** to confirm.

---

## 3. **Install TigerVNC Server**

```bash
sudo apt install tigervnc-standalone-server
```

---

## 4. **Create a New User**

```bash
sudo adduser {name}
```

* When prompted, enter the password:

---

## 5. **Switch to the New User**

```bash
su - {name}
```

---

## 6. **Start VNC Server**

```bash
vncserver -localhost no
```

* When prompted, set the VNC password:


---

## 7. **Done!**

You can now connect to your server’s VNC session using a VNC client.

---

**Note:**

* You can customize usernames and passwords as needed.
* By default, VNC starts on port `5901` (display `:1`).
* To stop the VNC server, run:

  ```bash
  vncserver -kill :1
  ```

---
