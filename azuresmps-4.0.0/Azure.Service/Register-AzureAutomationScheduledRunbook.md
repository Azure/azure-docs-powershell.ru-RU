---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075873"
---
# <span data-ttu-id="52304-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="52304-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="52304-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52304-102">SYNOPSIS</span></span>

<span data-ttu-id="52304-103">Связывание модуля Runbook с расписанием.</span><span class="sxs-lookup"><span data-stu-id="52304-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="52304-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52304-104">SYNTAX</span></span>

### <span data-ttu-id="52304-105">ByRunbookName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52304-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="52304-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="52304-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52304-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52304-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="52304-108">Командлет **Register-AzureAutomationScheduledRunbook** связывает Runbook с расписанием.</span><span class="sxs-lookup"><span data-stu-id="52304-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="52304-109">Модуль Runbook запускается в соответствии с расписанием, указанным с помощью параметра *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="52304-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="52304-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52304-110">EXAMPLES</span></span>

### <span data-ttu-id="52304-111">Пример 1: связывание модуля Runbook с расписанием</span><span class="sxs-lookup"><span data-stu-id="52304-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="52304-112">Эта команда связывает Runbook с именем Runbk01 с расписанием с именем Sched01 в учетной записи службы автоматизации Azure под названием Contoso17.</span><span class="sxs-lookup"><span data-stu-id="52304-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="52304-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52304-113">PARAMETERS</span></span>

### <span data-ttu-id="52304-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="52304-114">-AutomationAccountName</span></span>
<span data-ttu-id="52304-115">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="52304-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="52304-116">-Parameters</span><span class="sxs-lookup"><span data-stu-id="52304-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52304-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="52304-117">-Profile</span></span>
<span data-ttu-id="52304-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="52304-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52304-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52304-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52304-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="52304-120">-RunbookName</span></span>
<span data-ttu-id="52304-121">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="52304-121">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="52304-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="52304-122">-ScheduleName</span></span>
<span data-ttu-id="52304-123">Указывает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="52304-123">Specifies the name of the schedule.</span></span>

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

### <span data-ttu-id="52304-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52304-124">CommonParameters</span></span>
<span data-ttu-id="52304-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52304-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52304-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52304-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52304-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52304-127">INPUTS</span></span>

## <span data-ttu-id="52304-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52304-128">OUTPUTS</span></span>

### <span data-ttu-id="52304-129">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="52304-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="52304-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="52304-130">NOTES</span></span>

## <span data-ttu-id="52304-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52304-131">RELATED LINKS</span></span>

[<span data-ttu-id="52304-132">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="52304-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="52304-133">Отмена регистрации — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="52304-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


