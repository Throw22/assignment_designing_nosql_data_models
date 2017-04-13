You're building an activity feed for a social media site. The feed must display a chronological list of activities for the current user's friends. These activities could potentially be any action performed on the site including uploading a photo, changing their profile, friending another user, commenting, liking etc... Further, you only want to display activities for users that the current user interacts with frequently.

user {
  username:
  friends: [user7, user9, etc...]
  bestfriends: [user2, user3] (if actions includedUsers shows up often then they're on the bestfriends list)
  actions: [
    {
      id: 25
      date: Jan 1 2017
      type: 'photo upload'
      content: --photo data--
      includedUsers: user2, user3
    },
    {
      id: 24
      date: Dec 26 2016
      type: 'comment'
      content: --text--
      includedUsers: user2
    }]
  feed: [feedItem1, feedItem2, feedItem3]
}


actions {
  all actions ever taken from every user
}

feeds {
  user1'sfeed: [feedItem1, feedItem2]

  id2: {

  }
}
