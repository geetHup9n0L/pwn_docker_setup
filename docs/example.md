### Example of creating docker's container with dbg tools inside:

* unzipped files provided from challenge:
<img width="808" height="70" alt="image" src="https://github.com/user-attachments/assets/89251fff-4283-4304-97dc-2b2b9ac08a0d" />

* initial `Dockerfile` config:
<img width="815" height="307" alt="image" src="https://github.com/user-attachments/assets/b5d3f2c9-75a2-416a-bbb7-b4554dc42ca6" />

* build that server-identical image:
<img width="812" height="380" alt="image" src="https://github.com/user-attachments/assets/45202186-eb7e-409c-813c-93be1495c7f3" />

* create a `Dockerfile.debug`:
<img width="812" height="50" alt="image" src="https://github.com/user-attachments/assets/5c3d5fb3-3edb-49c9-883a-45c4a3a166ce" />
<img width="715" height="541" alt="image" src="https://github.com/user-attachments/assets/bb14ea9a-7a9e-4a48-8108-92a43e27db97" />


* build the extended image (dbg version):
<img width="815" height="308" alt="image" src="https://github.com/user-attachments/assets/7a67642b-03c1-4642-82a6-36d30c283e4b" />

* now we run the debug container:
<img width="810" height="180" alt="image" src="https://github.com/user-attachments/assets/6366f63f-7af3-4745-8cc4-fa7b86aac2f0" />

* check gdb-pwndbg:
<img width="814" height="402" alt="image" src="https://github.com/user-attachments/assets/68f9b1f6-6c0f-4233-bb3e-916dae0df1f3" />
