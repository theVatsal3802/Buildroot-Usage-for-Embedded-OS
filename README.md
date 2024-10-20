# Overview of the steps to be followed for modifying and compiling buildroot for Raspberry Pi 3

By:
- Vatsal Adhiya (24VS60R26)
- Himanshu Likhar (24CS60R43)

## Steps to be followed:
- Download the tarball from [Buildroot Website](https://buildroot.org).
- Unzip the tarball using the following command:
```
tar -xf buildroot-2024.02.6.tar.gz
```
- Open the unzipped folder in the terminal and run the following command as shown below and copy the name for the configuration for `raspberry pi 3`:
```
make list-defconfigs
```
https://github.com/user-attachments/assets/991bbe1a-4b5d-4963-b2be-5e72d163184e
- Next, we select the `raspberry pi 3` configuration as follows and then open `menuconfig` for modifications:
```
make raspberrypi3_defconfig
make menuconfig
```
https://github.com/user-attachments/assets/a28a6a6e-d67e-4ece-9695-ea6d92a394bf
- Then, we perform all the required modifications as follows:
- Task 1: Display names in System Banner

https://github.com/user-attachments/assets/c5222b8f-3090-4952-b042-e85e9e151036
- Task 2: Enable `nano` text editor for convenience

https://github.com/user-attachments/assets/0204be5f-1ab1-4e19-ba0e-e0e2d2880371
- Task 3: Set `root` password for system security

https://github.com/user-attachments/assets/69d3cc34-5295-4e85-bdb0-7f6a12b936c2
- Task 4: Enable SSH Server capabilities

https://github.com/user-attachments/assets/0cfd2518-2946-48d8-9eab-327503385aae
- Task 5: Enable netwrok utilities by selecting `Net-tools`

https://github.com/user-attachments/assets/81b1d47b-a0de-40f6-9e9e-2f8a1ff0aa31
- After all these tasks are completed, we need to compile and generate an image that can be used on `Raspberry Pi 3`. For that, we use the following command:
```
make all -j8
```
This will compile and store the generated image in the `output` folder. (Note: this operation takes a lot of time approx. 1.5 hours).
This completes the build process for Raspberry Pi 3.
