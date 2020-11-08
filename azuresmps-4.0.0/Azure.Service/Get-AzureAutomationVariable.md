---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075653"
---
# <span data-ttu-id="4227a-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4227a-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="4227a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4227a-102">SYNOPSIS</span></span>

<span data-ttu-id="4227a-103">Возвращает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4227a-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="4227a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4227a-104">SYNTAX</span></span>

### <span data-ttu-id="4227a-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4227a-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4227a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4227a-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4227a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4227a-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4227a-108">Командлет **Get-AzureAutomationVariable** получает одну или несколько переменных автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4227a-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="4227a-109">По умолчанию возвращаются все переменные.</span><span class="sxs-lookup"><span data-stu-id="4227a-109">By default, all variables are returned.</span></span>
<span data-ttu-id="4227a-110">Чтобы получить определенную переменную, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="4227a-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="4227a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4227a-111">EXAMPLES</span></span>

### <span data-ttu-id="4227a-112">Пример 1: получение переменной</span><span class="sxs-lookup"><span data-stu-id="4227a-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="4227a-113">Эти команды получают переменную автоматизации с именем MyVariable и присвойте ей значение переменной с именем $value.</span><span class="sxs-lookup"><span data-stu-id="4227a-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="4227a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4227a-114">PARAMETERS</span></span>

### <span data-ttu-id="4227a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4227a-115">-AutomationAccountName</span></span>
<span data-ttu-id="4227a-116">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4227a-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="4227a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4227a-117">-Name</span></span>
<span data-ttu-id="4227a-118">Указывает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="4227a-118">Specifies the name of a variable.</span></span>

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

### <span data-ttu-id="4227a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="4227a-119">-Profile</span></span>
<span data-ttu-id="4227a-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4227a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4227a-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4227a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4227a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4227a-122">CommonParameters</span></span>
<span data-ttu-id="4227a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4227a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4227a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4227a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4227a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4227a-125">INPUTS</span></span>

## <span data-ttu-id="4227a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4227a-126">OUTPUTS</span></span>

### <span data-ttu-id="4227a-127">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="4227a-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="4227a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="4227a-128">NOTES</span></span>

## <span data-ttu-id="4227a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4227a-129">RELATED LINKS</span></span>

[<span data-ttu-id="4227a-130">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4227a-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="4227a-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4227a-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="4227a-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4227a-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


