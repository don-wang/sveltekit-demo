<script context="module">
  export async function load({ fetch, url, params }) {
    const id = params.postId;
    const res = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`);
    const post = await res.json();

    if (res.ok) {
      return {
        props: {
          post,
        },
      };
    }
    return {
      status: res.status,
      error: new Error("Fetch failed"),
    };
  }
</script>

<script>
  export let post;
</script>

<div class="guide">
  <h2>{post.title}</h2>
  <p>{post.body}</p>
</div>

<style>
  .guide {
    margin-top: 40px;
    padding: 10px;
    border: 1px dotted rgba(255, 255, 255, 0.2);
  }
</style>
