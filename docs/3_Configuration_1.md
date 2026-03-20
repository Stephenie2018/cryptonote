First, create a unique name for your cryptocurrency that aligns with your theme and philosophy. It is highly recommended to use a search engine to ensure this name isn't already in use. 

For this project, we will use the name **"Aura"**.

You need to configure this name in two specific files:

#### 1. `src/CMakeLists.txt`
In this file, locate the following line (usually found near the bottom):

```cmake
set_property(TARGET daemon PROPERTY OUTPUT_NAME "furiouscoind")
```
Change furiouscoin to your chosen name. The letter "**d**" at the end stands for **daemon** (a background process); make sure to keep it. For example: "**aurad**".

>If you can't find this line, ensure you have opened the CMakeLists.txt file specifically located in the src folder, as there may be multiple files with this name in the project.

#### 2. `src/CryptoNoteConfig.h`
Open this file and go to line **76** (or search for the `CRYPTONOTE_NAME` constant). Replace the default name with your chosen name, but **do not add the "d" at the end here.**

**Original:**
```c
const char CRYPTONOTE_NAME[] = "furiouscoin";
```
**Updated:**
```c
const char CRYPTONOTE_NAME[] = "aura";
```
