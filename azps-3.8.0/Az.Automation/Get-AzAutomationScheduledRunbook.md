---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072667"
---
# <span data-ttu-id="f8955-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f8955-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="f8955-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8955-102">SYNOPSIS</span></span>
<span data-ttu-id="f8955-103">Возвращает Runbook Automation и связанные расписания.</span><span class="sxs-lookup"><span data-stu-id="f8955-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="f8955-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8955-104">SYNTAX</span></span>

### <span data-ttu-id="f8955-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8955-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8955-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="f8955-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8955-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="f8955-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8955-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="f8955-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8955-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="f8955-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8955-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8955-110">DESCRIPTION</span></span>
<span data-ttu-id="f8955-111">Командлет **Get-AzAutomationScheduledRunbook** получает один или несколько Runbook автоматизации Azure и связанных с ними расписаний.</span><span class="sxs-lookup"><span data-stu-id="f8955-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="f8955-112">По умолчанию этот командлет получает все запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8955-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="f8955-113">Укажите имя Runbook или расписание или оба варианта для просмотра конкретных расписаний Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8955-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="f8955-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8955-114">EXAMPLES</span></span>

### <span data-ttu-id="f8955-115">Пример 1: получение всех запланированных Runbook</span><span class="sxs-lookup"><span data-stu-id="f8955-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8955-116">Эта команда получает все запланированные Runbook в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8955-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8955-117">Пример 2: получение всех расписаний, связанных с модулем Runbook</span><span class="sxs-lookup"><span data-stu-id="f8955-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="f8955-118">Эта команда получает все запланированные Runbook для модуля Runbook Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8955-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8955-119">Пример 3: получение всех модулей Runbook, связанных с расписанием</span><span class="sxs-lookup"><span data-stu-id="f8955-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="f8955-120">Эта команда получает все запланированные Runbook для Schedule01 расписания в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8955-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f8955-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8955-121">PARAMETERS</span></span>

### <span data-ttu-id="f8955-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8955-122">-AutomationAccountName</span></span>
<span data-ttu-id="f8955-123">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f8955-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f8955-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8955-124">-DefaultProfile</span></span>
<span data-ttu-id="f8955-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f8955-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8955-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="f8955-126">-JobScheduleId</span></span>
<span data-ttu-id="f8955-127">Указывает идентификатор запланированного задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f8955-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8955-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8955-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8955-129">Указывает имя группы ресурсов для запланированных Runbook, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f8955-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8955-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="f8955-130">-RunbookName</span></span>
<span data-ttu-id="f8955-131">Указывает имя Runbook, для которого этот командлет получает запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8955-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8955-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="f8955-132">-ScheduleName</span></span>
<span data-ttu-id="f8955-133">Указывает имя расписания, для которого этот командлет получает запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8955-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8955-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8955-134">CommonParameters</span></span>
<span data-ttu-id="f8955-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8955-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8955-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8955-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8955-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8955-137">INPUTS</span></span>

### <span data-ttu-id="f8955-138">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f8955-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f8955-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f8955-139">System.String</span></span>

## <span data-ttu-id="f8955-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8955-140">OUTPUTS</span></span>

### <span data-ttu-id="f8955-141">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="f8955-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="f8955-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8955-142">NOTES</span></span>

## <span data-ttu-id="f8955-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8955-143">RELATED LINKS</span></span>

[<span data-ttu-id="f8955-144">Регистрация — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f8955-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="f8955-145">Отмена регистрации — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f8955-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


