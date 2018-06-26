# express-graphql

```javascript
query getSingleCourse($courseID: Int!) {
  course(id: $courseID) {
    title
    author
    description
    topic
    url
  }
}

{"courseID": 1}
```

```javascript
query getCoursesForTopic($courseTopic: String!) {
  courses(topic: $courseTopic) {
    title
    author
    description
    topic
    url
  }
}

{"courseTopic": "Node.js"}
```
