<template>
    <h4 style="text-decoration: underline;">Interview Task One</h4>
    <div v-for="(students, subject) in transformedStudents" :key="subject" style="margin-bottom: 10px;">
        <strong>{{ subject }}: </strong>
        <span v-for="(student, index) in students" :key="student" style="padding-right: 5px;"> {{ index + 1 }}. {{ student }}
        </span>
    </div>
</template>

<script>
export default {
    data() {
        return {
            students: [
                { name: "John", grade: 9, subjects: ["Math", "Science", "History"] },
                { name: "Alice", grade: 10, subjects: ["Math", "Biology", "Physics"] },
                { name: "Bob", grade: 11, subjects: ["Chemistry", "Physics", "Literature"] }
            ]
        }
    },
    computed: {
        transformedStudents() {
            const result = {};
            this.students.forEach(student => {
                student.subjects.forEach(subject => {
                    if (!result[subject]) {
                        result[subject] = [];
                    }
                    result[subject].push(student.name);
                });
            });
            return result;
        }
    }
}
</script>