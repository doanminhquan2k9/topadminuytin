<?php
// Token và Chat ID của bot Telegram
$botToken = "7623590164:AAEoVKHVYlZ0UcDoKxcPCiSc_FOEAT_tC5s";
$chatId = "6664054279";

// Lấy dữ liệu từ biểu mẫu
$studentId = $_POST['student_id'];
$dob = $_POST['dob'];
$fbLink = $_POST['fb_link'];
$request = isset($_POST['request']) ? $_POST['request'] : 'Không có yêu cầu thêm';
$receipt = $_FILES['receipt']['tmp_name'];
$receiptName = $_FILES['receipt']['name'];

// Tạo tin nhắn
$message = "📋 **Thông Tin Đã Nhận**:\n";
$message .= "🎓 Mã Sinh Viên: " . $studentId . "\n";
$message .= "📅 Ngày Sinh: " . $dob . "\n";
$message .= "🔗 Link Facebook: " . $fbLink . "\n";
$message .= "✍️ Yêu Cầu Thêm: " . $request . "\n";

// Gửi tin nhắn đến Telegram
$apiUrl = "https://api.telegram.org/bot$botToken/sendMessage";
$data = [
    'chat_id' => $chatId,
    'text' => $message,
    'parse_mode' => 'Markdown',
];

// Gửi tin nhắn
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, $apiUrl);
curl_setopt($ch, CURLOPT_POST, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
$response = curl_exec($ch);
curl_close($ch);

// Kiểm tra và gửi ảnh chuyển khoản
if ($response) {
    $photoApiUrl = "https://api.telegram.org/bot$botToken/sendPhoto";
    $photoData = [
        'chat_id' => $chatId,
        'photo' => new CURLFile(realpath($receipt)), // Kiểm tra đường dẫn tệp
        'caption' => "Ảnh chuyển khoản: " . $receiptName,
    ];
    
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, $photoApiUrl);
    curl_setopt($ch, CURLOPT_POST, true);
    curl_setopt($ch, CURLOPT_POSTFIELDS, $photoData);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
    $photoResponse = curl_exec($ch);
    curl_close($ch);
    
    if ($photoResponse) {
        echo 'Gửi thành công!';
    } else {
        echo 'Gửi ảnh thất bại!';
    }
} else {
    echo 'Gửi thất bại!';
}
?>
