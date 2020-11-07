---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: c5f7348d59b18a3e0cedfcf52c22c4328c28944a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731497"
---
# <span data-ttu-id="58a28-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="58a28-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="58a28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58a28-102">SYNOPSIS</span></span>
<span data-ttu-id="58a28-103">Изменение расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="58a28-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="58a28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58a28-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58a28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58a28-105">DESCRIPTION</span></span>
<span data-ttu-id="58a28-106">Командлет **Set-AzAutomationSchedule** изменяет расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="58a28-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="58a28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58a28-107">EXAMPLES</span></span>

### <span data-ttu-id="58a28-108">Пример 1: изменение расписания</span><span class="sxs-lookup"><span data-stu-id="58a28-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58a28-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="58a28-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="58a28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58a28-110">PARAMETERS</span></span>

### <span data-ttu-id="58a28-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="58a28-111">-AutomationAccountName</span></span>
<span data-ttu-id="58a28-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="58a28-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="58a28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a28-113">-DefaultProfile</span></span>
<span data-ttu-id="58a28-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="58a28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58a28-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="58a28-115">-Description</span></span>
<span data-ttu-id="58a28-116">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="58a28-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="58a28-117">-Включено</span><span class="sxs-lookup"><span data-stu-id="58a28-117">-IsEnabled</span></span>
<span data-ttu-id="58a28-118">Указывает, включает ли этот командлет расписание.</span><span class="sxs-lookup"><span data-stu-id="58a28-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="58a28-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58a28-119">-Name</span></span>
<span data-ttu-id="58a28-120">Указывает имя расписания, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="58a28-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="58a28-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a28-121">-ResourceGroupName</span></span>
<span data-ttu-id="58a28-122">Указывает имя группы ресурсов, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="58a28-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="58a28-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a28-123">CommonParameters</span></span>
<span data-ttu-id="58a28-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58a28-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a28-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a28-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a28-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58a28-126">INPUTS</span></span>

### <span data-ttu-id="58a28-127">System. String</span><span class="sxs-lookup"><span data-stu-id="58a28-127">System.String</span></span>

### <span data-ttu-id="58a28-128">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58a28-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="58a28-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58a28-129">OUTPUTS</span></span>

### <span data-ttu-id="58a28-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="58a28-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="58a28-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="58a28-131">NOTES</span></span>

## <span data-ttu-id="58a28-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58a28-132">RELATED LINKS</span></span>

[<span data-ttu-id="58a28-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="58a28-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="58a28-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="58a28-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="58a28-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="58a28-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


