public enum NotificationType{
		//0通知消息；1课程更新；2课件更新；3添加好友；4解除好友；5接受好友请求；6拒绝好友请求;7讨论回复;8新私信
		/**
		 * 0未定义
		 */
		Undefined,
		/**
		 * 1通知消息
		 */
		NewNotice,
		/**
		 * 2课程更新
		 */
		CourseUpdate,
		/**
		 * 3课件更新
		 */
		CoursewareUpdate,
		/**
		 * 4添加好友
		 */
		NewFriendRequest,
		/**
		 * 5接受好友请求
		 */
		FriendRequestBeAccepted,
		/**
		 * 6拒绝好友请求
		 */
		FriendRequestBeRejected,
		
		/**
		 * 7好友关系解除
		 */
		FriendDeleted,
		
		/**
		 * 8讨论回复;
		 */
		NewTopicReply,
		/**
		 * 9讨论被AT
		 */
		NewTopicAt,
		/**
		 * 10新私信
		 */
		NewChat,
		/**
		 * 11作业更新
		 */
		HomeworkUpdate,
		/**
		 * 12考试更新
		 */
		ExamUpdate;
		
		public int getValue(){
			return this.ordinal();
		}
		
	}


push内容：
private static String msgPattern = "{\"aps\":{\"alert\":{\"body\":\"%1$s\",\"title\":\"%2$s\"},\"badge\":1},\"wkt\":{\"t\":\"%3$s\",\"param\":\"%4$s\"}}";

其中param的注解：
1. t=2,param=课程ID
2. t=3,param=课程ID,课件ID




