---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075885"
---
# <span data-ttu-id="d37ae-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="d37ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d37ae-102">SYNOPSIS</span></span>

<span data-ttu-id="d37ae-103">Публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="d37ae-103">Publishes a runbook.</span></span>

## <span data-ttu-id="d37ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d37ae-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d37ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d37ae-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d37ae-106">Командлет **Publish-AzureAutomationRunbook** публикует Runbook для использования в рабочей среде автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d37ae-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d37ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d37ae-107">EXAMPLES</span></span>

### <span data-ttu-id="d37ae-108">Пример 1: публикация Runbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="d37ae-109">Эта команда публикует Runbook с именем Runbk01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d37ae-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d37ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d37ae-110">PARAMETERS</span></span>

### <span data-ttu-id="d37ae-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d37ae-111">-AutomationAccountName</span></span>
<span data-ttu-id="d37ae-112">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d37ae-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="d37ae-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d37ae-113">-Name</span></span>
<span data-ttu-id="d37ae-114">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="d37ae-114">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="d37ae-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="d37ae-115">-Profile</span></span>
<span data-ttu-id="d37ae-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d37ae-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d37ae-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d37ae-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d37ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37ae-118">CommonParameters</span></span>
<span data-ttu-id="d37ae-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d37ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37ae-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37ae-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37ae-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d37ae-121">INPUTS</span></span>

## <span data-ttu-id="d37ae-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d37ae-122">OUTPUTS</span></span>

## <span data-ttu-id="d37ae-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="d37ae-123">NOTES</span></span>

## <span data-ttu-id="d37ae-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d37ae-124">RELATED LINKS</span></span>

[<span data-ttu-id="d37ae-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="d37ae-126">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="d37ae-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="d37ae-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="d37ae-129">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d37ae-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


