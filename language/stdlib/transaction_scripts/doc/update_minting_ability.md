
<a name="SCRIPT"></a>

# Script `update_minting_ability.move`

### Table of Contents

-  [Function `main`](#SCRIPT_main)



<a name="SCRIPT_main"></a>

## Function `main`



<pre><code><b>public</b> <b>fun</b> <a href="#SCRIPT_main">main</a>&lt;unknown#0&gt;(account: &signer, allow_minting: bool)
</code></pre>



<details>
<summary>Implementation</summary>


<pre><code><b>fun</b> <a href="#SCRIPT_main">main</a>&lt;Currency&gt;(account: &signer, allow_minting: bool) {
    <a href="../../modules/doc/Libra.md#0x1_Libra_update_minting_ability">Libra::update_minting_ability</a>&lt;Currency&gt;(account, allow_minting)
}
</code></pre>



</details>
