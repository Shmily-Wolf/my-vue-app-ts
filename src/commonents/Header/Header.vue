<template>
    <div class="Header">
        <div class="logo">
            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACMAAAAjCAYAAAAe2bNZAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyZpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNi1jMTM4IDc5LjE1OTgyNCwgMjAxNi8wOS8xNC0wMTowOTowMSAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIDIwMTcgKFdpbmRvd3MpIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOjJGOTYxRTY0MjY2QzExRTc5MkMxQTFGMDhDMjA3NjkyIiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOjJGOTYxRTY1MjY2QzExRTc5MkMxQTFGMDhDMjA3NjkyIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6MkY5NjFFNjIyNjZDMTFFNzkyQzFBMUYwOEMyMDc2OTIiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6MkY5NjFFNjMyNjZDMTFFNzkyQzFBMUYwOEMyMDc2OTIiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz50nU2cAAAD+klEQVR42tRYa0gUURQ+M/uaZXtoGf3TTDOwqKUQy7LHYggRFGEQZQlFUEGPPwVFIEYg2B+pqCAKehJRUBCRaFtZWRHZAwrykdqvgsq12lZndp3Omb0zzqyz7kxuVB8cZuc+zvnuueeePXecYAOyLHvwUY4SQJmDUoCSheJAiaF8RmlDaUUJojRwHDcA6QSSyEY5hhKS7SHE5mWng4QPpQ5FlEcHkenx/S4RP0q7nF6QPr9dIstRfsp/BqR3uZldzowIPq6juJSGaBSib99ArLMd5EgEHFPzwDWvJOWCpCctEHvfCZzXC468aeAsnAHgdGrdKKswuG8lJcNc2ILipXexsQH6z56Gwa9fgMvIAG/VZnAHliFNV2r3ShKIwUaI4Hw5FAJ+wkQQaP6ycnVEBKUECb0cRoYFF3Xk03v/uTPQf/mi0ucomA6+6kPAZ06wHXuDvV8hXHMAYm3vlHdh7XoQNm5SuztQ/EgoTC+8bl61SiT66oVGhM+aBGMO1v4WEWU+zlPmox5lkaiX9DPkM7ugkWF5YLfaOHDtiqbMgyvhxo0fVYqg+aTHTD/ZVfOQ6pm9hoB9rW0juGb505I49XoU/bGY1sXsA89SfKW2x6FekEVxaM8xeNMBvR7ST7GkQyXx4Nl/zXjdkTIoEe80pkpKIId/DJuXiGF6jOPJfrmT/ekNBVxGZjwf4HbFj/dtcM72x4+0Xhd6sP/SeRDvNiGZMHA+H7iXloGwbgOmgUwjETzipGdoz1xxO0YEOHRPM/4o1bfSUZSePjbu+YJFSo5w5OXDYHcXhA/XgvytzzRYfXv2AT8lFxNlh5KrpEfNRl3F85VUkYAHROYj/pisb431dMH3HVs176QV6PWxR0+CIyc3secTz+oRA2igb381cG53WnmQPtJrQoSQRZ5JGnmxDz0QOXUCos+fjd4hc4vAu2UbOLJzkpNFLlFWqcFIpKSHzSA9uIdb2G2ZgCNnCrhKl4Br4aIRSahmTGMmGQZu3oDI8SOWyXi37wTPipVWhysx02Z5palXN5rxbTwrnq3te+FMzCdjrAUrjqPxNtDKsyre8rEUKqssDVXGDRVTVhAkMg0ofVZneFau1hdIpqB+GmcDZL+BZ/eaC3Zmerfv0uqTYfULtlO/TVwgHmoJUcfqUmvx4PGAs6jYfCexnfptQGL24/UMsvqAj3q72dRO+wioZ/YNZWcNq0ktekcwbxcEO0Q6mF0wkGFF8RpWtVso3ZxJT5xFkJ01ajGe6Blg14YKK/HDCV5b7SZxUqG/pphe4nQXuavq/SlZhSfeD4IUbFJKSroXuQJl4F4coFWl8khF4gXu/7hr/3NfIf7G9xnuX/py9UuAAQDXmoV5SCuuIwAAAABJRU5ErkJggg=="
                alt="">
            <span>西部管理平台</span>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="less">
.Header {
    color: #FFF;
    display: flex;
    height: 100%;
    align-items: center;

    .logo {
        display: flex;
        align-items: center;
        span {
            line-height: 1;
            font-size: 16px;
            padding-left: 10px;
        }
    }
}
</style>