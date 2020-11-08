---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075934"
---
# <span data-ttu-id="c484a-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c484a-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="c484a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c484a-102">SYNOPSIS</span></span>

<span data-ttu-id="c484a-103">Создание Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-103">Creates a runbook.</span></span>

## <span data-ttu-id="c484a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c484a-104">SYNTAX</span></span>

### <span data-ttu-id="c484a-105">ByRunbookName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c484a-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c484a-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="c484a-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c484a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c484a-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c484a-108">Командлет **New-AzureAutomationRunbook** создает новый пустой Runbook Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c484a-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="c484a-109">Укажите имя для создания нового Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="c484a-110">Вы также можете указать путь к файлу сценария Windows PowerShell (PS1), чтобы импортировать Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="c484a-111">Сценарий, который нужно импортировать, должен содержать одно определение рабочего процесса Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c484a-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="c484a-112">Имя этого рабочего процесса Windows PowerShell становится именем Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="c484a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c484a-113">EXAMPLES</span></span>

### <span data-ttu-id="c484a-114">Пример 1: создание Runbook</span><span class="sxs-lookup"><span data-stu-id="c484a-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="c484a-115">Эта команда создает новый Runbook с именем Runbook02 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c484a-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c484a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c484a-116">PARAMETERS</span></span>

### <span data-ttu-id="c484a-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c484a-117">-AutomationAccountName</span></span>
<span data-ttu-id="c484a-118">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c484a-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="c484a-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="c484a-119">-Description</span></span>
<span data-ttu-id="c484a-120">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="c484a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c484a-121">-Name</span></span>
<span data-ttu-id="c484a-122">Задает имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c484a-123">-Path</span><span class="sxs-lookup"><span data-stu-id="c484a-123">-Path</span></span>
<span data-ttu-id="c484a-124">Указывает путь.</span><span class="sxs-lookup"><span data-stu-id="c484a-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c484a-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="c484a-125">-Profile</span></span>
<span data-ttu-id="c484a-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c484a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c484a-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c484a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c484a-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="c484a-128">-Tags</span></span>
<span data-ttu-id="c484a-129">Указывает теги для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="c484a-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c484a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c484a-130">CommonParameters</span></span>
<span data-ttu-id="c484a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c484a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c484a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c484a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c484a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c484a-133">INPUTS</span></span>

## <span data-ttu-id="c484a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c484a-134">OUTPUTS</span></span>

### <span data-ttu-id="c484a-135">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="c484a-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="c484a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c484a-136">NOTES</span></span>

## <span data-ttu-id="c484a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c484a-137">RELATED LINKS</span></span>

[<span data-ttu-id="c484a-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c484a-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="c484a-139">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c484a-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="c484a-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c484a-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="c484a-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c484a-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="c484a-142">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c484a-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


