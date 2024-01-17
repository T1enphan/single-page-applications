<template>
    <div class="row">
        <div class="card">
            <div class="card-header">
                Danh Sách Hóa Đơn Nhập Kho
            </div>
            <div class="card-body">
                <div class="table-responesive">
                    <table class="table table-bordered">
                        <thead>
                            <tr class="text-center align-middle">
                                <th>#</th>
                                <th>Mã Hóa Đơn</th>
                                <th>Tổng Tiền</th>
                                <th>Nhà Cung Cấp</th>
                                <th>Ghi Chú</th>
                                <th>Nhân Viên</th>
                                <th>Chi Tiết Hóa Đơn</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <th class="text-center align-middle">1</th>
                                <td class="text-center align-middle">MD1</td>
                                <td class="text-end align-middle">175.000 ₫</td>
                                <td class="align-middle">CÔNG TY TNHH SƠN TÙNG</td>
                                <td class="text-center align-middle">
                                    <i class="fa-solid fa-notes-medical fa-2x text-info" data-bs-toggle="modal"
                                    data-bs-target="#ghiChuModal"></i>
                                </td>
                                <td class="align-middle">Admin</td>
                                <td class="text-center align-middle">
                                    <i class="fa-solid fa-circle-info fa-2x text-success" data-bs-toggle="modal"
                                    data-bs-target="#chiTietModal"></i>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <div class="modal fade" id="ghiChuModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h1 class="modal-title fs-5" id="exampleModalLabel">Ghi Chú</h1>
                                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <textarea class="form-control" cols="30" rows="10"></textarea>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Đóng</button>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="modal fade" id="chiTietModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h1 class="modal-title fs-5" id="exampleModalLabel">Chi Tiết Hóa Đơn</h1>
                                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <div class="table-responesive">
                                    <table class="table table-bordered">
                                        <thead>
                                            <tr class="text-center align-middle">
                                                <th>#</th>
                                                <th>Nguyên Liệu</th>
                                                <th>Số Lượng</th>
                                                <th>Đơn Giá</th>
                                                <th>Thành Tiền</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr>
                                                <th class="text-center align-middle">1</th>
                                                <td class="text-start align-middle"> Tên nguyên Liệu</td>
                                                <td class="text-center align-middle">Số Lượng</td>
                                                <td class="text-end align-middle">Đơn Giá</td>
                                                <td class="text-end align-middle">Thành Tiền</td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Đóng</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { createToaster } from "@meforma/vue-toaster";
const toaster = createToaster({ position: "top-right" });
import baseRequest from '../../core/baseRequest';
export default {
    data() {
        return {

        }
    },
    mounted() {
        
    },
    methods: {
        formatToVND(number) {
            number = parseInt(number);
            return number.toLocaleString('vi-VN', { style: 'currency', currency: 'VND' });
        },
    },
}
</script>
<style>
    
</style>