---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 0820905ff8a4673c9abae56be2f7792912095e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563140"
---
# <span data-ttu-id="d11a0-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d11a0-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="d11a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d11a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d11a0-103">Приостанавливает задание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d11a0-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d11a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d11a0-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d11a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d11a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d11a0-106">Командлет **Suspend-AzureRmAutomationJob** приостанавливает задание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d11a0-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="d11a0-107">Укажите выполнение задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d11a0-107">Specify a running Automation job.</span></span>
<span data-ttu-id="d11a0-108">Чтобы возобновить приостановленное задание, используйте командлет Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="d11a0-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="d11a0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d11a0-109">EXAMPLES</span></span>

### <span data-ttu-id="d11a0-110">Пример 1: Приостановка задания</span><span class="sxs-lookup"><span data-stu-id="d11a0-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d11a0-111">Эта команда приостанавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="d11a0-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="d11a0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d11a0-112">PARAMETERS</span></span>

### <span data-ttu-id="d11a0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d11a0-113">-AutomationAccountName</span></span>
<span data-ttu-id="d11a0-114">Указывает имя учетной записи автоматизации, в которой этот командлет приостанавливает задание.</span><span class="sxs-lookup"><span data-stu-id="d11a0-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="d11a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11a0-115">-DefaultProfile</span></span>
<span data-ttu-id="d11a0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d11a0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d11a0-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d11a0-117">-Id</span></span>
<span data-ttu-id="d11a0-118">Указывает идентификатор задания, приостановки которого является этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d11a0-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d11a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="d11a0-120">Указывает идентификатор задания, приостановки которого является этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d11a0-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d11a0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11a0-121">CommonParameters</span></span>
<span data-ttu-id="d11a0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d11a0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11a0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11a0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11a0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d11a0-124">INPUTS</span></span>

### <span data-ttu-id="d11a0-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d11a0-125">System.Guid</span></span>

### <span data-ttu-id="d11a0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d11a0-126">System.String</span></span>

## <span data-ttu-id="d11a0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d11a0-127">OUTPUTS</span></span>

### <span data-ttu-id="d11a0-128">System. void</span><span class="sxs-lookup"><span data-stu-id="d11a0-128">System.Void</span></span>

## <span data-ttu-id="d11a0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d11a0-129">NOTES</span></span>

## <span data-ttu-id="d11a0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d11a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="d11a0-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d11a0-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="d11a0-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d11a0-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="d11a0-133">Возобновить — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d11a0-133">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="d11a0-134">Остановить-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d11a0-134">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


