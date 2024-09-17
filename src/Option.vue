<script>
export default {
data() {
    return {
      name : "Jonh Doe",
      status : 'active',
      tasks : ['Task One', 'Task Two', 'Task Three'],
      link : 'https://google.com',
    };
  },
  methods: {
    toggleStatus () {
      if (this.status === 'active') {
        this.status = 'pending';
      } else if (this.status === 'pending') {
        this.status = 'inactive';
      }  else {
        this.status = 'active'
      }
    },
  },
};
</script>