---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568338"
---
# <span data-ttu-id="140b7-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="140b7-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="140b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="140b7-102">SYNOPSIS</span></span>
<span data-ttu-id="140b7-103">Удаляет связь между модулем Runbook и расписанием.</span><span class="sxs-lookup"><span data-stu-id="140b7-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="140b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="140b7-104">SYNTAX</span></span>

### <span data-ttu-id="140b7-105">ByJobScheduleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="140b7-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="140b7-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="140b7-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="140b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="140b7-107">DESCRIPTION</span></span>
<span data-ttu-id="140b7-108">Командлет **Unregister-AzureRmAutomationScheduledRunbook** удаляет связь между Runbook и модулем автоматизации Azure и расписанием.</span><span class="sxs-lookup"><span data-stu-id="140b7-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="140b7-109">Расписание больше не запускает Runbook.</span><span class="sxs-lookup"><span data-stu-id="140b7-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="140b7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="140b7-110">EXAMPLES</span></span>

### <span data-ttu-id="140b7-111">Пример 1: Удаление связи между модулем Runbook и расписанием</span><span class="sxs-lookup"><span data-stu-id="140b7-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="140b7-112">Эта команда удаляет связь между модулем Runbook с именем Runbk01 и расписанием под названием Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="140b7-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="140b7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="140b7-113">PARAMETERS</span></span>

### <span data-ttu-id="140b7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="140b7-114">-AutomationAccountName</span></span>
<span data-ttu-id="140b7-115">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="140b7-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="140b7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="140b7-116">-Force</span></span>
<span data-ttu-id="140b7-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="140b7-117">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-118">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="140b7-118">-JobScheduleId</span></span>
<span data-ttu-id="140b7-119">Указывает идентификатор запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="140b7-119">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140b7-120">-ResourceGroupName</span></span>
<span data-ttu-id="140b7-121">Указывает имя группы ресурсов для запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="140b7-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="140b7-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="140b7-122">-RunbookName</span></span>
<span data-ttu-id="140b7-123">Указывает имя Runbook, который отменяет этот командлет из расписания.</span><span class="sxs-lookup"><span data-stu-id="140b7-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="140b7-124">-ScheduleName</span></span>
<span data-ttu-id="140b7-125">Указывает имя расписания, из которого этот командлет не отменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="140b7-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="140b7-126">-Confirm</span></span>
<span data-ttu-id="140b7-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="140b7-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="140b7-128">-WhatIf</span></span>
<span data-ttu-id="140b7-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="140b7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="140b7-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="140b7-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140b7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140b7-131">-DefaultProfile</span></span>
<span data-ttu-id="140b7-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="140b7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="140b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140b7-133">CommonParameters</span></span>
<span data-ttu-id="140b7-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="140b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140b7-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="140b7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140b7-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="140b7-136">INPUTS</span></span>

## <span data-ttu-id="140b7-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="140b7-137">OUTPUTS</span></span>

## <span data-ttu-id="140b7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="140b7-138">NOTES</span></span>

## <span data-ttu-id="140b7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="140b7-139">RELATED LINKS</span></span>

[<span data-ttu-id="140b7-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="140b7-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="140b7-141">Регистрация — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="140b7-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


