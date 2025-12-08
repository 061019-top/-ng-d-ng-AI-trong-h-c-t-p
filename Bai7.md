📘 MINI-PROJECT: KIỂM TRA CHUỖI PALINDROME
1. Hỏi AI để hiểu “palindrome” → Viết lại theo lời mình

Prompt mình gửi cho AI:

“Hãy giải thích khái niệm palindrome trong lập trình, kèm ví dụ dễ hiểu.”

AI trả lời (tóm lược):
Palindrome là chuỗi đọc xuôi hay ngược đều giống nhau, ví dụ: “level”, “madam”, “racecar”.

Giải thích lại theo lời của mình:

Palindrome là một chuỗi mà khi mình đảo ngược nó lại, thứ tự ký tự không thay đổi. Tức là đọc từ trái sang phải hay phải sang trái đều giống nhau. Những từ như “madam”, “level” là ví dụ điển hình. Điều quan trọng là khoảng trắng và chữ in–hoa/in–thường có thể ảnh hưởng tùy cách mình xử lý.

2. Nhờ AI gợi ý thuật toán và code mẫu

Prompt mình gửi AI:

“Hãy đề xuất thuật toán đơn giản để kiểm tra palindrome bằng Python và viết code mẫu.”

AI gợi ý:

Chuẩn hóa chuỗi (lowercase).

Đảo chuỗi bằng slicing.

So sánh chuỗi gốc với chuỗi đảo.

Code AI gợi ý:

def is_palindrome(s):
    s = s.lower()
    return s == s[::-1]

3. Viết lại code theo ý mình (tự chỉnh sửa)

Mình muốn code dễ đọc hơn và bỏ ký tự không phải chữ cái.

import re

def is_palindrome(text):
    # Chỉ giữ chữ cái và số
    cleaned = re.sub(r'[^a-zA-Z0-9]', '', text).lower()
    reversed_text = cleaned[::-1]
    return cleaned == reversed_text

4. Tạo một lỗi nhỏ cố ý → nhờ AI debug

Mình cố ý tạo lỗi sai:

def is_palindrome(text):
    cleaned = re.sub(r'[^a-zA-Z0-9]', '', text).lower()
    reversed = cleaned[-1]   # ❌ lỗi cố ý: đảo chuỗi không đúng
    return cleaned == reversed


Prompt gửi AI:

“Đoạn code palindrome này không hoạt động. Bạn hãy phân tích lỗi và sửa giúp tôi.”

AI trả lời (tóm tắt):

Lỗi ở dòng reversed = cleaned[-1].
cleaned[-1] chỉ lấy ký tự cuối, không phải đảo cả chuỗi.

Cách đúng phải dùng cleaned[::-1].

AI đưa code sửa:

reversed = cleaned[::-1]

5. Nhận xét về quá trình sử dụng AI

Điều hiệu quả:

AI giải thích khái niệm nhanh, dễ hiểu, giúp mình tiết kiệm thời gian đọc tài liệu.

Thuật toán được đề xuất rõ ràng → dễ triển khai.

Khi cố ý tạo lỗi, AI phát hiện đúng và giải thích lý do sai rất chi tiết.

AI hỗ trợ tốt cho việc refactor và viết code gọn hơn.

Điều chưa hiệu quả:

Nếu chỉ dựa vào AI thì dễ bị “bị động”, không tự nghĩ ra thuật toán ban đầu.

Code gợi ý của AI đôi khi quá ngắn và không giải thích sâu (phải hỏi thêm).

Nếu lỗi phức tạp hơn hoặc liên quan đến nhiều file, cần IDE như Cursor chứ ChatGPT không đủ ngữ cảnh.