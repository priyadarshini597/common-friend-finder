def find_common_friends(users_friends):
    # Convert each user's friend list into a set
    friend_sets = [set(friends) for friends in users_friends.values()]
    
    # Find the intersection of all sets to get common friends
    common_friends = set.intersection(*friend_sets)
    
    return common_friends

# Example Usage
if __name__ == "__main__":
    # Example data: A dictionary where keys are user names and values are their friends
    users_friends = {
        "Alice": ["Bob", "Charlie", "David", "Eva"],
        "Bob": ["Alice", "Charlie", "Eva", "David"],
        "Charlie": ["Alice", "Bob", "Eva", "David"],
    }
    
    common_friends = find_common_friends(users_friends)
    
    if common_friends:
        print("Common friends:", common_friends)
    else:
        print("No common friends found.")
