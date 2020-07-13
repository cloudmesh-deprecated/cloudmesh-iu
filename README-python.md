# Install from source

## Python 3.7

```bash
mkdir -p $HOME/local/source
cd $HOME/local/source
cd Python-3.7.8
./configure --prefix=$HOME/local/python/3.7.8 --enable-optimizations
make
make install
ls $HOME/python/3.7.8/bin/
```

Installation will be slw as after the compile over 400 tests are run

## Python 3.8

``` bash
mkdir -p $HOME/local/source
cd Python-3.8.3
./configure --prefix=$HOME/local/python/3.8.3 --enable-optimizations
make
make install
ls $HOME/python/3.8.3/bin/
```

## Instalation with pyenv

Execute this on romeo

add to your .bashrc file on romeo:

```bash
export PATH="$HOME/.pyenv/bin:$PATH"
if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init -)"
  eval "$(pyenv virtualenv-init -)"
fi
```

Available versions

```bash
pyenv install --list | fgrep 3.7
```

```bash
pyenv install --list | fgrep 3.8
```
