<template>
    <div id="app">

        <receipts name="Your Receipt" currency="EUR">
            <receipt-items :products="invoiceItem"></receipt-items>
            <receipt-summary :summary="invoiceSummaryData"></receipt-summary>
        </receipts>

    </div>
</template>

<script>
    import { Receipts, ReceiptItems, ReceiptSummary } from './receipt';

    export default {
        name: 'app',
        data() {
            return {
                invoiceItem: [
                    { name: 'Cheese Product 1', price: 2.50 },
                    { name: 'Cheese Product 2', price: 3.23 },
                    { name: 'Cheese Product 3', price: 4.35 },
                    { name: 'Cheese Product 4', price: 1.99 }
                ],
                invoiceSummaryData: {
                    // subtotal: 25.25,
                    discount: 25,
                    // discountprice: 10,
                    vatpercentage: 21,
                    // vatprice: 20,
                    // total: 1400
                }
            }
        },
        components: {
            Receipts,
            ReceiptItems,
            ReceiptSummary
        }
    }
</script>
