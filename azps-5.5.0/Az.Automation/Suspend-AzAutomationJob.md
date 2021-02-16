---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233668"
---
# <span data-ttu-id="97cd1-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97cd1-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="97cd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="97cd1-103">Приостановка задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="97cd1-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="97cd1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97cd1-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97cd1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="97cd1-106">Приостановка задания автоматизации Azure с использованием cmdlet **Suspend-AzAutomationJob.**</span><span class="sxs-lookup"><span data-stu-id="97cd1-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="97cd1-107">Задание запускаемой автоматизации.</span><span class="sxs-lookup"><span data-stu-id="97cd1-107">Specify a running Automation job.</span></span>
<span data-ttu-id="97cd1-108">Чтобы возобновить приостановленное задание, воспользуйтесь Resume-AzAutomationJob управления.</span><span class="sxs-lookup"><span data-stu-id="97cd1-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="97cd1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97cd1-109">EXAMPLES</span></span>

### <span data-ttu-id="97cd1-110">Пример 1. Приостановка задания</span><span class="sxs-lookup"><span data-stu-id="97cd1-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="97cd1-111">Эта команда приостанавливать задание с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="97cd1-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="97cd1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97cd1-112">PARAMETERS</span></span>

### <span data-ttu-id="97cd1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97cd1-113">-AutomationAccountName</span></span>
<span data-ttu-id="97cd1-114">Указывает имя учетной записи автоматизации, в которой этот cmdlet приостанавливал задание.</span><span class="sxs-lookup"><span data-stu-id="97cd1-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="97cd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cd1-115">-DefaultProfile</span></span>
<span data-ttu-id="97cd1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97cd1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97cd1-117">-Id</span><span class="sxs-lookup"><span data-stu-id="97cd1-117">-Id</span></span>
<span data-ttu-id="97cd1-118">Определяет код задания, которое этот cmdlet приостанавливал.</span><span class="sxs-lookup"><span data-stu-id="97cd1-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="97cd1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97cd1-119">-ResourceGroupName</span></span>
<span data-ttu-id="97cd1-120">Определяет код задания, которое этот cmdlet приостанавливал.</span><span class="sxs-lookup"><span data-stu-id="97cd1-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="97cd1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cd1-121">CommonParameters</span></span>
<span data-ttu-id="97cd1-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97cd1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cd1-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97cd1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cd1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97cd1-124">INPUTS</span></span>

### <span data-ttu-id="97cd1-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="97cd1-125">System.Guid</span></span>

### <span data-ttu-id="97cd1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="97cd1-126">System.String</span></span>

## <span data-ttu-id="97cd1-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97cd1-127">OUTPUTS</span></span>

### <span data-ttu-id="97cd1-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="97cd1-128">System.Void</span></span>

## <span data-ttu-id="97cd1-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97cd1-129">NOTES</span></span>

## <span data-ttu-id="97cd1-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97cd1-130">RELATED LINKS</span></span>

[<span data-ttu-id="97cd1-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97cd1-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="97cd1-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="97cd1-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="97cd1-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97cd1-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="97cd1-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97cd1-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


