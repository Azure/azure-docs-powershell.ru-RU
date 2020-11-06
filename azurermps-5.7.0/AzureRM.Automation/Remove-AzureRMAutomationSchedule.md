---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 83481e1d12782c3381c2d5923aa610072da41d9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569048"
---
# <span data-ttu-id="7a465-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7a465-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="7a465-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a465-102">SYNOPSIS</span></span>
<span data-ttu-id="7a465-103">Удаление расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7a465-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a465-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a465-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a465-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a465-105">DESCRIPTION</span></span>
<span data-ttu-id="7a465-106">Командлет **Remove-AzureRmAutomationSchedule** Удаляет расписание из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7a465-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="7a465-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a465-107">EXAMPLES</span></span>

### <span data-ttu-id="7a465-108">Пример 1: Удаление расписания</span><span class="sxs-lookup"><span data-stu-id="7a465-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7a465-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="7a465-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="7a465-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a465-110">PARAMETERS</span></span>

### <span data-ttu-id="7a465-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a465-111">-AutomationAccountName</span></span>
<span data-ttu-id="7a465-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="7a465-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="7a465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a465-113">-DefaultProfile</span></span>
<span data-ttu-id="7a465-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a465-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a465-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a465-115">-Force</span></span>
<span data-ttu-id="7a465-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7a465-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a465-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a465-117">-Name</span></span>
<span data-ttu-id="7a465-118">Указывает имя расписания, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7a465-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a465-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a465-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a465-120">Указывает имя группы ресурсов, для которой этот командлет удаляет расписание.</span><span class="sxs-lookup"><span data-stu-id="7a465-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="7a465-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a465-121">-Confirm</span></span>
<span data-ttu-id="7a465-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a465-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a465-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a465-123">-WhatIf</span></span>
<span data-ttu-id="7a465-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a465-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a465-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a465-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a465-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a465-126">CommonParameters</span></span>
<span data-ttu-id="7a465-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a465-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a465-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a465-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a465-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a465-129">INPUTS</span></span>

### <span data-ttu-id="7a465-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="7a465-130">None</span></span>
<span data-ttu-id="7a465-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7a465-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a465-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a465-132">OUTPUTS</span></span>

## <span data-ttu-id="7a465-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a465-133">NOTES</span></span>

## <span data-ttu-id="7a465-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a465-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a465-135">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7a465-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="7a465-136">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7a465-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="7a465-137">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7a465-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


