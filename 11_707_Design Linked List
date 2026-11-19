class MyLinkedList {
private:
    struct Node {
        int val;
        Node* next;

        Node(int value) : val(value), next(nullptr) {}
    };

    Node* head;
    int length;

public:
    MyLinkedList() : head(nullptr), length(0) {}

    int get(int index) {
        if (index < 0 || index >= length) return -1;

        Node* current = head;
        for (int i = 0; i < index; i++) {
            current = current->next;
        }

        return current->val;
    }

    void addAtHead(int val) {
        Node* node = new Node(val);
        node->next = head;
        head = node;
        length++;
    }

    void addAtTail(int val) {
        Node* node = new Node(val);

        if (head == nullptr) {
            head = node;
        } else {
            Node* current = head;
            while (current->next != nullptr) {
                current = current->next;
            }
            current->next = node;
        }

        length++;
    }

    void addAtIndex(int index, int val) {
        if (index < 0) index = 0;
        if (index > length) return;

        if (index == 0) {
            addAtHead(val);
            return;
        }

        Node* current = head;
        for (int i = 0; i < index - 1; i++) {
            current = current->next;
        }

        Node* node = new Node(val);
        node->next = current->next;
        current->next = node;
        length++;
    }

    void deleteAtIndex(int index) {
        if (index < 0 || index >= length) return;

        if (index == 0) {
            Node* oldHead = head;
            head = head->next;
            delete oldHead;
        } else {
            Node* current = head;
            for (int i = 0; i < index - 1; i++) {
                current = current->next;
            }

            Node* nodeToDelete = current->next;
            current->next = nodeToDelete->next;
            delete nodeToDelete;
        }

        length--;
    }
};
