<template>
  <q-page padding class="page-wrapper">
    <div class="q-pa-sm row">
      <div class="col-sm-12 q-my-md">
        <q-markdown :src="t" />
    <q-markdown src="
:::info
X-CA is not be trusted all OS, if you want use it, must config **X ROOT CA**.
:::

---

## Some Links

- [sorce code](https://github.com/x-ca/x-ca)
- [theory](https://www.xiexianbin.cn/s/ca)

---

### Some Files

- [root-ca.crt](https://ca.xiexianbin.cn/root-ca.crt)
- [tls-ca-chain.pem](https://ca.xiexianbin.cn/tls-ca-chain.pem)
- [tls-ca.cer](https://ca.xiexianbin.cn/tls-ca.crt)
- [tls-ca.crl](https://ca.xiexianbin.cn/tls-ca.crl)

---

## install X Root CA

- download root CA

```
curl -o root-ca.crt https://ca.xiexianbin.cn/root-ca.crt
```

- CentOS/Redhat

```
yum install -y ca-certificates
cp root-ca.crt /etc/pki/ca-trust/source/anchors
update-ca-trust
```

- Mac

double click `root-ca.crt`

- Ubuntu

```
apt install -y ca-certificates
cp root-ca.crt /usr/local/share/ca-certificates
update-ca-certificates

# delete ca
rm /usr/local/share/ca-certificates/ca.crt
update-ca-certificates
```

- [ref](https://www.xiexianbin.cn/http/ssl/2017-02-15-openssl-self-sign-ca/#导出导入自签名证书)

"></q-markdown>
      </div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { QMarkdown } from '@quasar/quasar-ui-qmarkdown'
import '@quasar/quasar-ui-qmarkdown/dist/index.min.css'

const t = `
<h4> X-CA </h4>

___

Self Sign CA for TLS/Software/Email
`;

export default {
  name: 'PageIndex',
  components: {
    // eslint-disable-next-line @typescript-eslint/no-unsafe-assignment
    QMarkdown,
  },
  setup() {
    return {
      t,
    };
  },
};
</script>

<style lang="sass" scoped>
</style>
