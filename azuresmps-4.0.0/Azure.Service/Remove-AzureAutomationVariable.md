---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076169"
---
# <span data-ttu-id="e6882-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6882-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="e6882-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6882-102">SYNOPSIS</span></span>

<span data-ttu-id="e6882-103">Удаляет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e6882-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="e6882-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6882-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6882-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6882-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e6882-106">Командлет **Remove-AzureAutomationVariable** удаляет переменную из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e6882-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e6882-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6882-107">EXAMPLES</span></span>

### <span data-ttu-id="e6882-108">Пример 1: Удаление переменной</span><span class="sxs-lookup"><span data-stu-id="e6882-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="e6882-109">Эта команда удаляет переменную с именем MyStringVariable в учетной записи автоматизации с именем Contoso17 без запроса на проверку пользователей.</span><span class="sxs-lookup"><span data-stu-id="e6882-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="e6882-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6882-110">PARAMETERS</span></span>

### <span data-ttu-id="e6882-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6882-111">-AutomationAccountName</span></span>
<span data-ttu-id="e6882-112">Указывает имя учетной записи автоматизации с переменной.</span><span class="sxs-lookup"><span data-stu-id="e6882-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="e6882-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e6882-113">-Force</span></span>
<span data-ttu-id="e6882-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6882-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6882-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6882-115">-Name</span></span>
<span data-ttu-id="e6882-116">Указывает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="e6882-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="e6882-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6882-117">-Profile</span></span>
<span data-ttu-id="e6882-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e6882-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6882-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6882-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6882-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6882-120">CommonParameters</span></span>
<span data-ttu-id="e6882-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6882-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6882-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6882-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6882-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6882-123">INPUTS</span></span>

## <span data-ttu-id="e6882-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6882-124">OUTPUTS</span></span>

## <span data-ttu-id="e6882-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6882-125">NOTES</span></span>

## <span data-ttu-id="e6882-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6882-126">RELATED LINKS</span></span>

[<span data-ttu-id="e6882-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6882-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="e6882-128">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6882-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="e6882-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6882-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


