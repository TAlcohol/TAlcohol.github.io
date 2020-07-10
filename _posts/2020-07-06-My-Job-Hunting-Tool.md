---
layout: single
title: My Job Hunting Tool
---

For the job hunting times, there are too much positions need to apply. So I am using Numbers to record every position I have applied, for saving the job descriptions and other informations.

While it won't last for long. There's too much work for maintain and the adding way are making my finger broken.

So I build a website runs locally for storing those positions and companies. I learned Vue.js days ago and I thought this is the perfect chance for me to learn Vue in a practical way.

{% highlight javascript %}
getPositions() {
      const path = `http://localhost:5000/users/1/user_positions?page=${this.currentPage}`;
      axios.get(path)
        .then((res) => {
          this.positions = res.data.positions;
          this.total_rows = res.data.total_count;
        })
        .catch((error) => {
          // eslint-disable-next-line
          console.error(error);
        });
},
{% endhighlight %}

----

A screenshot of this tool.
![My helpful screenshot](/assets/images/job-tracker.png)