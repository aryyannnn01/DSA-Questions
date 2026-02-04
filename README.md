# DSA-Questions
preparing stuff which helps in placement.

// LeetCode Problem no. - 236
public TreeNode lowestCommonAncestor(TreeNode root, TreeNode p, TreeNode q){
  if(root == null){
    return null;
  }
  if(root == p || root == q){
    return root;
  }

  TreeNode left = lowestCommonAncestor(root.left, p, q);
  TreeNode right = lowestCommonAncestor(root.right, p, q);

  if(left != null || right != null){
    return root;
  }
  
  return root;
}
