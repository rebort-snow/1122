
---
title: 'Chris'
date: 2023-10-01 09:15:35
tag: 红药丸
---

<div id="aplayer"></div>

<script>
const ap = new APlayer({
    container: document.getElementById('aplayer'),
    audio: [
        {
            name: '01什么是高阶聊天【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/01%E4%BB%80%E4%B9%88%E6%98%AF%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '02社交软件核心算法【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/02%E7%A4%BE%E4%BA%A4%E8%BD%AF%E4%BB%B6%E6%A0%B8%E5%BF%83%E7%AE%97%E6%B3%95%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '03聊天结构模型上【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/03%E8%81%8A%E5%A4%A9%E7%BB%93%E6%9E%84%E6%A8%A1%E5%9E%8B%E4%B8%8A%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '04聊天结构模型下【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/04%E8%81%8A%E5%A4%A9%E7%BB%93%E6%9E%84%E6%A8%A1%E5%9E%8B%E4%B8%8B%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '05开始聊天【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/05%E5%BC%80%E5%A7%8B%E8%81%8A%E5%A4%A9%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '06氛围营造＆个性样本【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/06%E6%B0%9B%E5%9B%B4%E8%90%A5%E9%80%A0%EF%BC%86%E4%B8%AA%E6%80%A7%E6%A0%B7%E6%9C%AC%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '07价值＆生活模式样本【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/07%E4%BB%B7%E5%80%BC%EF%BC%86%E7%94%9F%E6%B4%BB%E6%A8%A1%E5%BC%8F%E6%A0%B7%E6%9C%AC%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '08升级核心技巧【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/08%E5%8D%87%E7%BA%A7%E6%A0%B8%E5%BF%83%E6%8A%80%E5%B7%A7%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '09收尾（邀约）【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/09%E6%94%B6%E5%B0%BE%EF%BC%88%E9%82%80%E7%BA%A6%EF%BC%89%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶技术pro【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E6%8A%80%E6%9C%AFpro%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第一集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E4%B8%80%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第二集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E4%BA%8C%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第三集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E4%B8%89%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第四集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E5%9B%9B%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第五集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E4%BA%94%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第六集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E5%85%AD%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第七集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E4%B8%83%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }, 
        {
            name: '高阶聊天第八集【WWW.PUACP.COM】.mp3',
            artist: '艺术家',
            url: 'https://cdn.nidhogg-110.cn/music/chirs%E8%81%8A%E5%A4%A9/%E9%AB%98%E9%98%B6%E8%81%8A%E5%A4%A9%E7%AC%AC%E5%85%AB%E9%9B%86%E3%80%90WWW.PUACP.COM%E3%80%91.mp3',
            cover: 'http://cdn.nidhogg-110.cn/typora/channels4_profile.jpg'
        }]
});
</script>
