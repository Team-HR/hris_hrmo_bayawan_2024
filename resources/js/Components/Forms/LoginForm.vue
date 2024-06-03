<template>
    <div class="card bg-base-100 w-full max-w-96 shadow-sm md:shadow-xl">
        <div class="card-body flex items-center md:p-6 p-4">
            <img src="images/hrLogo.ico" alt="hr logo" class="max-w-28">
            <h2 class="card-title">Login iHRIS</h2>
            <label class="form-control w-full">
                <div class="label">
                    <span class="label-text">Username</span>
                </div>
                <input type="text" placeholder="Type here" class="input input-bordered w-full" />
            </label>
            <label class="form-control w-full">
                <div class="label">
                    <span class="label-text">Password</span>
                </div>
                <input type="password" placeholder="Type here" class="input input-bordered w-full" />
            </label>
            <div class="card-footer w-full">
                <div class="divider"></div> 
                <button class="btn btn-primary w-full">Login</button>
            </div>
        </div>
    </div>
</template>