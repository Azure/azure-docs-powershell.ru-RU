---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: b311554fa5aeeae67829055506b85766fd6f9670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566249"
---
# <span data-ttu-id="97184-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="97184-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="97184-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97184-102">SYNOPSIS</span></span>
<span data-ttu-id="97184-103">Изменение расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="97184-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97184-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97184-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97184-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97184-105">DESCRIPTION</span></span>
<span data-ttu-id="97184-106">Командлет **Set-AzureRmAutomationSchedule** изменяет расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="97184-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="97184-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97184-107">EXAMPLES</span></span>

### <span data-ttu-id="97184-108">Пример 1: изменение расписания</span><span class="sxs-lookup"><span data-stu-id="97184-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="97184-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="97184-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="97184-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97184-110">PARAMETERS</span></span>

### <span data-ttu-id="97184-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97184-111">-AutomationAccountName</span></span>
<span data-ttu-id="97184-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="97184-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="97184-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97184-113">-DefaultProfile</span></span>
<span data-ttu-id="97184-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97184-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97184-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="97184-115">-Description</span></span>
<span data-ttu-id="97184-116">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="97184-116">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97184-117">-Включено</span><span class="sxs-lookup"><span data-stu-id="97184-117">-IsEnabled</span></span>
<span data-ttu-id="97184-118">Указывает, включает ли этот командлет расписание.</span><span class="sxs-lookup"><span data-stu-id="97184-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97184-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97184-119">-Name</span></span>
<span data-ttu-id="97184-120">Указывает имя расписания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="97184-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97184-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97184-121">-ResourceGroupName</span></span>
<span data-ttu-id="97184-122">Указывает имя группы ресурсов, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="97184-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="97184-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97184-123">CommonParameters</span></span>
<span data-ttu-id="97184-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97184-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97184-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97184-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97184-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97184-126">INPUTS</span></span>

### <span data-ttu-id="97184-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="97184-127">None</span></span>
<span data-ttu-id="97184-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="97184-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97184-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97184-129">OUTPUTS</span></span>

### <span data-ttu-id="97184-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="97184-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="97184-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="97184-131">NOTES</span></span>

## <span data-ttu-id="97184-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97184-132">RELATED LINKS</span></span>

[<span data-ttu-id="97184-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="97184-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="97184-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="97184-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="97184-135">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="97184-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


