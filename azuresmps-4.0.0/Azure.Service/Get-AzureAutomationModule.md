---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076368"
---
# <span data-ttu-id="4a976-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a976-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="4a976-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a976-102">SYNOPSIS</span></span>

<span data-ttu-id="4a976-103">Получение модуля автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4a976-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="4a976-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a976-104">SYNTAX</span></span>

### <span data-ttu-id="4a976-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a976-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4a976-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4a976-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a976-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a976-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4a976-108">Командлет **Get-AzureAutomationModule** получает один или несколько модулей автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a976-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="4a976-109">По умолчанию возвращаются все модули.</span><span class="sxs-lookup"><span data-stu-id="4a976-109">By default, all modules are returned.</span></span>
<span data-ttu-id="4a976-110">Чтобы получить определенный модуль, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="4a976-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="4a976-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a976-111">EXAMPLES</span></span>

### <span data-ttu-id="4a976-112">Пример 1: получение всех модулей</span><span class="sxs-lookup"><span data-stu-id="4a976-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4a976-113">Эта команда получает все модули в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4a976-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4a976-114">Пример 2: получение модуля</span><span class="sxs-lookup"><span data-stu-id="4a976-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="4a976-115">Эта команда получает модуль с именем ContosoModule в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4a976-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4a976-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a976-116">PARAMETERS</span></span>

### <span data-ttu-id="4a976-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a976-117">-AutomationAccountName</span></span>
<span data-ttu-id="4a976-118">Указывает имя учетной записи автоматизации, для которой требуется извлечь Runbook.</span><span class="sxs-lookup"><span data-stu-id="4a976-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="4a976-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a976-119">-Name</span></span>
<span data-ttu-id="4a976-120">Указывает имя извлекаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="4a976-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a976-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="4a976-121">-Profile</span></span>
<span data-ttu-id="4a976-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4a976-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a976-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a976-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a976-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a976-124">CommonParameters</span></span>
<span data-ttu-id="4a976-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a976-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a976-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a976-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a976-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a976-127">INPUTS</span></span>

## <span data-ttu-id="4a976-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a976-128">OUTPUTS</span></span>

### <span data-ttu-id="4a976-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="4a976-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="4a976-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a976-130">NOTES</span></span>

## <span data-ttu-id="4a976-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a976-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a976-132">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a976-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="4a976-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a976-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="4a976-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4a976-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


