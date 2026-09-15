# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**:Thuleer R
* **Register Number**: 212225230285
* **Date of Submission**: 05-09-26

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1.Created an EBS volume in the same Availability Zone as the EC2 instance and selected the required volume size and type.

2.Attached the newly created EBS volume to the running EC2 instance and connected to the instance using SSH.

3.Formatted the attached volume with the ext4 file system and mounted it to the /data directory.

4.Created sample files in the mounted EBS volume, rebooted the EC2 instance, and verified that the stored data was still available.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1824" height="866" alt="EX4 1" src="https://github.com/user-attachments/assets/80d408f8-7b9c-4d1c-9183-d119d8754c38" />


### Screenshot 2: EBS Volume Attached to EC2

<img width="1920" height="1200" alt="EX4 2" src="https://github.com/user-attachments/assets/3a8d685d-41a5-42d5-9ea3-371c585a04c3" />


---

### Screenshot 3: Mounted Volume with Data

<img width="1920" height="1200" alt="EX4 3" src="https://github.com/user-attachments/assets/1e50587c-7f44-4d53-9d46-1f0fcb1f815d" />


---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
