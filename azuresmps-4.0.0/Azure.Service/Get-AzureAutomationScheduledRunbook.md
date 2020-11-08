---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076357"
---
# <span data-ttu-id="29872-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="29872-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="29872-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29872-102">SYNOPSIS</span></span>

<span data-ttu-id="29872-103">Возвращает Runbook службы автоматизации Azure и связанные расписания.</span><span class="sxs-lookup"><span data-stu-id="29872-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="29872-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29872-104">SYNTAX</span></span>

### <span data-ttu-id="29872-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29872-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="29872-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="29872-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="29872-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="29872-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="29872-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="29872-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="29872-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="29872-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29872-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29872-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="29872-111">**Get-AzureAutomationScheduledRunbook** возвращает один или несколько Runbook Azure Automation и связанных с ними расписаний.</span><span class="sxs-lookup"><span data-stu-id="29872-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="29872-112">По умолчанию возвращаются все запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="29872-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="29872-113">Чтобы получить определенную запланированную Runbook, укажите имя Runbook и имя расписания.</span><span class="sxs-lookup"><span data-stu-id="29872-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="29872-114">Чтобы получить все расписания, связанные с модулем Runbook, укажите только имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="29872-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="29872-115">Чтобы получить все модули Runbook, связанные с расписанием, укажите только имя расписания.</span><span class="sxs-lookup"><span data-stu-id="29872-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="29872-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29872-116">EXAMPLES</span></span>

### <span data-ttu-id="29872-117">Пример 1: получение всех запланированных Runbook</span><span class="sxs-lookup"><span data-stu-id="29872-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="29872-118">Эта команда получает все запланированные Runbook в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="29872-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="29872-119">Пример 2: получение всех расписаний, связанных с модулем Runbook</span><span class="sxs-lookup"><span data-stu-id="29872-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="29872-120">Эта команда получает все запланированные Runbook для модуля Runbook Runbk01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="29872-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="29872-121">Пример 3: получение всех модулей Runbook, связанных с расписанием</span><span class="sxs-lookup"><span data-stu-id="29872-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="29872-122">Эта команда получает все запланированные Runbook для Schedule01 расписания в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="29872-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="29872-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29872-123">PARAMETERS</span></span>

### <span data-ttu-id="29872-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29872-124">-AutomationAccountName</span></span>
<span data-ttu-id="29872-125">Указывает имя учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="29872-125">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29872-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="29872-126">-JobScheduleId</span></span>
<span data-ttu-id="29872-127">Указывает идентификатор запланированного задания.</span><span class="sxs-lookup"><span data-stu-id="29872-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29872-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="29872-128">-Profile</span></span>
<span data-ttu-id="29872-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="29872-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29872-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="29872-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29872-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="29872-131">-RunbookName</span></span>
<span data-ttu-id="29872-132">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="29872-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29872-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="29872-133">-ScheduleName</span></span>
<span data-ttu-id="29872-134">Указывает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="29872-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29872-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29872-135">CommonParameters</span></span>
<span data-ttu-id="29872-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29872-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29872-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29872-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29872-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29872-138">INPUTS</span></span>

## <span data-ttu-id="29872-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29872-139">OUTPUTS</span></span>

### <span data-ttu-id="29872-140">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="29872-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="29872-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="29872-141">NOTES</span></span>

## <span data-ttu-id="29872-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29872-142">RELATED LINKS</span></span>

[<span data-ttu-id="29872-143">Регистрация — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="29872-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="29872-144">Отмена регистрации — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="29872-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


