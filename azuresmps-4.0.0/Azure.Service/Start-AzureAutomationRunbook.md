---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076032"
---
# <span data-ttu-id="e84d5-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="e84d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e84d5-102">SYNOPSIS</span></span>

<span data-ttu-id="e84d5-103">Запускает задание Runbook.</span><span class="sxs-lookup"><span data-stu-id="e84d5-103">Starts a runbook job.</span></span>

## <span data-ttu-id="e84d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e84d5-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e84d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e84d5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e84d5-106">Командлет **Start-AzureAutomationRunbook** запускает задание Microsoft Azure Automation Runbook.</span><span class="sxs-lookup"><span data-stu-id="e84d5-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="e84d5-107">Укажите идентификатор или имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="e84d5-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="e84d5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e84d5-108">EXAMPLES</span></span>

### <span data-ttu-id="e84d5-109">Пример 1: запуск задания Runbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="e84d5-110">Эта команда запускает задание Runbook для модуля Runbook с именем Runbk01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e84d5-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e84d5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e84d5-111">PARAMETERS</span></span>

### <span data-ttu-id="e84d5-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e84d5-112">-AutomationAccountName</span></span>
<span data-ttu-id="e84d5-113">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e84d5-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="e84d5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e84d5-114">-Name</span></span>
<span data-ttu-id="e84d5-115">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="e84d5-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="e84d5-116">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e84d5-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e84d5-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e84d5-117">-Profile</span></span>
<span data-ttu-id="e84d5-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e84d5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e84d5-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e84d5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e84d5-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e84d5-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e84d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84d5-121">CommonParameters</span></span>
<span data-ttu-id="e84d5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e84d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84d5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e84d5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84d5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e84d5-124">INPUTS</span></span>

## <span data-ttu-id="e84d5-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e84d5-125">OUTPUTS</span></span>

### <span data-ttu-id="e84d5-126">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="e84d5-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="e84d5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e84d5-127">NOTES</span></span>

## <span data-ttu-id="e84d5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e84d5-128">RELATED LINKS</span></span>

[<span data-ttu-id="e84d5-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="e84d5-130">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="e84d5-131">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="e84d5-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="e84d5-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e84d5-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


