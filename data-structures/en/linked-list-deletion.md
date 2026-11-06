# C++ Template Singly Linked List with a Head Node: Delete Function and Key Points

## I. Standardized, Complete, Runnable Code (C++ Template Singly Linked List with a Head Node)

```cpp
#include <iostream>
#include <cstdlib>  // free() frees memory
using namespace std;

// Template linked list node definition
template<class DT>
struct LNode {
    DT data;         // data field
    LNode<DT>* next; // pointer field, points to the next node
};

// ======================================
// Function 1: DD(L) deletes all nodes with even values from the list
// Parameter LNode<DT> *&L: reference to a pointer; modifications to the list inside the function affect the caller's argument as well
// ======================================
template<class DT>
void DD(LNode<DT>*& L) {
    LNode<DT>* q = L;        // q: p's predecessor node, initially points to the head node
    LNode<DT>* p = L->next;  // p: the node currently being traversed, initially points to the first element node
    while (p != nullptr) {
        // Check: the current node's data is even, so delete it
        if (p->data % 2 == 0) {
            q->next = p->next; // the predecessor skips the current p, breaking p off the chain
            free(p);           // free the deleted node's memory to prevent memory leaks
            p = q->next;       // p moves on to the next node to check
        } else {
            // no deletion: move both pointers forward in step
            q = p;
            p = p->next;
        }
    }
}

// ======================================
// Function 2: DF(L, m, n) deletes all nodes whose data falls within the range [m, n]
// ======================================
template<class DT>
void DF(LNode<DT>*& L, int m, int n) {
    LNode<DT>* q = L;
    LNode<DT>* p = L->next;
    while (p != nullptr) {
        // the current node's value lies within [m, n], delete it
        if (p->data >= m && p->data <= n) {
            q->next = p->next;
            free(p);
            p = q->next;
        } else {
            q = p;
            p = p->next;
        }
    }
}

// ======================================
// Overload the unary operator ~: move all negative-valued nodes to the very front of the list (right after the head node)
// Handwritten logic: on meeting a negative, detach it and insert it at the front; positives are traversed normally
// ======================================
template<class DT>
void operator~(LNode<DT>*& L) {
    LNode<DT>* q = L;
    LNode<DT>* p = L->next;
    while (p != nullptr) {
        if (p->data < 0) {
            // 1. first unlink p from its original position
            q->next = p->next;
            // 2. insert p right after the [head node L] (at the very front of the list)
            p->next = L->next;
            L->next = p;
            // 3. p moves to q's next node (q stays put, because the next node still needs to be checked)
            p = q->next;
        } else {
            // positive value: move both pointers forward
            q = p;
            p = p->next;
        }
    }
}

// ======================================
// Utility function: first find the minimum value in the list, then delete all nodes equal to the minimum
// ======================================
template<class DT>
void DelMinNode(LNode<DT>*& L) {
    if (L->next == nullptr) return; // empty list: exit immediately

    // First pass: find the minimum value min in the list
    DT min = L->next->data;
    LNode<DT>* p = L->next;
    while (p != nullptr) {
        if (p->data < min) {
            min = p->data;
        }
        p = p->next;
    }

    // Second pass: delete all nodes whose data == min
    LNode<DT>* q = L;
    p = L->next;
    while (p != nullptr) {
        if (p->data == min) {
            q->next = p->next;
            free(p);
            p = q->next;
        } else {
            q = p;
            p = p->next;
        }
    }
}

// ---------------- Helper test function (optional, used to print the list) ----------------
template<class DT>
void PrintList(LNode<DT>* L) {
    LNode<DT>* p = L->next;
    while (p) {
        cout << p->data << " ";
        p = p->next;
    }
    cout << endl;
}

// ---------------- Helper: create an empty list with a head node ----------------
template<class DT>
LNode<DT>* CreateEmptyList() {
    LNode<DT>* head = (LNode<DT>*)malloc(sizeof(LNode<DT>));
    head->next = nullptr;
    return head;
}

int main() {
    // Example test
    LNode<int>* head = CreateEmptyList<int>();
    // Write tail insertion yourself to insert data and test each function
    return 0;
}
```

