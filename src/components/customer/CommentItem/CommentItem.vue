<script setup>
import {
    CommentOutlined,
    StarFilled,
    CheckCircleFilled,
    LikeFilled,
    DislikeFilled,
} from '@ant-design/icons-vue';
</script>

<template>
    <div class="flex gap-10 mb-[36px] bg-[#fff] p-6 shadow-lg shadow-[#ccc]">
        <div class="flex flex-col gap-[20px]">
            <div class="flex items-center">
                <img
                    class="w-[80px] h-[80px] rounded-full mr-3"
                    src="data:image/jpeg;base64,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"
                    alt=""
                />
                <div>
                    <h3 class="block mb-6 text-[1.8rem] font-medium">
                        Vũ Ngọc
                    </h3>
                    <span class="text-[1.5rem] text-[#6e6363] leading-3"
                        >Đã tham gia 3 tháng</span
                    >
                </div>
            </div>
            <div class="flex justify-between text-[13px]">
                <div class="text-[#808089] ml-6 flex items-center">
                    <CommentOutlined class="text-[2rem] mr-4" />
                    <span class="">Đã viết</span>
                </div>
                <span class="text-[#4d4d53]">1 đánh giá</span>
            </div>
        </div>
        <div class="flex-1">
            <div class="text-[2rem] mb-3">
                <StarFilled class="text-[#ffff00e7]" />
                <StarFilled class="text-[yellow]" />
                <StarFilled class="text-[yellow]" />
                <StarFilled class="text-[#ccc]" />
                <StarFilled class="text-[#ccc]" />
            </div>
            <div
                class="flex items-center text-[1.3rem] mb-6 text-[var(--primary-color)]"
            >
                <CheckCircleFilled class="mr-6 text-[1.8rem]" />
                Đã mua hàng
            </div>
            <p class="text-[1.6rem] leading-relaxed">
                Sách được đóng gói cẩn thận. Bìa sách hình tấm bản đồ chỉ dẫn
                đến kho báu rất độc lạ. Sách viết về những sức mạnh, khả năng
                tiềm ẩn bên trong con người và cách để đánh thức được chúng, rất
                chi tiết và... Xem thêm
            </p>
            <div class="flex justify-between">
                <span class="text-[13px]">Đánh giá vào 3 tháng trước</span>
                <div class="flex gap-6">
                    <div
                        class="flex items-center text-[16px] gap-3 font-medium"
                    >
                        <LikeFilled class="text-[2.5rem] text-[#808089]" />
                        2,8N
                    </div>
                    <div
                        class="flex items-center text-[16px] gap-3 font-medium"
                    >
                        <DislikeFilled class="text-[2.5rem] text-[#808089]" />
                        2,8N
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
