# majordomo-telegram
добавлена поддержка тем в чате,
айди темы указывается в логах модуля,
айди темы пишется в базу данных
Примеры использования новых методов для работы с темами (threads):
     * $thread_id = положительное число id темы чата
     * 1. Отправка сообщения в тему пользователю:
     *    $telegram->sendMessageToUserThread($user_id, $thread_id, $message);
     * 
     * 2. Отправка сообщения в тему всем пользователям:
     *    $telegram->sendMessageToAllThread($thread_id, $message);
     * 
     * 3. Отправка сообщения в тему администраторам:
     *    $telegram->sendMessageToAdminThread($thread_id, $message);
     * 
     * 4. Отправка изображения в тему:
     *    $telegram->sendImageToUserThread($user_id, $thread_id, $image_path, $caption);
     * 
     * 5. Отправка файла в тему:
     *    $telegram->sendFileToUserThread($user_id, $thread_id, $file_path, $caption);
     * 
     * 6. Редактирование сообщения в теме:
     *    $telegram->editMessageThread($user_id, $thread_id, $message_id, $new_message);
     * 
     * 7. Использование через SAY с thread_id:
     *    say('Сообщение', 2, 0, '', array('thread_id' => 5));
