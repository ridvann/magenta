<template>
  <AppView>
    <a-row :gutter="32">
      <a-col :lg="15">
        <TransactionCreateCard />
      </a-col>
      <a-col :lg="9">
        <WalletBalanceCard />
      </a-col>
    </a-row>
  </AppView>
</template>

<script>
export default {
  layout: 'app',
  created() {
    const payload = {
      model: { type: 'withdraw' },
      title: 'Fazer um saque',
      description: 'Faça um resgate de valor da sua conta.',
    }
    this.$store.dispatch('transaction/openForm', payload)
  },
}
</script>
