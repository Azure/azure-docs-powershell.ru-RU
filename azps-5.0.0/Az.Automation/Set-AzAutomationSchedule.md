---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247659"
---
# <span data-ttu-id="1ecc8-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1ecc8-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="1ecc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ecc8-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecc8-103">Изменение расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="1ecc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ecc8-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ecc8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecc8-105">DESCRIPTION</span></span>
<span data-ttu-id="1ecc8-106">Командлет **Set-AzAutomationSchedule** изменяет расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="1ecc8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ecc8-107">EXAMPLES</span></span>

### <span data-ttu-id="1ecc8-108">Пример 1: изменение расписания</span><span class="sxs-lookup"><span data-stu-id="1ecc8-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1ecc8-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="1ecc8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ecc8-110">PARAMETERS</span></span>

### <span data-ttu-id="1ecc8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ecc8-111">-AutomationAccountName</span></span>
<span data-ttu-id="1ecc8-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="1ecc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecc8-113">-DefaultProfile</span></span>
<span data-ttu-id="1ecc8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ecc8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ecc8-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="1ecc8-115">-Description</span></span>
<span data-ttu-id="1ecc8-116">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecc8-117">-Включено</span><span class="sxs-lookup"><span data-stu-id="1ecc8-117">-IsEnabled</span></span>
<span data-ttu-id="1ecc8-118">Указывает, включает ли этот командлет расписание.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecc8-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ecc8-119">-Name</span></span>
<span data-ttu-id="1ecc8-120">Указывает имя расписания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecc8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecc8-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ecc8-122">Указывает имя группы ресурсов, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="1ecc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecc8-123">CommonParameters</span></span>
<span data-ttu-id="1ecc8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecc8-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecc8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecc8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ecc8-126">INPUTS</span></span>

### <span data-ttu-id="1ecc8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1ecc8-127">System.String</span></span>

### <span data-ttu-id="1ecc8-128">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1ecc8-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1ecc8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecc8-129">OUTPUTS</span></span>

### <span data-ttu-id="1ecc8-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="1ecc8-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="1ecc8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ecc8-131">NOTES</span></span>

## <span data-ttu-id="1ecc8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ecc8-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ecc8-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1ecc8-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="1ecc8-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1ecc8-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="1ecc8-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1ecc8-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


