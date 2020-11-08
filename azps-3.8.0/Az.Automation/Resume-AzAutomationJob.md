---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074918"
---
# <span data-ttu-id="651fd-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="651fd-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="651fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="651fd-102">SYNOPSIS</span></span>
<span data-ttu-id="651fd-103">Возобновление приостановленного задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="651fd-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="651fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="651fd-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="651fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="651fd-105">DESCRIPTION</span></span>
<span data-ttu-id="651fd-106">Командлет **Resume-AzAutomationJob** возобновляет приостановленное задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="651fd-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="651fd-107">Укажите приостановленное задание.</span><span class="sxs-lookup"><span data-stu-id="651fd-107">Specify the suspended job.</span></span>
<span data-ttu-id="651fd-108">Чтобы приостановить задание, используйте командлет Suspend-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="651fd-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="651fd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="651fd-109">EXAMPLES</span></span>

### <span data-ttu-id="651fd-110">Пример 1: возобновление приостановленного задания</span><span class="sxs-lookup"><span data-stu-id="651fd-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="651fd-111">Эта команда возобновляет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="651fd-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="651fd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="651fd-112">PARAMETERS</span></span>

### <span data-ttu-id="651fd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="651fd-113">-AutomationAccountName</span></span>
<span data-ttu-id="651fd-114">Указывает имя учетной записи автоматизации, в которой этот командлет возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="651fd-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="651fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651fd-115">-DefaultProfile</span></span>
<span data-ttu-id="651fd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="651fd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="651fd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="651fd-117">-Id</span></span>
<span data-ttu-id="651fd-118">Указывает идентификатор задания, возобновляемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="651fd-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="651fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="651fd-120">Указывает имя группы ресурсов, для которой этот командлет возобновляет задание.</span><span class="sxs-lookup"><span data-stu-id="651fd-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="651fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651fd-121">CommonParameters</span></span>
<span data-ttu-id="651fd-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="651fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651fd-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651fd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651fd-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="651fd-124">INPUTS</span></span>

### <span data-ttu-id="651fd-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="651fd-125">System.Guid</span></span>

### <span data-ttu-id="651fd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="651fd-126">System.String</span></span>

## <span data-ttu-id="651fd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="651fd-127">OUTPUTS</span></span>

### <span data-ttu-id="651fd-128">System. void</span><span class="sxs-lookup"><span data-stu-id="651fd-128">System.Void</span></span>

## <span data-ttu-id="651fd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="651fd-129">NOTES</span></span>

## <span data-ttu-id="651fd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="651fd-130">RELATED LINKS</span></span>

[<span data-ttu-id="651fd-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="651fd-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="651fd-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="651fd-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="651fd-133">Остановить-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="651fd-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="651fd-134">Приостановить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="651fd-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


