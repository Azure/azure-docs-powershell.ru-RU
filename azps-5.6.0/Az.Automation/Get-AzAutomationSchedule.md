---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a32b86ce308f18537ec1acda62c2694e7b621d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014216"
---
# <span data-ttu-id="5e61d-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5e61d-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="5e61d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e61d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e61d-103">Получает расписание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5e61d-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="5e61d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e61d-104">SYNTAX</span></span>

### <span data-ttu-id="5e61d-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e61d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e61d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5e61d-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e61d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e61d-107">DESCRIPTION</span></span>
<span data-ttu-id="5e61d-108">Для получения календарного плана автоматизации Azure возвращается календарный план **Get-AzAutomationSchedule.**</span><span class="sxs-lookup"><span data-stu-id="5e61d-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="5e61d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e61d-109">EXAMPLES</span></span>

### <span data-ttu-id="5e61d-110">Пример 1. Получить расписание</span><span class="sxs-lookup"><span data-stu-id="5e61d-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5e61d-111">Эта команда получает расписание с именем DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="5e61d-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="5e61d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e61d-112">PARAMETERS</span></span>

### <span data-ttu-id="5e61d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e61d-113">-AutomationAccountName</span></span>
<span data-ttu-id="5e61d-114">Указывает имя учетной записи автоматизации, для которой этот cmdlet получит расписание.</span><span class="sxs-lookup"><span data-stu-id="5e61d-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="5e61d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e61d-115">-DefaultProfile</span></span>
<span data-ttu-id="5e61d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5e61d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e61d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e61d-117">-Name</span></span>
<span data-ttu-id="5e61d-118">Определяет имя календарного плана, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e61d-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5e61d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e61d-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e61d-120">Указывает имя группы ресурсов, для которой этот cmdlet получает расписание.</span><span class="sxs-lookup"><span data-stu-id="5e61d-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="5e61d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e61d-121">CommonParameters</span></span>
<span data-ttu-id="5e61d-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e61d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e61d-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e61d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e61d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e61d-124">INPUTS</span></span>

### <span data-ttu-id="5e61d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5e61d-125">System.String</span></span>

## <span data-ttu-id="5e61d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e61d-126">OUTPUTS</span></span>

### <span data-ttu-id="5e61d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="5e61d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="5e61d-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e61d-128">NOTES</span></span>

## <span data-ttu-id="5e61d-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e61d-129">RELATED LINKS</span></span>

[<span data-ttu-id="5e61d-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5e61d-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="5e61d-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5e61d-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="5e61d-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5e61d-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


