---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075657"
---
# <span data-ttu-id="9e972-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e972-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="9e972-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e972-102">SYNOPSIS</span></span>

<span data-ttu-id="9e972-103">Получает Runbook.</span><span class="sxs-lookup"><span data-stu-id="9e972-103">Gets a runbook.</span></span>

## <span data-ttu-id="9e972-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e972-104">SYNTAX</span></span>

### <span data-ttu-id="9e972-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e972-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9e972-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="9e972-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e972-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e972-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9e972-108">Командлет **Get-AzureAutomationRunbook** получает один или несколько модулей Runbook Automation для Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e972-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="9e972-109">По умолчанию возвращаются все модули Runbook.</span><span class="sxs-lookup"><span data-stu-id="9e972-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="9e972-110">Чтобы получить определенный Runbook, укажите его имя или идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9e972-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="9e972-111">Чтобы получить доступ ко всем модулям Runbook, связанным с определенным расписанием, укажите имя расписания.</span><span class="sxs-lookup"><span data-stu-id="9e972-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="9e972-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e972-112">EXAMPLES</span></span>

### <span data-ttu-id="9e972-113">Пример 1: получение всех модулей Runbook</span><span class="sxs-lookup"><span data-stu-id="9e972-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9e972-114">Эта команда получает все runbooks в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9e972-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9e972-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e972-115">PARAMETERS</span></span>

### <span data-ttu-id="9e972-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e972-116">-AutomationAccountName</span></span>
<span data-ttu-id="9e972-117">Указывает имя учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="9e972-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="9e972-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e972-118">-Name</span></span>
<span data-ttu-id="9e972-119">Указывает имя Runbook.</span><span class="sxs-lookup"><span data-stu-id="9e972-119">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="9e972-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="9e972-120">-Profile</span></span>
<span data-ttu-id="9e972-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9e972-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e972-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e972-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e972-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e972-123">CommonParameters</span></span>
<span data-ttu-id="9e972-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e972-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e972-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e972-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e972-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e972-126">INPUTS</span></span>

## <span data-ttu-id="9e972-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e972-127">OUTPUTS</span></span>

### <span data-ttu-id="9e972-128">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="9e972-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9e972-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e972-129">NOTES</span></span>

## <span data-ttu-id="9e972-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e972-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e972-131">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e972-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="9e972-132">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e972-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="9e972-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e972-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="9e972-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e972-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="9e972-135">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e972-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


