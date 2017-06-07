# Render-data-and-important

  ## renderPosts(){
    return this.props.posts.map(function(post){
      return(
          <li key={post.id} className="list-group-item">
            <Link to={"posts/"+post.id+"/"}>
              <strong>{post.title}</strong>
              <span className="pull-xs-right">{post.categories}</span>
            </Link>
          </li>
      );
    });
  }



 ## render(){
    return(
    <div>
      <div className="text-xs-right">
        <Link to="posts/new" className="btn btn-primary">
          Add a Post
        </Link>
      </div>
      <h3>Posts</h3>
      <ul className="list-group" >
        {this.renderPosts()}
      </ul>
    </div>);
  }
