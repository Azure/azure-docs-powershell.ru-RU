---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959784"
---
# <span data-ttu-id="66759-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="66759-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="66759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66759-102">SYNOPSIS</span></span>
<span data-ttu-id="66759-103">Получить учетные записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-103">Get billing accounts.</span></span>

## <span data-ttu-id="66759-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="66759-104">SYNTAX</span></span>

### <span data-ttu-id="66759-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66759-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66759-106">Один</span><span class="sxs-lookup"><span data-stu-id="66759-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66759-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66759-107">DESCRIPTION</span></span>
<span data-ttu-id="66759-108">Для получения учетных записей вычетов и доступа к ним пользователю возвращается **cmdlet Get-AzBillingAccount.**</span><span class="sxs-lookup"><span data-stu-id="66759-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="66759-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="66759-109">EXAMPLES</span></span>

### <span data-ttu-id="66759-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66759-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="66759-111">Получить доступ ко всем учетным записям вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="66759-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="66759-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="66759-113">Получить учетную запись вы выставления счетов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="66759-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="66759-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="66759-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="66759-115">Получить доступ ко всем учетным записям вы выставления счетов и включить адрес в результат.</span><span class="sxs-lookup"><span data-stu-id="66759-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="66759-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="66759-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="66759-117">Получите все учетные записи вы выставления счетов, к которые у пользователя есть доступ, и включит профили вы выставления счетов в результат.</span><span class="sxs-lookup"><span data-stu-id="66759-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="66759-118">Пример 5</span><span class="sxs-lookup"><span data-stu-id="66759-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="66759-119">Получите все учетные записи выставления счетов, к которые у пользователя есть доступ, и включит в результат профили выставления счетов и разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="66759-120">Пример 6</span><span class="sxs-lookup"><span data-stu-id="66759-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="66759-121">Получите учетную запись выставления счетов с указанным именем, включив в результат адрес, профили выставления счетов и разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="66759-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66759-122">PARAMETERS</span></span>

### <span data-ttu-id="66759-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66759-123">-DefaultProfile</span></span>
<span data-ttu-id="66759-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="66759-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66759-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="66759-125">-IncludeAddress</span></span>
<span data-ttu-id="66759-126">Укаймь адрес учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-126">Include the address of the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66759-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="66759-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="66759-128">Включив профили вы выставления счетов в учетную запись вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-128">Include the billing profiles under the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66759-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="66759-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="66759-130">Включив в них профили выставления счетов в разделах учетной записи выставления счетов и счетах.</span><span class="sxs-lookup"><span data-stu-id="66759-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66759-131">-Name</span><span class="sxs-lookup"><span data-stu-id="66759-131">-Name</span></span>
<span data-ttu-id="66759-132">Имя определенной учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="66759-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66759-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="66759-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="66759-134">Перечислить объекты вы счета в учетной записи вы выставления счетов, которую можно использовать для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="66759-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66759-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66759-135">CommonParameters</span></span>
<span data-ttu-id="66759-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66759-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66759-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66759-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66759-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66759-138">INPUTS</span></span>

### <span data-ttu-id="66759-139">Нет</span><span class="sxs-lookup"><span data-stu-id="66759-139">None</span></span>

## <span data-ttu-id="66759-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66759-140">OUTPUTS</span></span>

### <span data-ttu-id="66759-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="66759-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="66759-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="66759-142">NOTES</span></span>

## <span data-ttu-id="66759-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66759-143">RELATED LINKS</span></span>
