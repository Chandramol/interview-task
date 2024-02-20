<template>
    <h4 style="text-decoration: underline;">Interview Task Two</h4>
    <div>
        <p>Second Largest Value : {{ secondLargestValue }}</p>
        <strong>From this list {{ array }}</strong>
    </div>
</template>

<script>
export default {
    data() {
        return {
            array: [2, 1, 7, 3, 8, 9, 4, 3]
        }
    },
    computed: {
        // Methods to find second
        secondLargestValue() {
            // initial value
            let firstNumber = Number.MIN_SAFE_INTEGER;
            let secondNumber = Number.MIN_SAFE_INTEGER;

            this.array.forEach(element => {
                if (element > firstNumber) {
                    secondNumber = firstNumber;
                    firstNumber = element;
                } else if (element > secondNumber && element !== firstNumber) {
                    secondNumber = element;
                }
            });
            return secondNumber;
        }
    }
}
</script>