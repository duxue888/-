def convert_chinese_to_arabic(chinese_num):
    chinese_num_dict = {
        "一百": 100,
        "二百": 200,
        "三百": 300,
        "四百": 400,
        "五百": 500,
        "六百": 600,
        "七百": 700,
        "八百": 800,
        "九百": 900,
        "一十": 10,
        "二十": 20,
        "三十": 30,
        "四十": 40,
        "五十": 50,
        "六十": 60,
        "七十": 70,
        "八十": 80,
        "九十": 90
    }
    parts = chinese_num.split()
    arabic_num = 0
    for part in parts[::-1]:
        if part in chinese_num_dict:
            arabic_num += chinese_num_dict[part]
    return arabic_num
