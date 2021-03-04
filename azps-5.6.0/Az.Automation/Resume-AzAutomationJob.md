---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 68520eda43b3586e63930b6a96cec2fc6483c594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957752"
---
# <span data-ttu-id="59645-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="59645-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="59645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59645-102">SYNOPSIS</span></span>
<span data-ttu-id="59645-103">Возобновление приостановленного задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="59645-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="59645-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59645-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59645-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59645-105">DESCRIPTION</span></span>
<span data-ttu-id="59645-106">Для приостановки задания автоматизации Azure будет возобновлено действие из cmdlet **Resume-AzAutomationJob.**</span><span class="sxs-lookup"><span data-stu-id="59645-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="59645-107">Задание приостановленного задания.</span><span class="sxs-lookup"><span data-stu-id="59645-107">Specify the suspended job.</span></span>
<span data-ttu-id="59645-108">Чтобы приостановить задание, воспользуйтесь Suspend-AzAutomationJob управления.</span><span class="sxs-lookup"><span data-stu-id="59645-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="59645-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59645-109">EXAMPLES</span></span>

### <span data-ttu-id="59645-110">Пример 1. Возобновление приостановленного задания</span><span class="sxs-lookup"><span data-stu-id="59645-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="59645-111">Эта команда возобновляет задание с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="59645-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="59645-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59645-112">PARAMETERS</span></span>

### <span data-ttu-id="59645-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="59645-113">-AutomationAccountName</span></span>
<span data-ttu-id="59645-114">Указывает имя учетной записи автоматизации, в которой этот cmdlet возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="59645-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59645-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59645-115">-DefaultProfile</span></span>
<span data-ttu-id="59645-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="59645-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59645-117">-Id</span><span class="sxs-lookup"><span data-stu-id="59645-117">-Id</span></span>
<span data-ttu-id="59645-118">Определяет код задания, которое этот cmdlet возобновляет.</span><span class="sxs-lookup"><span data-stu-id="59645-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59645-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59645-119">-ResourceGroupName</span></span>
<span data-ttu-id="59645-120">Указывает имя группы ресурсов, для которой этот cmdlet возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="59645-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59645-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59645-121">CommonParameters</span></span>
<span data-ttu-id="59645-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59645-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59645-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59645-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59645-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59645-124">INPUTS</span></span>

### <span data-ttu-id="59645-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="59645-125">System.Guid</span></span>

### <span data-ttu-id="59645-126">System.String</span><span class="sxs-lookup"><span data-stu-id="59645-126">System.String</span></span>

## <span data-ttu-id="59645-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59645-127">OUTPUTS</span></span>

### <span data-ttu-id="59645-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="59645-128">System.Void</span></span>

## <span data-ttu-id="59645-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59645-129">NOTES</span></span>

## <span data-ttu-id="59645-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59645-130">RELATED LINKS</span></span>

[<span data-ttu-id="59645-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="59645-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="59645-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="59645-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="59645-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="59645-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="59645-134">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="59645-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


