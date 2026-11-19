# 海外 OEM 客户开发 Skill

帮化妆品或个护 OEM/ODM 工厂每天寻找海外品牌客户，用对方母语写好开发信草稿，并同步到表格和 CRM。只存草稿，不会擅自发信。

这是从公开的 [海外OEM客户开发助手](https://x.ai/bot/xe5WHnuK_NdTmAClDLtxr) 工作流整理出的可安装 Skill，已去掉具体公司、账号和客户数据。你填好自己的公司资料后即可使用。

## 它能做什么

- 按目标市场寻找海外独立护肤或个护品牌，并先去重
- 补全公开邮箱、电话、WhatsApp、决策人和社媒，并注明来源
- 研究品牌后再用对方母语写定制开发信（约 150 词以内）
- 把草稿存进企业邮箱草稿箱，或先把完整草稿交给你审核
- 有公开邮箱的客户才写入 CRM；没有邮箱的只留在表格里

## 安装

### 用 skills CLI（推荐）

```bash
npx skills add https://github.com/XIAOMAGE8868/overseas-oem-customer-development
```

如果只要这一个技能，也可以：

```bash
npx skills add https://github.com/XIAOMAGE8868/overseas-oem-customer-development --skill overseas-oem-customer-development
```

### 手动安装

把本仓库复制到你的助手技能目录，例如：

```bash
git clone https://github.com/XIAOMAGE8868/overseas-oem-customer-development.git
cp -r overseas-oem-customer-development ~/.claude/skills/overseas-oem-customer-development
# 或 Cursor / Codex 等技能目录
```

### 在 Grok Bot 里用

把本仓库链接发给你的 Bot，或把 `SKILL.md` 上传给它，告诉它按这份技能执行。你也可以直接复制已发布的 [海外OEM客户开发助手](https://x.ai/bot/xe5WHnuK_NdTmAClDLtxr)。

## 使用前准备

1. 填写 [templates/company-profile.md](templates/company-profile.md)：公司事实、产品手册位置、署名、目标市场、每天新客户数量等
2. 准备一张客户名单表格，字段见 [templates/lead-sheet.md](templates/lead-sheet.md)
3. 如需自动存草稿和同步 CRM，请连接企业邮箱、表格工具（如 Google 表格）和 CRM（如 HubSpot）
4. 对企业网页邮箱，建议把登录信息存在保险库，不要写进技能文件

准备好后，对助手说：

> 先找 1 家客户并写一封开发信草稿

它会先确认公司信息和发信规则，再开始。

## 仓库结构

- `SKILL.md`：完整工作流和硬性规则
- `templates/company-profile.md`：公司资料模板
- `templates/lead-sheet.md`：客户表字段
- `references/google-search-operators.md`：外贸获客常用搜索指令

## 注意事项

- 千万不要让助手自己点发送。
- 不要编造联系方式或公司能力。
- 没有公开邮箱的客户不要进 CRM。
- 如果启用每天定时找客户、写草稿和汇报，额度消耗会比较大。
- 网页邮箱可能掉线或显示其他时区，核对发送记录时要先换算。
- 本技能不是买家数据库，也不会自动群发。

## 许可

MIT License。欢迎下载、修改和用于自己的工厂获客流程。
