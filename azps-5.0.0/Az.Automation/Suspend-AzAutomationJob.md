---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249231"
---
# <span data-ttu-id="68248-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="68248-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="68248-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68248-102">SYNOPSIS</span></span>
<span data-ttu-id="68248-103">Приостанавливает задание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="68248-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="68248-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68248-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68248-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68248-105">DESCRIPTION</span></span>
<span data-ttu-id="68248-106">Командлет **Suspend-AzAutomationJob** приостанавливает задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="68248-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="68248-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="68248-107">Specify a running Automation job.</span></span>
<span data-ttu-id="68248-108">Чтобы возобновить приостановленное задание, используйте командлет Resume-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="68248-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="68248-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68248-109">EXAMPLES</span></span>

### <span data-ttu-id="68248-110">Пример 1: Приостановка задания</span><span class="sxs-lookup"><span data-stu-id="68248-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="68248-111">Эта команда приостанавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="68248-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="68248-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68248-112">PARAMETERS</span></span>

### <span data-ttu-id="68248-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68248-113">-AutomationAccountName</span></span>
<span data-ttu-id="68248-114">Указывает имя учетной записи автоматизации, в которой этот командлет приостанавливает задание.</span><span class="sxs-lookup"><span data-stu-id="68248-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="68248-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68248-115">-DefaultProfile</span></span>
<span data-ttu-id="68248-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="68248-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68248-117">-ID</span><span class="sxs-lookup"><span data-stu-id="68248-117">-Id</span></span>
<span data-ttu-id="68248-118">Указывает идентификатор задания, приостановки которого является этот командлет.</span><span class="sxs-lookup"><span data-stu-id="68248-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="68248-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68248-119">-ResourceGroupName</span></span>
<span data-ttu-id="68248-120">Указывает идентификатор задания, приостановки которого является этот командлет.</span><span class="sxs-lookup"><span data-stu-id="68248-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="68248-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68248-121">CommonParameters</span></span>
<span data-ttu-id="68248-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68248-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68248-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68248-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68248-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68248-124">INPUTS</span></span>

### <span data-ttu-id="68248-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="68248-125">System.Guid</span></span>

### <span data-ttu-id="68248-126">System. String</span><span class="sxs-lookup"><span data-stu-id="68248-126">System.String</span></span>

## <span data-ttu-id="68248-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68248-127">OUTPUTS</span></span>

### <span data-ttu-id="68248-128">System. void</span><span class="sxs-lookup"><span data-stu-id="68248-128">System.Void</span></span>

## <span data-ttu-id="68248-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="68248-129">NOTES</span></span>

## <span data-ttu-id="68248-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68248-130">RELATED LINKS</span></span>

[<span data-ttu-id="68248-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="68248-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="68248-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="68248-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="68248-133">Возобновить — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="68248-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="68248-134">Остановить-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="68248-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


