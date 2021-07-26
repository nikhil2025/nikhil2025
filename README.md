- 👋 Hi, I’m @nikhil2025
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
nikhil2025/nikhil2025 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
//merge two sorted linked lists
Node* sortedMerge(Node* h1, Node* h2)
{
	if (!h1)
		return h2;
	if (!h2)
		return h1;

	// start with the linked list
	// whose head data is the least
	if (h1->data < h2->data) {
		h1->next = sortedMerge(h1->next, h2);
		return h1;
	}
	else {
		h2->next = sortedMerge(h1, h2->next);
		return h2;
	}
}

