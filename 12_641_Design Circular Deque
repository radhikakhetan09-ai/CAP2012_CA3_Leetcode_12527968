class MyCircularDeque {
private:
    vector<int> data;
    int capacity;
    int count;
    int frontIndex;

public:
    MyCircularDeque(int k)
        : data(k), capacity(k), count(0), frontIndex(0) {}

    bool insertFront(int value) {
        if (isFull()) return false;

        frontIndex = (frontIndex - 1 + capacity) % capacity;
        data[frontIndex] = value;
        count++;
        return true;
    }

    bool insertLast(int value) {
        if (isFull()) return false;

        int index = (frontIndex + count) % capacity;
        data[index] = value;
        count++;
        return true;
    }

    bool deleteFront() {
        if (isEmpty()) return false;

        frontIndex = (frontIndex + 1) % capacity;
        count--;
        return true;
    }

    bool deleteLast() {
        if (isEmpty()) return false;

        count--;
        return true;
    }

    int getFront() {
        return isEmpty() ? -1 : data[frontIndex];
    }

    int getRear() {
        if (isEmpty()) return -1;

        int index = (frontIndex + count - 1) % capacity;
        return data[index];
    }

    bool isEmpty() {
        return count == 0;
    }

    bool isFull() {
        return count == capacity;
    }
};
