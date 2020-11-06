---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 2b35281cd276be9149f2d4c4e17cb38f48eadc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568263"
---
# <span data-ttu-id="6def6-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6def6-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="6def6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6def6-102">SYNOPSIS</span></span>
<span data-ttu-id="6def6-103">Возвращает расписание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6def6-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6def6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6def6-104">SYNTAX</span></span>

### <span data-ttu-id="6def6-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6def6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6def6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6def6-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6def6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6def6-107">DESCRIPTION</span></span>
<span data-ttu-id="6def6-108">Командлет **Get-AzureRmAutomationSchedule** получает расписание автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6def6-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="6def6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6def6-109">EXAMPLES</span></span>

### <span data-ttu-id="6def6-110">Пример 1: получение расписания</span><span class="sxs-lookup"><span data-stu-id="6def6-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6def6-111">Эта команда получает расписание с именем DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="6def6-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="6def6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6def6-112">PARAMETERS</span></span>

### <span data-ttu-id="6def6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6def6-113">-AutomationAccountName</span></span>
<span data-ttu-id="6def6-114">Указывает имя учетной записи автоматизации, для которой этот командлет получает расписание.</span><span class="sxs-lookup"><span data-stu-id="6def6-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6def6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6def6-115">-DefaultProfile</span></span>
<span data-ttu-id="6def6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6def6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6def6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6def6-117">-Name</span></span>
<span data-ttu-id="6def6-118">Указывает имя расписания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6def6-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6def6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6def6-119">-ResourceGroupName</span></span>
<span data-ttu-id="6def6-120">Указывает имя группы ресурсов, для которой этот командлет получает расписание.</span><span class="sxs-lookup"><span data-stu-id="6def6-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6def6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6def6-121">CommonParameters</span></span>
<span data-ttu-id="6def6-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6def6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6def6-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6def6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6def6-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6def6-124">INPUTS</span></span>

### <span data-ttu-id="6def6-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="6def6-125">None</span></span>
<span data-ttu-id="6def6-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6def6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6def6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6def6-127">OUTPUTS</span></span>

### <span data-ttu-id="6def6-128">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="6def6-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="6def6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6def6-129">NOTES</span></span>

## <span data-ttu-id="6def6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6def6-130">RELATED LINKS</span></span>

[<span data-ttu-id="6def6-131">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6def6-131">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6def6-132">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6def6-132">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6def6-133">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6def6-133">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


