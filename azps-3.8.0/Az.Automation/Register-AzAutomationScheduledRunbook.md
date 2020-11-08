---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 132726601b429819fa0d90186fd0d6448719df70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074946"
---
# <span data-ttu-id="55fcd-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="55fcd-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="55fcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="55fcd-103">Связывание модуля Runbook с расписанием.</span><span class="sxs-lookup"><span data-stu-id="55fcd-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="55fcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55fcd-104">SYNTAX</span></span>

### <span data-ttu-id="55fcd-105">ByRunbookName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55fcd-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55fcd-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="55fcd-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55fcd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55fcd-107">DESCRIPTION</span></span>
<span data-ttu-id="55fcd-108">Командлет **Register-AzAutomationScheduledRunbook** связывает Runbook службы автоматизации Azure с расписанием.</span><span class="sxs-lookup"><span data-stu-id="55fcd-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="55fcd-109">Модуль Runbook запускается в соответствии с расписанием, указанным с помощью параметра *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="55fcd-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="55fcd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55fcd-110">EXAMPLES</span></span>

### <span data-ttu-id="55fcd-111">Пример 1: связывание модуля Runbook с расписанием</span><span class="sxs-lookup"><span data-stu-id="55fcd-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="55fcd-112">Эта команда связывает Runbook с именем Runbk01 с расписанием с именем Sched01 в учетной записи службы автоматизации Azure под названием Contoso17.</span><span class="sxs-lookup"><span data-stu-id="55fcd-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="55fcd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55fcd-113">PARAMETERS</span></span>

### <span data-ttu-id="55fcd-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55fcd-114">-AutomationAccountName</span></span>
<span data-ttu-id="55fcd-115">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="55fcd-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="55fcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fcd-116">-DefaultProfile</span></span>
<span data-ttu-id="55fcd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55fcd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55fcd-118">-Parameters</span><span class="sxs-lookup"><span data-stu-id="55fcd-118">-Parameters</span></span>
<span data-ttu-id="55fcd-119">Указывает хэш-таблицу для пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="55fcd-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="55fcd-120">Ключи представляют собой имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="55fcd-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="55fcd-121">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="55fcd-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="55fcd-122">При запуске модуля Runbook в ответ на связанное расписание эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="55fcd-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="55fcd-124">Указывает имя группы ресурсов для запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="55fcd-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="55fcd-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="55fcd-125">-RunbookName</span></span>
<span data-ttu-id="55fcd-126">Указывает имя Runbook, который этот командлет связывает с расписанием.</span><span class="sxs-lookup"><span data-stu-id="55fcd-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="55fcd-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="55fcd-127">-RunOn</span></span>
<span data-ttu-id="55fcd-128">Имя группы гибридной рабочей роли Runbook.</span><span class="sxs-lookup"><span data-stu-id="55fcd-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fcd-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="55fcd-129">-ScheduleName</span></span>
<span data-ttu-id="55fcd-130">Указывает имя расписания, в которое этот командлет связывается с модулем Runbook.</span><span class="sxs-lookup"><span data-stu-id="55fcd-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="55fcd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fcd-131">CommonParameters</span></span>
<span data-ttu-id="55fcd-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55fcd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fcd-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55fcd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fcd-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55fcd-134">INPUTS</span></span>

### <span data-ttu-id="55fcd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="55fcd-135">System.String</span></span>

## <span data-ttu-id="55fcd-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55fcd-136">OUTPUTS</span></span>

### <span data-ttu-id="55fcd-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="55fcd-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="55fcd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="55fcd-138">NOTES</span></span>

## <span data-ttu-id="55fcd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55fcd-139">RELATED LINKS</span></span>

[<span data-ttu-id="55fcd-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="55fcd-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="55fcd-141">Отмена регистрации — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="55fcd-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


