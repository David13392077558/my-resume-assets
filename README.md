import { Mail, Phone, GraduationCap, Code2, Award } from "lucide-react";

export default function Resume() {
    // 实际使用时，请将此URL替换为您的图片公开访问地址
    // 本地图片需要先上传到网络或转换为Base64
    const avatarUrl = "https://example.com/your-avatar.jpg"; // 替换为真实图片URL
    // 本地图片Base64示例（实际使用时删除这行）：
    // const avatarUrl = "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQ..."; 

    return (
        <div className="min-h-screen bg-blue-50 p-8 flex justify-center items-center">
            <div className="w-full max-w-3xl bg-white rounded-2xl shadow-xl overflow-hidden">
                {/* 左侧基本信息 */}
                <div className="bg-blue-600 p-6 flex flex-col items-center md:items-start">
                    {/* 头像组件 - 添加了加载状态处理 */}
                    <img 
                        src={avatarUrl || "https://yiyan.baidu.com/eb/shortLink/image/original?code=3yfhQwj"} 
                        alt="个人头像"
                        className="w-32 h-32 rounded-full mb-4 border-4 border-white shadow-md object-cover"
                        onError={(e) => {
                            // 如果图片加载失败，显示默认头像
                            e.currentTarget.src = "https://yiyan.baidu.com/eb/shortLink/image/original?code=3yfnkfX";
                        }}
                        loading="lazy"
                    />
                    <h1 className="text-3xl font-bold text-white mb-1">梁子羿</h1>
                    <div className="flex items-center text-blue-100 mb-2">
                        <Phone size={18} className="mr-2" />
                        <span className="text-sm">166-2463-3403</span>
                    </div>
                    <div className="flex items-center text-blue-100">
                        <Mail size={18} className="mr-2" />
                        <span className="text-sm">2428511134@qq.com</span>
                    </div>
                </div>

                {/* 右侧内容保持不变 */}
                <div className="p-6 md:p-8 space-y-6">
                    {/* 教育经历卡片 */}
                    <div className="bg-white p-6 rounded-2xl shadow-md border border-blue-100">
                        <div className="flex items-center mb-4">
                            <GraduationCap className="text-blue-600 mr-2" />
                            <h2 className="text-xl font-bold text-gray-800">教育经历</h2>
                        </div>
                        <div className="space-y-3">
                            <div>
                                <h3 className="font-semibold text-blue-700">广东外语外贸大学 · 人工智能</h3>
                                <p className="text-sm text-gray-600">2024年至今</p>
                            </div>
                            <ul className="list-disc pl-5 space-y-1 text-gray-700">
                                <li>GPA: 3.6/4.0 (专业前15%)</li>
                                <li>核心课程: 机器学习(92)、数据结构(88)、人工智能导论(90)</li>
                                <li>2024年新生奖学金获得者</li>
                                <li>参与校级AI研究项目：基于深度学习的图像分类</li>
                            </ul>
                        </div>
                    </div>

                    {/* 专业技能卡片 */}
                    <div className="bg-white p-6 rounded-2xl shadow-md border border-blue-100">
                        <div className="flex items-center mb-4">
                            <Code2 className="text-blue-600 mr-2" />
                            <h2 className="text-xl font-bold text-gray-800">专业技能</h2>
                        </div>
                        <div className="space-y-4">
                            <div>
                                <h3 className="font-semibold text-blue-700">Office办公软件</h3>
                                <ul className="list-disc pl-5 space-y-1 text-gray-700">
                                    <li>Excel: 精通数据可视化、Power Query数据清洗、高级函数应用</li>
                                    <li>PPT: 擅长科技类演示设计，掌握动画效果和交互式元素</li>
                                    <li>Word: 精通学术论文排版，熟悉样式集和参考文献管理</li>
                                </ul>
                            </div>
                            <div>
                                <h3 className="font-semibold text-blue-700">专业领域软件</h3>
                                <ul className="list-disc pl-5 space-y-1 text-gray-700">
                                    <li>Python: 熟练使用NumPy、Pandas、Matplotlib进行数据分析</li>
                                    <li>TensorFlow/PyTorch: 掌握基础神经网络构建和训练</li>
                                    <li>SQL: 熟悉数据库查询和优化</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    {/* 相关经验卡片 */}
                    <div className="bg-white p-6 rounded-2xl shadow-md border border-blue-100">
                        <div className="flex items-center mb-4">
                            <Award className="text-blue-600 mr-2" />
                            <h2 className="text-xl font-bold text-gray-800">相关经验</h2>
                        </div>
                        <div className="space-y-5">
                            <div>
                                <h3 className="font-semibold text-blue-700">广东区大学工程挑战赛</h3>
                                <p className="text-sm text-gray-600">2024年11月 - 2025年5月</p>
                                <ul className="list-disc pl-5 space-y-1 text-gray-700 mt-2">
                                    <li>担任算法组核心成员，负责智能推荐系统开发</li>
                                    <li>实现基于协同过滤的推荐算法，准确率提升25%</li>
                                    <li>项目进入省级决赛，目前排名前10%</li>
                                </ul>
                            </div>
                            <div>
                                <h3 className="font-semibold text-blue-700">校园AI技术沙龙发起人</h3>
                                <p className="text-sm text-gray-600">2024年8月 - 2024年10月</p>
                                <ul className="list-disc pl-5 space-y-1 text-gray-700 mt-2">
                                    <li>发起并组织AI技术交流活动，吸引150+学生参与</li>
                                    <li>邀请3位企业AI工程师进行实战经验分享</li>
                                    <li>建立校级AI学习社群，目前成员超300人</li>
                                    <li>活动被学校公众号报道，获得"优秀社团活动"称号</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    );
}
