---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 78e34c5d3d94a964fbff6d0cbaa74c9dd3dd2177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567317"
---
# <span data-ttu-id="19143-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19143-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="19143-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19143-102">SYNOPSIS</span></span>
<span data-ttu-id="19143-103">Возвращает расписание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="19143-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19143-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19143-104">SYNTAX</span></span>

### <span data-ttu-id="19143-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19143-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19143-106">ByName</span><span class="sxs-lookup"><span data-stu-id="19143-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19143-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19143-107">DESCRIPTION</span></span>
<span data-ttu-id="19143-108">Командлет **Get-AzureRmAutomationSchedule** получает расписание автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="19143-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="19143-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19143-109">EXAMPLES</span></span>

### <span data-ttu-id="19143-110">Пример 1: получение расписания</span><span class="sxs-lookup"><span data-stu-id="19143-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19143-111">Эта команда получает расписание с именем DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="19143-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="19143-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19143-112">PARAMETERS</span></span>

### <span data-ttu-id="19143-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19143-113">-AutomationAccountName</span></span>
<span data-ttu-id="19143-114">Указывает имя учетной записи автоматизации, для которой этот командлет получает расписание.</span><span class="sxs-lookup"><span data-stu-id="19143-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="19143-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19143-115">-DefaultProfile</span></span>
<span data-ttu-id="19143-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19143-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19143-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19143-117">-Name</span></span>
<span data-ttu-id="19143-118">Указывает имя расписания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19143-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19143-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19143-119">-ResourceGroupName</span></span>
<span data-ttu-id="19143-120">Указывает имя группы ресурсов, для которой этот командлет получает расписание.</span><span class="sxs-lookup"><span data-stu-id="19143-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="19143-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19143-121">CommonParameters</span></span>
<span data-ttu-id="19143-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19143-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19143-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19143-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19143-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19143-124">INPUTS</span></span>

### <span data-ttu-id="19143-125">System. String</span><span class="sxs-lookup"><span data-stu-id="19143-125">System.String</span></span>

## <span data-ttu-id="19143-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19143-126">OUTPUTS</span></span>

### <span data-ttu-id="19143-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="19143-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="19143-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="19143-128">NOTES</span></span>

## <span data-ttu-id="19143-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19143-129">RELATED LINKS</span></span>

[<span data-ttu-id="19143-130">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19143-130">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="19143-131">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19143-131">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="19143-132">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19143-132">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


