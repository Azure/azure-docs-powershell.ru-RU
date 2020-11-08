---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076587"
---
# <span data-ttu-id="c05c9-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c05c9-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="c05c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c05c9-102">SYNOPSIS</span></span>

<span data-ttu-id="c05c9-103">Удаляет связь между модулем Runbook и расписанием.</span><span class="sxs-lookup"><span data-stu-id="c05c9-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="c05c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c05c9-104">SYNTAX</span></span>

### <span data-ttu-id="c05c9-105">ByJobScheduleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c05c9-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c05c9-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="c05c9-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c05c9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c05c9-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c05c9-108">Командлет **Unregister-AzureAutomationScheduledRunbook** удаляет связь между модулем автоматизации Microsoft Azure Automation Runbook и расписанием, что приводит к остановке запуска модуля Runbook при срабатывании расписания.</span><span class="sxs-lookup"><span data-stu-id="c05c9-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="c05c9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c05c9-109">EXAMPLES</span></span>

### <span data-ttu-id="c05c9-110">Пример 1: Удаление связи между модулем Runbook и расписанием</span><span class="sxs-lookup"><span data-stu-id="c05c9-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="c05c9-111">Эта команда удаляет связь между модулем Runbook с именем Runbk01 и расписанием под названием Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="c05c9-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="c05c9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c05c9-112">PARAMETERS</span></span>

### <span data-ttu-id="c05c9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c05c9-113">-AutomationAccountName</span></span>
<span data-ttu-id="c05c9-114">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c05c9-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c05c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c05c9-115">-Force</span></span>
<span data-ttu-id="c05c9-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c05c9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c05c9-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c05c9-117">-JobScheduleId</span></span>
<span data-ttu-id="c05c9-118">Указывает идентификатор запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="c05c9-118">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="c05c9-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="c05c9-119">-Profile</span></span>
<span data-ttu-id="c05c9-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c05c9-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c05c9-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c05c9-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c05c9-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c05c9-122">-RunbookName</span></span>
<span data-ttu-id="c05c9-123">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="c05c9-123">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05c9-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="c05c9-124">-ScheduleName</span></span>
<span data-ttu-id="c05c9-125">Указывает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="c05c9-125">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05c9-126">CommonParameters</span></span>
<span data-ttu-id="c05c9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c05c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05c9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05c9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c05c9-129">INPUTS</span></span>

## <span data-ttu-id="c05c9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c05c9-130">OUTPUTS</span></span>

## <span data-ttu-id="c05c9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c05c9-131">NOTES</span></span>

## <span data-ttu-id="c05c9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c05c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="c05c9-133">Регистрация — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c05c9-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


