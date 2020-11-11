# **:triangular_flag_on_post: WEBHOOKS** (version 1)



---

## **:package: Main tools used**

- [x] child_process
- [x] crypto
- [x] http

---

## **:wrench: Developer usage**

### **Set up project**

- Make sure your poject is cloned and installed and you have created a process
- Go to your Github Repo/settings/webhooks
    - Add Webhook
        - Payload URL: http://YOUR_IP:YOUR_OPEN_PORT
            - **Not the same open port as your project**
        - Content Type: application/json
        - Secret: Generate from https://randomkeygen.com/
            - Make a note of this, you will need this soon
- Choose a folder in your system and switch in `cd [folder path]`
- Clone the repo in your folder path
- Paste the secret you just generated into "INSERT YOUR SECRET HERE"
- Replace REPO_LOCATION with your project repo location
- Replace PROCESS_NAME with your process name
- Replace port with your open port (from  the webhook)

---

### **Installation**

In order to install the project and all dependencies, enter in the project folder and run `npm install`

---

### Setup the service

```bash
cd [folder path]
sudo cp webhook.service /etc/systemd/system/SERVICE_NAME.service
```
- Replace port number with the port number defined in your WEBHOOK_NAME.js file
- Replace WEBHOOK_LOCATION with the location of your WEBHOOK_NAME.js file

```bash
sudo systemctl enable SERVICE_NAME.service
sudo systemctl start SERVICE_NAME
sudo systemctl status SERVICE_NAME

```


---


## **:handshake: Contributing**

- Fork it!
- Create your feature branch: `git checkout -b my-new-feature`
- Commit your changes: `git commit -am 'Add some feature'`
- Push to the branch: `git push origin my-new-feature`
- Submit a pull request

---


### **:anger: Troubleshootings**

This is just a personal project created to simplify my working life, it may or may
not be a good fit for your project(s).

---

### **:heart: Show your support**

Please :star: this repository if you like it or this project helped you!\
Feel free to open issues or submit pull-requests to help me improving my work.


---


Copyright Rohan Krishna © 2020 
