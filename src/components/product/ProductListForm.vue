<template lang="">
    <div>
        <h2>상품 목록</h2>
        <table>
            <tr>
                <th align="center" width="5%">상품명</th>
                <th align="center" width="5%">가격</th>
                <th align="center" width="5%">제조사</th>
                <th align="center" width="5%">유통기한</th>
                <th align="center" width="5%">제조일</th>
                <th align="center" width="5%">카테고리</th>
            </tr>
            <tr v-if="!products || (Array.isArray(products) && products.length === 0)">
                <td colspan="6">
                    등록된 상품이 없습니다.
                </td>
            </tr>
            <tr v-else v-for= "product in products" :key ="product.productId">
                <td>{{product.name}}</td>
                <td>{{product.price}}</td>
                <td>{{product.company}}</td>
                <td>{{product.expDate}}</td>
                <td>{{product.manufactureDate}}</td>
                <td>{{product.category}}</td>
            </tr>
        </table>
    </div>
</template>
<script>
export default {

}
</script>
<style lang="">
    
</style>