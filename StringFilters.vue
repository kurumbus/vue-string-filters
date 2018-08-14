<script>
    export default {
      filters: {
        capitalize: function (value) {
          if (!value) return '';
          value = value.toString();
          return value.charAt(0).toUpperCase() + value.slice(1);
        },
        wordCase: function (value) {
            let result = value.replace( /([A-Z])/g, " $1" );
            result = result.replace(/[_\.-]/g, ' ');
            let finalResult = result.charAt(0).toUpperCase() + result.slice(1);
            return finalResult;
        },
        initials: function (value) {
            let initials = value.replace(/[^a-zA-Z- ]/g, "").match(/\b\w/g);
            return initials.join('');
        }
      }
    }
</script>
