
<a name="SCRIPT"></a>

# Script `mint.move`

### Table of Contents

-  [Function `main`](#SCRIPT_main)



<a name="SCRIPT_main"></a>

## Function `main`



<pre><code><b>public</b> <b>fun</b> <a href="#SCRIPT_main">main</a>&lt;unknown#0&gt;(account: &signer, payee: address, auth_key_prefix: vector&lt;u8&gt;, amount: u64)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>fun</b> <a href="#SCRIPT_main">main</a>&lt;Token&gt;(account: &signer, payee: address, auth_key_prefix: vector&lt;u8&gt;, amount: u64) {
  <b>if</b> (!<a href="../../modules/doc/LibraAccount.md#0x1_LibraAccount_exists_at">LibraAccount::exists_at</a>(payee)) {
      <a href="../../modules/doc/LibraAccount.md#0x1_LibraAccount_create_testnet_account">LibraAccount::create_testnet_account</a>&lt;Token&gt;(account, payee, auth_key_prefix)
  };
  <a href="../../modules/doc/LibraAccount.md#0x1_LibraAccount_mint_to_address">LibraAccount::mint_to_address</a>&lt;Token&gt;(account, payee, amount);
}
</code></pre>



</details>
