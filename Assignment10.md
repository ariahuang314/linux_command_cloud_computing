# 实践指南

本次作业的目的是让你们熟悉 github 的基本操作。

以小组（不超过四人）为单位，从 github 仓库中的一个指定文件中寻找 typo 并提出修复的 PR。每个小组被要求找到并修复恰好三个 typo，并且要注意避免和其他小组重复。可以使用 github 的搜索功能来检查是否有重复的 PR。

如果小队恰好是四个人，可以由队长负责合并队员的 PR，其他三人提供 typo 修复。少于四人的小队可以自行分配每个人多少修改。（不影响个人评分）

具体步骤如下：

1. 初期工作
   - 队长访问 <https://github.com/X-lab2017/oss101> fork 此仓库。
   - 克隆到本地，创建 `team-<队长学号>` （例如 `team-5555903XXX`） 的分支，作为团队的工作分支。
   - 队长创建好 PR 之后，立即提交 draft PR。标题可以暂定为 `typo:`，也可以优先占坑，例如 `` typo: `peple` at line 27, `throu gh` at line 109 ... ``，即便你们 PR 内容还什么都没有，也可以表明你们先占有了这样里的 typo。（注意避免和其他已有同学重复）
   - 强调：我个人希望同学们不要急于求成，完全可以先占坑之后慢慢做协作的部分，不要因为仓促导致了复杂的问题。而从课程的角度我们鼓励出现复杂的问题给学生带来更好的 git 实践经历。
   - 队员 fork 队长的分支，也是采用 PR 的方式向队长分支提交 commit。结合所学 git 协作方法，队长采用 `Rebase and merge` 合并队员的分支避免引入 merge commit。队员的 commit massage 可以参考： `` Fix extra space typo `throu gh` at line 109 `` （添加行号是为了便于其他同学核对）
   - 鼓励队员 fork 队长仓库通过 PR 的方式来提交变更，而不是全队加入队长的仓库的 member 方式来协作。（这一点不强制，在评分上优先考虑第一种。）
2. 查看文件 `Assignments/Assignment-typo-for-cloud-computing.md`
   - 本作业的主要工作是在 `Assignment-typo-for-cloud-computing.md` 内部寻找以下几种有限类型的错误，并且除此之外不能包含例如排版，不可见字符，增减空行的修改。如果你有额外的想贡献的内容，我们欢迎额外提单独的 PR。
     - Skip letter 20
     - Extra letter 10
     - Skip spaces 15
     - Extra space 10
     - Wrong letter 10
   - 为便于查找 typo，我推荐对比原文，或者使用语法检查工具：
     - 原文： <http://www.catb.org/~esr/faqs/smart-questions.html>
     - 语法检查工具：<https://www.grammarly.com/blog/category/handbook/>
3. 修复 typo，转化 draft PR。
   - PR 的内容参考见下文的示例，注意随时可以编辑标题和正文内容。
   - 队长注意检查 PR 页面的 `Commits` 和 `Files changed` 标签，确保变更内容和文本都正常规范（不能有多余的 change）。
   - 在完成了队内协作以后，可以点击 draft PR 页面的按钮，ready for review 转化成常规 PR。
   - PR 的标题要以 `` typo: `<typo原文>` at <行号>, ... `` 作为标题，例如 `` typo: `peple` at line 27, `throu gh` at line 109，`th gh` at line ``（这样做的目的也是便于其他同学核对检索）
   - 强调：一个小组的作业对应一个 PR，并且考虑到任务不复杂， git 可以完全可以重做分支所以本次作业 PR 不允许自行关闭重开。
   - 鼓励队员 fork 队长仓库通过 PR 的方式来提交变更，而不是全队加入队长的仓库的 member 方式来协作。（在评分上优先考虑第一种，但不强制这一点。）
4. 等待助教或老师审核 PR
   - 助教可能会给出 approve，但不一定保证没有冲突，冲突会在 merge 阶段报告。
   - 助教大概率不会马上合并所有 PR，所以要注意不要与已有的同学冲突。
   - 假如大多数同学已经被助教 approve，那么助教会开始按时间顺序合入 PR，如果有同学被 check 到有冲突，助教会把 PR 打回 draft PR 并且合入顺序会调到下一次合入。请注意及时修改。在这个阶段有一定概率，你们会被后面与你冲突的人二次覆盖，所以希望大家仔细检查尽量一次通过。

作业的评分标准如下（本次实验在云计算课程中只记录通过情况，考虑到同学其他安排也繁忙，尽量提早完成避免意外）：

- 内容：typo 是否正确识别和修复、没有重复和额外的修改、并且和修改内容保持一致（许多人会忘记这一点）
- 协作：是否恰好包含全体队员的 commits（4 人团队的队长例外）。
- 格式：PR 以及 commits 的内容是否标准规范。
- 综合：以上内容都会给出机会修改，评分会优先考虑被助教给出意见较少的团队。
  - 为避免惨剧发生，建议队长仔细检查 file diff 查看变更是否正常。在确保一切正常以后再转化 PR 邀请审查。一人出错可以包容，而我们都不希望出现多人疏忽的小概率事件。

作业的截止日期是 2023 年 5 月 28 日 23:59。请在截止日期前提交 PR，并确保 PR 能够被合并。逾期提交或提交失败的作业将不予评分。如果你们在完成作业的过程中遇到任何问题或困难，请及时联系老师或助教。

## 附录 1 PR 示例

以下是一个更清晰 PR 文本的例子，标题代表 PR 的标题，之后是 PR 的正文，请同学们务必参考：

<table>
  <tr>
    <td> markdown </td>
    <td> 预览 </td>
  </tr>
  <tr>
<td>

```markdown
标题 typo: `peple` at line 27, `throu gh` at line 109

fixes #143

- fix extra space typo `throu gh` at line 109 to `through` @whofixit
- fix skip letter typo `lbrary` at line 111 to `library` @whofixit

team: 522759030XX 522759030XX
```

</td>
<td>

标题 typo: `peple` at line 27, `throu gh` at line 109

fixes #143

- fix extra space typo `throu gh` at line 109 to `through` @whofixit
- fix skip letter typo `lbrary` at line 111 to `library` @whofixit

team: 522759030XX 522759030XX

</td>
</tr>
</table>

`@whofixit` 是 @ 团队成员的 GitHub id。

## 附录 2 重要警示

我们的文档中存在一种非空格的不可见字符 [Unicode Character 'NO-BREAK SPACE' (U+00A0)](https://www.fileformat.info/info/unicode/char/00a0/index.htm)，顾名思义，他是一种不折行的空格。

但非常不巧，它和我们常用的空格 [SPACE (U+0020)](https://www.fileformat.info/info/unicode/char/0020/index.htm) 是两种完全不同的符号。我观察到有部分同学的 commit 中，可能因为一些意外（比如使用 GitHub 内置的文本编辑），导致这个符号被转换了。

进而导致引入了额外的变更。请各位同学和队长留心 review code diff，因为额外的变更在 diff 中是很显而易见的。
