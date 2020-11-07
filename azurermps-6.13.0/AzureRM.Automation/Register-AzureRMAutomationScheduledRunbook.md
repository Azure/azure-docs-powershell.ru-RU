---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: deb6611fedbb1f88b9668b4750e096056ea8b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732807"
---
# <span data-ttu-id="2f81a-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2f81a-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="2f81a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f81a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f81a-103">Связывание модуля Runbook с расписанием.</span><span class="sxs-lookup"><span data-stu-id="2f81a-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f81a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f81a-104">SYNTAX</span></span>

### <span data-ttu-id="2f81a-105">ByRunbookName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f81a-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f81a-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="2f81a-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f81a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f81a-107">DESCRIPTION</span></span>
<span data-ttu-id="2f81a-108">Командлет **Register-AzureRmAutomationScheduledRunbook** связывает Runbook службы автоматизации Azure с расписанием.</span><span class="sxs-lookup"><span data-stu-id="2f81a-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="2f81a-109">Модуль Runbook запускается в соответствии с расписанием, указанным с помощью параметра *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="2f81a-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="2f81a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f81a-110">EXAMPLES</span></span>

### <span data-ttu-id="2f81a-111">Пример 1: связывание модуля Runbook с расписанием</span><span class="sxs-lookup"><span data-stu-id="2f81a-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2f81a-112">Эта команда связывает Runbook с именем Runbk01 с расписанием с именем Sched01 в учетной записи службы автоматизации Azure под названием Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2f81a-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2f81a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f81a-113">PARAMETERS</span></span>

### <span data-ttu-id="2f81a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2f81a-114">-AutomationAccountName</span></span>
<span data-ttu-id="2f81a-115">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2f81a-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2f81a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f81a-116">-DefaultProfile</span></span>
<span data-ttu-id="2f81a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f81a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f81a-118">-Parameters</span><span class="sxs-lookup"><span data-stu-id="2f81a-118">-Parameters</span></span>
<span data-ttu-id="2f81a-119">Указывает хэш-таблицу для пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="2f81a-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="2f81a-120">Ключи представляют собой имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="2f81a-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="2f81a-121">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="2f81a-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="2f81a-122">При запуске модуля Runbook в ответ на связанное расписание эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="2f81a-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="2f81a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f81a-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f81a-124">Указывает имя группы ресурсов для запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="2f81a-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="2f81a-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2f81a-125">-RunbookName</span></span>
<span data-ttu-id="2f81a-126">Указывает имя Runbook, который этот командлет связывает с расписанием.</span><span class="sxs-lookup"><span data-stu-id="2f81a-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="2f81a-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="2f81a-127">-RunOn</span></span>
<span data-ttu-id="2f81a-128">Имя группы гибридной рабочей роли Runbook.</span><span class="sxs-lookup"><span data-stu-id="2f81a-128">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="2f81a-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="2f81a-129">-ScheduleName</span></span>
<span data-ttu-id="2f81a-130">Указывает имя расписания, в которое этот командлет связывается с модулем Runbook.</span><span class="sxs-lookup"><span data-stu-id="2f81a-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="2f81a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f81a-131">CommonParameters</span></span>
<span data-ttu-id="2f81a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f81a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f81a-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f81a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f81a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f81a-134">INPUTS</span></span>

### <span data-ttu-id="2f81a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2f81a-135">System.String</span></span>

## <span data-ttu-id="2f81a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f81a-136">OUTPUTS</span></span>

### <span data-ttu-id="2f81a-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="2f81a-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="2f81a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f81a-138">NOTES</span></span>

## <span data-ttu-id="2f81a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f81a-139">RELATED LINKS</span></span>

[<span data-ttu-id="2f81a-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2f81a-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="2f81a-141">Отмена регистрации — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2f81a-141">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


