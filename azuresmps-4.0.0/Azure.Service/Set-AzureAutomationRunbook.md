---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076072"
---
# <span data-ttu-id="49b28-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49b28-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="49b28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49b28-102">SYNOPSIS</span></span>

<span data-ttu-id="49b28-103">Изменяет конфигурацию модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="49b28-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="49b28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49b28-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="49b28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49b28-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="49b28-106">Командлет **Set-AzureAutomationRunbook** изменяет конфигурацию Runbook Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="49b28-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="49b28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49b28-107">EXAMPLES</span></span>

### <span data-ttu-id="49b28-108">Пример 1: включение подробного ведения журнала для модуля Runbook</span><span class="sxs-lookup"><span data-stu-id="49b28-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="49b28-109">Эта команда включает подробный журнал для заданий указанного Runbook в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="49b28-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="49b28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49b28-110">PARAMETERS</span></span>

### <span data-ttu-id="49b28-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49b28-111">-AutomationAccountName</span></span>
<span data-ttu-id="49b28-112">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="49b28-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="49b28-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="49b28-113">-Description</span></span>
<span data-ttu-id="49b28-114">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="49b28-114">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b28-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="49b28-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b28-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="49b28-116">-LogVerbose</span></span>
<span data-ttu-id="49b28-117">Указывает, следует ли использовать подробный журнал.</span><span class="sxs-lookup"><span data-stu-id="49b28-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b28-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49b28-118">-Name</span></span>
<span data-ttu-id="49b28-119">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="49b28-119">Specifies a name.</span></span>

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

### <span data-ttu-id="49b28-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="49b28-120">-Profile</span></span>
<span data-ttu-id="49b28-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="49b28-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49b28-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49b28-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49b28-123">-Теги</span><span class="sxs-lookup"><span data-stu-id="49b28-123">-Tags</span></span>
<span data-ttu-id="49b28-124">Задает массив тегов.</span><span class="sxs-lookup"><span data-stu-id="49b28-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49b28-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b28-125">CommonParameters</span></span>
<span data-ttu-id="49b28-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49b28-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b28-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b28-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b28-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49b28-128">INPUTS</span></span>

## <span data-ttu-id="49b28-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49b28-129">OUTPUTS</span></span>

### <span data-ttu-id="49b28-130">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="49b28-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="49b28-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="49b28-131">NOTES</span></span>

## <span data-ttu-id="49b28-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49b28-132">RELATED LINKS</span></span>

[<span data-ttu-id="49b28-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49b28-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="49b28-134">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49b28-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="49b28-135">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49b28-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="49b28-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49b28-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="49b28-137">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49b28-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


