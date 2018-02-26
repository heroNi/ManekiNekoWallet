**1. Clone wallet sources**

```
git clone https://github.com/cryptonotefoundation/cryptonotewallet.git
```

**2. Modify `CryptoNoteWallet.cmake`**
 
```

set(CN_PROJECT_NAME "manekineko")
set(CN_CURRENCY_DISPLAY_NAME "ManekiNeko")
set(CN_CURRENCY_TICKER "MaNe")

```

**3. Set symbolic link to coin sources at the same level as `src`. For example:**
** Alternative method should be used unless you know that all git clone files were successfull in carrying over as often the pull may not clone completely.
```
ln -s ../coind_dir_name name_of_symbolic_link
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/heroNi/Maneki-Neko-coin mane
```

Replace URL with git remote repository of your coin.

**. Wallet src update**
Verify that the CMAKELISTS TXT is point to the right directory
in the alternative example it is pointing to mane 

   if not pointing to mane, update

nano or vi into CMakeLists.txt and update paths to point to your directory name 

**4. Build**


```
mkdir build && cd build && cmake .. && make
```
