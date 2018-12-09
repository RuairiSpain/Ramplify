# Ramplify
Quickly scaffold React frontend for GraphQL APIs that use AWS Amplify backend

Research notes:

Auto generate a CRA app for each type: (similar to JHipster)
List with page, sort, filter, link
Details with images
Edit and create 
Takes care of login
Image view or document view
Use Amplify CSS styles/UI components (login/images...)

React CRUD + Search:
https://link.medium.com/3EKUUAgbwS

Schema:
https://github.com/aws-samples/aws-amplify-graphql




type Picture @model @auth(rules: [{allow: owner}]) {
  id: ID!
  name: String
  owner: String
  visibility: Visibility
  file: S3Object
  createdAt: String
}
 
type S3Object {
  bucket: String!
  region: String!
  key: String!
}
 
enum Visibility {
  public
  private
}



