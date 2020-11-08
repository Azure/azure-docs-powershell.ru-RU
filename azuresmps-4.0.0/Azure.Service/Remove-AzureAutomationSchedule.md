---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076170"
---
# <span data-ttu-id="ef44d-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef44d-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="ef44d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef44d-102">SYNOPSIS</span></span>

<span data-ttu-id="ef44d-103">Удаляет расписание службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44d-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="ef44d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef44d-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef44d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef44d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ef44d-106">Командлет **Remove-AzureAutomationSchedule** Удаляет расписание из Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ef44d-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="ef44d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef44d-107">EXAMPLES</span></span>

### <span data-ttu-id="ef44d-108">Пример 1: Удаление расписания</span><span class="sxs-lookup"><span data-stu-id="ef44d-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="ef44d-109">Эта команда удаляет расписание с именем MySchedule.</span><span class="sxs-lookup"><span data-stu-id="ef44d-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="ef44d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef44d-110">PARAMETERS</span></span>

### <span data-ttu-id="ef44d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef44d-111">-AutomationAccountName</span></span>
<span data-ttu-id="ef44d-112">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ef44d-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="ef44d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ef44d-113">-Force</span></span>
<span data-ttu-id="ef44d-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef44d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef44d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef44d-115">-Name</span></span>
<span data-ttu-id="ef44d-116">Указывает имя расписания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ef44d-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="ef44d-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef44d-117">-Profile</span></span>
<span data-ttu-id="ef44d-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ef44d-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef44d-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef44d-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef44d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef44d-120">-Confirm</span></span>
<span data-ttu-id="ef44d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef44d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef44d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef44d-122">-WhatIf</span></span>
<span data-ttu-id="ef44d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef44d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef44d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef44d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef44d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef44d-125">CommonParameters</span></span>
<span data-ttu-id="ef44d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef44d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef44d-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef44d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef44d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef44d-128">INPUTS</span></span>

## <span data-ttu-id="ef44d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef44d-129">OUTPUTS</span></span>

## <span data-ttu-id="ef44d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef44d-130">NOTES</span></span>

## <span data-ttu-id="ef44d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef44d-131">RELATED LINKS</span></span>

[<span data-ttu-id="ef44d-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef44d-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="ef44d-133">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef44d-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="ef44d-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ef44d-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


