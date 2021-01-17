---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405279"
---
# <span data-ttu-id="6c60c-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="6c60c-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="6c60c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c60c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c60c-103">Получить учетные записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-103">Get billing accounts.</span></span>

## <span data-ttu-id="6c60c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c60c-104">SYNTAX</span></span>

### <span data-ttu-id="6c60c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c60c-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c60c-106">Один</span><span class="sxs-lookup"><span data-stu-id="6c60c-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c60c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c60c-107">DESCRIPTION</span></span>
<span data-ttu-id="6c60c-108">Для получения учетных записей вычетов и доступа к ним у пользователя есть учетные записи **Get-AzBillingAccount.**</span><span class="sxs-lookup"><span data-stu-id="6c60c-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="6c60c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c60c-109">EXAMPLES</span></span>

### <span data-ttu-id="6c60c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c60c-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="6c60c-111">Получить доступ ко всем учетным записям вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="6c60c-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6c60c-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6c60c-113">Получить учетную запись вы выставления счетов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="6c60c-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="6c60c-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6c60c-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="6c60c-115">Получить доступ ко всем учетным записям вы выставления счетов и включить адрес в результат.</span><span class="sxs-lookup"><span data-stu-id="6c60c-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="6c60c-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6c60c-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="6c60c-117">Получите доступ ко всем учетным записям вы выставления счетов и включим в результат профили вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="6c60c-118">Пример 5</span><span class="sxs-lookup"><span data-stu-id="6c60c-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="6c60c-119">Получите все учетные записи выставления счетов, к которые у пользователя есть доступ, и включит в результат профили выставления счетов и разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="6c60c-120">Пример 6</span><span class="sxs-lookup"><span data-stu-id="6c60c-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6c60c-121">Получите учетную запись выставления счетов с указанным именем, включив в результат адрес, профили выставления счетов и разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="6c60c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c60c-122">PARAMETERS</span></span>

### <span data-ttu-id="6c60c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c60c-123">-DefaultProfile</span></span>
<span data-ttu-id="6c60c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6c60c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c60c-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="6c60c-125">-IncludeAddress</span></span>
<span data-ttu-id="6c60c-126">Укаймь адрес учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="6c60c-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="6c60c-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="6c60c-128">Включив профили вы выставления счетов в учетную запись вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="6c60c-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="6c60c-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="6c60c-130">Включив в них профили выставления счетов в разделах учетной записи выставления счетов и счетах.</span><span class="sxs-lookup"><span data-stu-id="6c60c-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="6c60c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6c60c-131">-Name</span></span>
<span data-ttu-id="6c60c-132">Имя определенной учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="6c60c-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="6c60c-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="6c60c-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="6c60c-134">Перечислить объекты вы счета в учетной записи вы выставления счетов, которую можно использовать для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="6c60c-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="6c60c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c60c-135">CommonParameters</span></span>
<span data-ttu-id="6c60c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c60c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c60c-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c60c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c60c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c60c-138">INPUTS</span></span>

### <span data-ttu-id="6c60c-139">Нет</span><span class="sxs-lookup"><span data-stu-id="6c60c-139">None</span></span>

## <span data-ttu-id="6c60c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c60c-140">OUTPUTS</span></span>

### <span data-ttu-id="6c60c-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="6c60c-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="6c60c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c60c-142">NOTES</span></span>

## <span data-ttu-id="6c60c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c60c-143">RELATED LINKS</span></span>
