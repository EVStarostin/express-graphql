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

QUERY VARIABLES
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

QUERY VARIABLES
{"courseTopic": "Node.js"}
```

```javascript
query getCoursesWithFragments($courseID1: Int!, $courseID2: Int!) {
  course1: course(id: $courseID1) {
    ...courseFields
  }
  course2: course(id: $courseID2) {
    ...courseFields
  }
}

fragment courseFields on Course {
  title
  author
  description
  topic
  url
}

QUERY VARIABLES
{
  "courseID1": 1,
  "courseID2": 2
}
```
