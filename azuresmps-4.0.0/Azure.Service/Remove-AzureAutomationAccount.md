---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076495"
---
# <span data-ttu-id="e24e6-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e24e6-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="e24e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e24e6-102">SYNOPSIS</span></span>

<span data-ttu-id="e24e6-103">Удаление учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e24e6-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="e24e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e24e6-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e24e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e24e6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e24e6-106">Командлет **Remove-AzureAutomationAccount** удаляет учетную запись из службы автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e24e6-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e24e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e24e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e24e6-108">Пример 1: Удаление учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="e24e6-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="e24e6-109">Эта команда удаляет учетную запись автоматизации с именем MyAutomationAccount без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e24e6-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="e24e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e24e6-110">PARAMETERS</span></span>

### <span data-ttu-id="e24e6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e24e6-111">-Force</span></span>
<span data-ttu-id="e24e6-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e24e6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e24e6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e24e6-113">-Name</span></span>
<span data-ttu-id="e24e6-114">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e24e6-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e6-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e24e6-115">-Profile</span></span>
<span data-ttu-id="e24e6-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e24e6-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e24e6-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e24e6-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e24e6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24e6-118">CommonParameters</span></span>
<span data-ttu-id="e24e6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e24e6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24e6-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e24e6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24e6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e24e6-121">INPUTS</span></span>

## <span data-ttu-id="e24e6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e24e6-122">OUTPUTS</span></span>

## <span data-ttu-id="e24e6-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e24e6-123">NOTES</span></span>

## <span data-ttu-id="e24e6-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e24e6-124">RELATED LINKS</span></span>

[<span data-ttu-id="e24e6-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e24e6-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="e24e6-126">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e24e6-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


