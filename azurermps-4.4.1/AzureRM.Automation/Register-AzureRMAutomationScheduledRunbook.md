---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: e58f3d429d036afa13f82e8e140ca8195eed612a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557951"
---
# <span data-ttu-id="df1b5-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="df1b5-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="df1b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="df1b5-103">Связывание модуля Runbook с расписанием.</span><span class="sxs-lookup"><span data-stu-id="df1b5-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df1b5-104">SYNTAX</span></span>

### <span data-ttu-id="df1b5-105">ByRunbookName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df1b5-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df1b5-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="df1b5-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df1b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df1b5-107">DESCRIPTION</span></span>
<span data-ttu-id="df1b5-108">Командлет **Register-AzureRmAutomationScheduledRunbook** связывает Runbook службы автоматизации Azure с расписанием.</span><span class="sxs-lookup"><span data-stu-id="df1b5-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="df1b5-109">Модуль Runbook запускается в соответствии с расписанием, указанным с помощью параметра *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="df1b5-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="df1b5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df1b5-110">EXAMPLES</span></span>

### <span data-ttu-id="df1b5-111">Пример 1: связывание модуля Runbook с расписанием</span><span class="sxs-lookup"><span data-stu-id="df1b5-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df1b5-112">Эта команда связывает Runbook с именем Runbk01 с расписанием с именем Sched01 в учетной записи службы автоматизации Azure под названием Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df1b5-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="df1b5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df1b5-113">PARAMETERS</span></span>

### <span data-ttu-id="df1b5-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df1b5-114">-AutomationAccountName</span></span>
<span data-ttu-id="df1b5-115">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="df1b5-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="df1b5-116">-Parameters</span><span class="sxs-lookup"><span data-stu-id="df1b5-116">-Parameters</span></span>
<span data-ttu-id="df1b5-117">Указывает хэш-таблицу для пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="df1b5-117">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="df1b5-118">Ключи представляют собой имена параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="df1b5-118">The keys are runbook parameter names.</span></span>
<span data-ttu-id="df1b5-119">Значения — это значения параметров Runbook.</span><span class="sxs-lookup"><span data-stu-id="df1b5-119">The values are runbook parameter values.</span></span>
<span data-ttu-id="df1b5-120">При запуске модуля Runbook в ответ на связанное расписание эти параметры передаются в модуль Runbook.</span><span class="sxs-lookup"><span data-stu-id="df1b5-120">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="df1b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="df1b5-122">Указывает имя группы ресурсов для запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="df1b5-122">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="df1b5-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="df1b5-123">-RunbookName</span></span>
<span data-ttu-id="df1b5-124">Указывает имя Runbook, который этот командлет связывает с расписанием.</span><span class="sxs-lookup"><span data-stu-id="df1b5-124">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="df1b5-125">-RunOn</span><span class="sxs-lookup"><span data-stu-id="df1b5-125">-RunOn</span></span>
<span data-ttu-id="df1b5-126">Имя группы гибридной рабочей роли Runbook.</span><span class="sxs-lookup"><span data-stu-id="df1b5-126">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="df1b5-127">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="df1b5-127">-ScheduleName</span></span>
<span data-ttu-id="df1b5-128">Указывает имя расписания, в которое этот командлет связывается с модулем Runbook.</span><span class="sxs-lookup"><span data-stu-id="df1b5-128">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="df1b5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1b5-129">-DefaultProfile</span></span>
<span data-ttu-id="df1b5-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df1b5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1b5-131">CommonParameters</span></span>
<span data-ttu-id="df1b5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df1b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1b5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1b5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1b5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df1b5-134">INPUTS</span></span>

## <span data-ttu-id="df1b5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df1b5-135">OUTPUTS</span></span>

### <span data-ttu-id="df1b5-136">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="df1b5-136">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="df1b5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="df1b5-137">NOTES</span></span>

## <span data-ttu-id="df1b5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df1b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="df1b5-139">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="df1b5-139">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="df1b5-140">Отмена регистрации — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="df1b5-140">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


