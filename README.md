# Facial-Expression-Recognition-Challenge

ეს პროექტი მიზნად ისახავს FER-2013 მონაცემთა ბაზის გამოყენებით ადამიანის სახის გამომეტყველების კლასიფიკაციას. გამოიყენება ღრმა კონვულუციური ნეირონული ქსელი, რომელიც განსაზღვრავს 7 კლასს: Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral.

პირველი მოდელი:
გამოიყენება CNN მოდელი 4 კონვოლუციური ბლოკით და 2 fully connected layer.

თითოეულ კონვოლუციურ ბლოკში გამოიყენება Conv2D BatchNorm ReLU MaxPool2D

ბოლო ნაწილში: Dropout რეგულარიზაცია და Linear ფენები კლასიფიკაციისთვის.

მონაცემები მოდის icml_face_data.csv ფაილიდან, ყოველი სურათი წარმოადგენს 48x48 პიქსელის გამოსახულებას.

მონაცემები იშლება და გარდაიქმნება FERDataset კლასში torch.utils.data.Dataset გამოყენებით. (RandomHorizontalFlip,RandomRotation,ToTensor,Normalize(mean=[0.5], std=[0.5]))
train_model() და evaluate_model() ფუნქციები მოდელის შეფასებისთვის.

Train Accuracy	54.86%
Train Loss	1.177
Validation Accuracy	56.43%
Validation Loss	1.133

მეორე მოდელი:






