---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076171"
---
# <span data-ttu-id="7bf74-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="7bf74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bf74-102">SYNOPSIS</span></span>

<span data-ttu-id="7bf74-103">Удаление модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="7bf74-103">Removes a runbook.</span></span>

## <span data-ttu-id="7bf74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bf74-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bf74-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7bf74-106">Командлет **Remove-AzureAutomationRunbook** удаляет Runbook из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf74-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7bf74-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bf74-107">EXAMPLES</span></span>

### <span data-ttu-id="7bf74-108">Пример 1: удаление Runbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="7bf74-109">Эта команда удаляет Runbook с именем MyRunbook в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7bf74-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7bf74-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bf74-110">PARAMETERS</span></span>

### <span data-ttu-id="7bf74-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7bf74-111">-AutomationAccountName</span></span>
<span data-ttu-id="7bf74-112">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7bf74-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="7bf74-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7bf74-113">-Force</span></span>
<span data-ttu-id="7bf74-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7bf74-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7bf74-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7bf74-115">-Name</span></span>
<span data-ttu-id="7bf74-116">Указывает имя модуля Runbook, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7bf74-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf74-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="7bf74-117">-Profile</span></span>
<span data-ttu-id="7bf74-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7bf74-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7bf74-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bf74-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7bf74-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bf74-120">-Confirm</span></span>
<span data-ttu-id="7bf74-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7bf74-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf74-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf74-122">-WhatIf</span></span>
<span data-ttu-id="7bf74-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7bf74-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bf74-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7bf74-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf74-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf74-125">CommonParameters</span></span>
<span data-ttu-id="7bf74-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bf74-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf74-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bf74-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf74-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bf74-128">INPUTS</span></span>

## <span data-ttu-id="7bf74-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bf74-129">OUTPUTS</span></span>

## <span data-ttu-id="7bf74-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bf74-130">NOTES</span></span>

## <span data-ttu-id="7bf74-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bf74-131">RELATED LINKS</span></span>

[<span data-ttu-id="7bf74-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="7bf74-133">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="7bf74-134">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="7bf74-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="7bf74-136">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bf74-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


