---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080087"
---
# <span data-ttu-id="6f29c-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f29c-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="6f29c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f29c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f29c-103">Возвращает расписание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6f29c-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="6f29c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f29c-104">SYNTAX</span></span>

### <span data-ttu-id="6f29c-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f29c-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f29c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f29c-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f29c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f29c-107">DESCRIPTION</span></span>
<span data-ttu-id="6f29c-108">Командлет **Get-AzAutomationSchedule** получает расписание автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6f29c-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="6f29c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f29c-109">EXAMPLES</span></span>

### <span data-ttu-id="6f29c-110">Пример 1: получение расписания</span><span class="sxs-lookup"><span data-stu-id="6f29c-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6f29c-111">Эта команда получает расписание с именем DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="6f29c-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="6f29c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f29c-112">PARAMETERS</span></span>

### <span data-ttu-id="6f29c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f29c-113">-AutomationAccountName</span></span>
<span data-ttu-id="6f29c-114">Указывает имя учетной записи автоматизации, для которой этот командлет получает расписание.</span><span class="sxs-lookup"><span data-stu-id="6f29c-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="6f29c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f29c-115">-DefaultProfile</span></span>
<span data-ttu-id="6f29c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6f29c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f29c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f29c-117">-Name</span></span>
<span data-ttu-id="6f29c-118">Указывает имя расписания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f29c-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f29c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f29c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f29c-120">Указывает имя группы ресурсов, для которой этот командлет получает расписание.</span><span class="sxs-lookup"><span data-stu-id="6f29c-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="6f29c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f29c-121">CommonParameters</span></span>
<span data-ttu-id="6f29c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f29c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f29c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f29c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f29c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f29c-124">INPUTS</span></span>

### <span data-ttu-id="6f29c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6f29c-125">System.String</span></span>

## <span data-ttu-id="6f29c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f29c-126">OUTPUTS</span></span>

### <span data-ttu-id="6f29c-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="6f29c-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="6f29c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f29c-128">NOTES</span></span>

## <span data-ttu-id="6f29c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f29c-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f29c-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f29c-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="6f29c-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f29c-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="6f29c-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6f29c-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