## II. Breakdown of the Core Knowledge Points (matching your four handwritten problems — guaranteed exam material)

### Knowledge Point 1: Basic Structure of the Singly Linked List with a Head Node

- **Head node** `L`: stores no business data and stays fixed at the very front of the list;
- **First element node**: `L->next`, the first node holding valid data;
- **Advantage**: when deleting the **first element node**, no separate special-case branch is needed; the deletion logic stays uniform.

> Compared with a list without a head node: deleting the first node requires modifying the head pointer, which adds an extra `if` branch to the code — prefer a list with a head node in exams.

### Knowledge Point 2: The Universal Two-Pointer Traversal Template (all four deletion problems reuse this framework)

Every traversal / deletion function has the same fixed structure:

```cpp
LNode<DT>* q = L;        // q = predecessor node, always one node before p
LNode<DT>* p = L->next;  // p = the node currently being traversed
while (p != nullptr) {
    if (node p should be deleted) {
        q->next = p->next; // 1. the predecessor bypasses p, breaking the chain
        free(p);           // 2. free the memory (you must write this in data-structures exams, or you lose points)
        p = q->next;       // 3. p jumps to the new next node; q stays put
    } else {
        // no deletion: both pointers move forward together
        q = p;
        p = p->next;
    }
}
```

**Key points to memorize:**

- When deleting a node: `q` does not move; only `p` is updated;
- When not deleting a node: `q = p; p = p->next` — both pointers move forward in step.

### Knowledge Point 3: The `LNode<DT> *&L` Reference-to-Pointer Parameter (high-frequency exam point)

- `LNode<DT>*`: an ordinary pointer — the function can only read the list; modifying `L` inside the function does not affect the caller;
- `LNode<DT>*& L`: a **reference to a pointer** — if the function modifies the head of the list, the caller's argument changes in step.
  Although these four problems all use a head node and never modify the head node itself, the standard exam convention is to add the `&`.

### Knowledge Point 4: The Generic `template` Linked List

The first line you hand-write, `template<class DT>`, is the template:

- It lets the list support `int`, `float`, `double`, or any other data type;
- If the exam question only requires an `int` list, the template can be omitted, but since the handwritten notes explicitly wrote `template`, it is recommended to memorize the template form for full marks.

### Knowledge Point 5: Node Relocation (the `~` overloaded function — the hard part)

The problem asks to move all negative numbers to the very front of the list. The core is three steps:

- First, unlink the current node `p`: `q->next = p->next`;
- Insert `p` at the front of the list (right after the head node):

```cpp
p->next = L->next; // p links onto what was the first node
L->next = p;       // the head node points to p, so p becomes the new first element node
```

- Continue the traversal with `p = q->next`; **`q` stays put** (do not write `q = p`, otherwise the nodes further back will be missed).

### Knowledge Point 6: Two Passes over the List (the delete-minimum function)

Two separate steps; exams often test the "find first, then batch-delete" pattern:

- **First pass: read-only, no modification** — scan the whole list to find the extreme value (the minimum `min`);
- **Second pass: modify and delete** — traverse again and delete all nodes equal to `min`.

### Knowledge Point 7: Boundary Testing (must be considered when writing code; easy to lose points in exams)

- Empty list (`L->next == nullptr`): return immediately to prevent a null-pointer crash;
- Every node must be deleted (the list ends up with only the head node);
- The nodes to delete sit at the head / tail of the list;
- Multiple consecutive nodes match the condition (e.g. consecutive even numbers, consecutive negatives).

### Knowledge Point 8: Freeing Memory — `free (p)`

A hard scoring point in data-structures exams: whenever a node is deleted, you must write `free(p)`;
omitting it is judged as a memory leak and costs 1–2 points directly.

## III. Quick Memory Sheet for the Four Function Problems (recite before the exam)

- **DD — delete even numbers**: traverse and check `p->data % 2 == 0`; delete when satisfied;
- **DF — delete the range [m,n]**: check `p->data >= m && p->data <= n`; delete if inside the range;
- **~ — move negatives to the front**: on meeting a negative, detach the node and insert it right after the head node; the `q` pointer does not move forward;
- **Delete all minimum values**: one pass to find `min`, a second pass to delete all nodes equal to `min`.
