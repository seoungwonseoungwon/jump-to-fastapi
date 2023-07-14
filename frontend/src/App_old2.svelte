<script>
  let message;
  let todo = "값없음";
  let url = "http://127.0.0.1:8000/hello"
  fetch(url).then((res) => {
    res.json().then((msg) => {
      console.log(msg)
      message = msg.message;
      todo = msg.todo;

    });
  });
</script>

<h1>{message}</h1>
<h1>{todo}</h1>
