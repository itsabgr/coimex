# Coimex

[**Data model**](https://dbdiagram.io/d/610ce94c2ecb310fc3c0289e)

api proto
-
```protobuf
syntax = "proto3";
message nil {}
service users { //2da*ys
  rpc RegisterByEmail(nil) returns (nil) {}
  rpc GetUserByEmail(nil) returns (nil) {}
  rpc GetUserByToken(nil) returns (nil) {}
  rpc GenerateUserToken(nil) returns (nil) {}
  rpc ChangePwdByOtp(nil) returns (nil) {}
  rpc ChangePwdByOldPwd(nil) returns (nil) {}
  rpc SyncPropsByToken(nil) returns (nil) {}
  rpc SetNotificationBroker(nil) returns (nil) {}
  rpc CreateUserPic(nil) returns (nil) {}

}
service txs { //1days
  rpc IncCreditByStripe1(nil) returns (nil) {}
  rpc IncCreditByStripe2(nil) returns (nil) {}
  rpc GetUserTxs(nil) returns (nil) {}
}
service OTPs { //1days
  rpc SendOtpToEmail(nil) returns (nil) {}
  rpc VerifyEmailSentOtp(nil) returns (nil) {}
}
service sessions { //1day
  rpc RefreshToken(nil) returns (nil) {}
  rpc PurgeUserSessions(nil) returns (nil) {}
  rpc PurgeByToken(nil) returns (nil) {}
  rpc GetByToken(nil) returns (nil) {}
  rpc ListUserSessions(nil) returns (nil) {}
}
service consts { //.5day
  rpc Find(nil) returns (nil) {}
}
service companies { //1day
  rpc Register(nil) returns (nil) {}
  rpc FindByOwner(nil) returns (nil) {}
  rpc Get(nil) returns (nil) {}
  rpc SyncProps(nil) returns (nil) {}
}
service ActivePlans { //1.5day
  rpc Purchase(nil) returns (nil) {}
  rpc GetActive(nil) returns (nil) {}
  rpc Find(nil) returns (nil) {}
  rpc Purge(nil) returns (nil) {}
}
service Employees { //1day
  rpc FindByCompany(nil) returns (nil) {}
  rpc FindByUser(nil) returns (nil) {}
  rpc Get(nil) returns (nil) {}
  rpc SetRoleByCompanyOwner(nil) returns (nil) {}
  rpc HireByCompanyOwner(nil) returns (nil) {}
  rpc PurgeByCompanyOwner(nil) returns (nil) {}
}

service Blobs { //2days
  rpc Write(nil) returns (nil) {}
  rpc Read(nil) returns (nil) {}
  rpc Close(nil) returns (nil) {}
  rpc Purge(nil) returns (nil) {}
  rpc AttachTo(nil) returns (nil) {}
  rpc FindByRef(nil) returns (nil) {}
  rpc GetRefs(nil) returns (nil) {}
}
service Blog { //3days
  rpc Create(nil) returns (nil) {}
  rpc SyncPropsByOwner(nil) returns (nil) {}
  rpc CreatePostImage(nil) returns (nil) {}
  rpc GetByOwner(nil) returns (nil) {}
  rpc PublishByOwner(nil) returns (nil) {}
  rpc GetPost(nil) returns (nil) {}
  rpc GetBlobs(nil) returns (nil) {}
  rpc LikePost(nil) returns (nil) {}
  rpc GetLikes(nil) returns (nil) {}
  rpc GetLikesCount(nil) returns (nil) {}
  rpc CommentOnPost(nil) returns (nil) {}
  rpc GetComments(nil) returns (nil) {}
  rpc GetCommentsCount(nil) returns (nil) {}
  rpc GetComment(nil) returns (nil) {}
}
service Messages { //1days
  rpc Send(nil) returns (nil) {}
  rpc Get(nil) returns (nil) {}
  rpc CreateMessageImage(nil) returns (nil){}
  rpc GetContent(nil) returns (nil) {}
  rpc FindByChat(nil) returns (nil) {}
  rpc DistinctChats(nil) returns (nil) {}
  rpc SetMessageSeenAt(nil) returns (nil) {}
}
service Offers { //4days
  rpc CreateOpportunity(nil) returns (nil) {}
  //xxx
}
//+2 days for core
```