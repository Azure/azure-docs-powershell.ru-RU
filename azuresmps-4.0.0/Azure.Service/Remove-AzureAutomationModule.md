---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076481"
---
# <span data-ttu-id="1099a-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1099a-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="1099a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1099a-102">SYNOPSIS</span></span>

<span data-ttu-id="1099a-103">Удаляет модуль из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1099a-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="1099a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1099a-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1099a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1099a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1099a-106">Командлет **Remove-AzureAutomationModule** удаляет учетную запись автоматизации из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1099a-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1099a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1099a-107">EXAMPLES</span></span>

### <span data-ttu-id="1099a-108">Пример 1: Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="1099a-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="1099a-109">Эта команда удаляет модуль с именем ContosoModule из учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1099a-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1099a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1099a-110">PARAMETERS</span></span>

### <span data-ttu-id="1099a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1099a-111">-AutomationAccountName</span></span>
<span data-ttu-id="1099a-112">Указывает имя учетной записи автоматизации для модуля.</span><span class="sxs-lookup"><span data-stu-id="1099a-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="1099a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1099a-113">-Force</span></span>
<span data-ttu-id="1099a-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1099a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1099a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1099a-115">-Name</span></span>
<span data-ttu-id="1099a-116">Указывает имя удаляемого модуля.</span><span class="sxs-lookup"><span data-stu-id="1099a-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="1099a-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="1099a-117">-Profile</span></span>
<span data-ttu-id="1099a-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1099a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1099a-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1099a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1099a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1099a-120">CommonParameters</span></span>
<span data-ttu-id="1099a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1099a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1099a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1099a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1099a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1099a-123">INPUTS</span></span>

## <span data-ttu-id="1099a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1099a-124">OUTPUTS</span></span>

## <span data-ttu-id="1099a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1099a-125">NOTES</span></span>

## <span data-ttu-id="1099a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1099a-126">RELATED LINKS</span></span>

[<span data-ttu-id="1099a-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1099a-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="1099a-128">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1099a-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="1099a-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1099a-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


