# SolaEver2
SolaEver custom genesis run

====================================
root@6029P:~# mkdir ~/solaever-keys && cd ~/solaever-keys
ew -o validator-keypair.json --no-passphrase

# 2. 투표 계정 키 생성
solana-keygen new -o vote-keypair.json --no-passphrase

# 3. 스테이크 계정 키 생성
solana-keygen new -o stake-keypair.json --no-passphraseroot@6029P:~/solaever-keys#
root@6029P:~/solaever-keys# # 1. 노드 아이덴티티 생성
root@6029P:~/solaever-keys# solana-keygen new -o validator-keypair.json --no-



solana-genesis \
  --cluster-type mainnet-beta \
  --ledger ~/solaever-ledger \
  --faucet-lamports 500000000000000000 \
  --faucet-pubkey [본인_Identity_Pubkey] \
  --bootstrap-validator \
    [본인_Identity_Pubkey] \
    [본인_Vote_Pubkey] \
    [본인_Stake_Pubkey] \
  --bootstrap-validator-lamports 500000000000000000 \
  --bootstrap-validator-stake-lamports 450000000000000000 \
--hashes-per-tick sleep



~/solaever-keys# /root/agave/target/release/agave-validator   --ledger /root/solaever-ledger   --identity /root/solaever-keys/validator-keypair.json   --vote-account /root/solaever-keys/vote-keypair.json   --rpc-port 8899   --gossip-port 8001   --limit-ledger-size 50000000   --allow-private-addr   --wait-for-supermajority 0   --expected-bank-hash GS3vh8FdHtPVZBFndWmHoyY3VpiJUfzn7TJ7h4unj4Va   --expected-shred-version 26088   --log -

