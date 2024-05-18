提問詞:請寫出二元搜尋樹的演算法
提問詞:請計算二元搜尋樹演算法的時間複雜度
提問詞:請用Python寫出二元搜尋樹的演算法
提問詞:請用C寫出二元搜尋樹的演算法
提問詞:請用C++寫出二元搜尋樹的演算法
提問詞:請用JAVA寫出二元搜尋樹的演算法
提問詞:請用Rust寫出二元搜尋樹的演算法
提問詞:請用go寫出二元搜尋樹的演算法
提問詞:請用C#寫出二元搜尋樹的演算法
提問詞:請用Javascript#寫出二元搜尋樹的演算法

# GenAI_Algorithm_lab1 ==> 二元搜尋樹的各種實作(heap sort)
- `提問詞`:請寫出heap sort的演算法
- `提問詞`:請計算heap sort演算法的時間複雜度
- `提問詞`:請用Python寫出heap sort的演算法
- `提問詞`:請用C寫出heap sort的演算法
- `提問詞`:請用C++寫出heap sort的演算法
- `提問詞`:請用JAVA寫出heap sort的演算法
- `提問詞`:請用Rust寫出heap sort的演算法
- `提問詞`:請用go寫出heap sort的演算法
- `提問詞`:請用C#寫出heap sort的演算法
- `提問詞`:請用Javascript#寫出heap sort的演算法
### '提問詞':請寫出heap sort的演算法
'''
#include <iostream>
using namespace std;

struct TreeNode {
    int data;
    TreeNode* left;
    TreeNode* right;
};

// 創建新節點
TreeNode* createNode(int data) {
    TreeNode* newNode = new TreeNode;
    newNode->data = data;
    newNode->left = nullptr;
    newNode->right = nullptr;
    return newNode;
}

// 插入節點
TreeNode* insert(TreeNode* root, int data) {
    if (root == nullptr) {
        return createNode(data);
    }
    if (data < root->data) {
        root->left = insert(root->left, data);
    } else if (data > root->data) {
        root->right = insert(root->right, data);
    }
    return root;
}

// 查找節點
TreeNode* search(TreeNode* root, int data) {
    if (root == nullptr || root->data == data) {
        return root;
    }
    if (data < root->data) {
        return search(root->left, data);
    }
    return search(root->right, data);
}

// 中序遍歷
void inOrder(TreeNode* root) {
    if (root != nullptr) {
        inOrder(root->left);
        cout << root->data << " ";
        inOrder(root->right);
    }
}

int main() {
    TreeNode* root = nullptr;
    root = insert(root, 50);
    insert(root, 30);
    insert(root, 70);
    insert(root, 20);
    insert(root, 40);
    insert(root, 60);
    insert(root, 80);

    cout << "In-order traversal:" << endl;
    inOrder(root);

    return 0;
}



'''

