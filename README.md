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
ln -s ../cryptonote cryptonote
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/heroNi/Maneki-Neko-coin cryptonote
```

Replace URL with git remote repository of your coin.

**4. Build**

```
mkdir build && cd build && cmake .. && make
```
