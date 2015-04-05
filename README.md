# mba_ansiblefile
MacBookAir をYosemiteにあげたときに使用したAnsible用のファイル

割とよく失敗するので、その時は気にせず再実行する。

1. XCodeをインストール
2. Homebrewをインストール  
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
3. homebrewをアップデートしてansibleをインストールする  
brew update  
brew install ansible
4. zshにシェルを切り替えておく（こうしないと途中で失敗した）  
chsh -s /bin/zsh
5. caskで入れるもののために環境設定  
export HOMEBREW_CASK_OPTS="--appdir=/Applications"
6. hostsファイルを作っておく。内容はlocalhost１行
7. 実行  
ansible-playbook -i hosts -vv localhost.yml

詳しくは
http://t-wada.hatenablog.jp/entry/mac-provisioning-by-ansible
を参照。
