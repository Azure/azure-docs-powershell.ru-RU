---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: c66b3a2c4c151daf0a5d3df62aaaf248a7d2e338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986219"
---
# <span data-ttu-id="858e8-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="858e8-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="858e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858e8-102">SYNOPSIS</span></span>
<span data-ttu-id="858e8-103">Получить профили вы выставления счета.</span><span class="sxs-lookup"><span data-stu-id="858e8-103">Get billing profiles.</span></span>

## <span data-ttu-id="858e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="858e8-104">SYNTAX</span></span>

### <span data-ttu-id="858e8-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="858e8-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="858e8-106">Один</span><span class="sxs-lookup"><span data-stu-id="858e8-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858e8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="858e8-107">DESCRIPTION</span></span>
<span data-ttu-id="858e8-108">Для **этого с его учетной** записью вы получаете профили вы счетов.</span><span class="sxs-lookup"><span data-stu-id="858e8-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="858e8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="858e8-109">EXAMPLES</span></span>

### <span data-ttu-id="858e8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="858e8-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="858e8-111">Получить все профили вы выставления счетов в соответствии с указанной учетной записью вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="858e8-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="858e8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="858e8-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="858e8-113">Получите профиль вы выставления счета с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="858e8-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="858e8-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="858e8-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="858e8-115">Получите все профили выставления счетов, указанные в указанной учетной записи выставления счетов, и включим в результат разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="858e8-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="858e8-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="858e8-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="858e8-117">Получите профиль выставления счетов с указанным именем и включим в результат разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="858e8-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="858e8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="858e8-118">PARAMETERS</span></span>

### <span data-ttu-id="858e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858e8-119">-DefaultProfile</span></span>
<span data-ttu-id="858e8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="858e8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="858e8-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="858e8-121">-BillingAccountName</span></span>
<span data-ttu-id="858e8-122">Имя определенной учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="858e8-122">Name of the specific billing account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e8-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="858e8-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="858e8-124">Включать разделы счетов в профиль выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="858e8-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="858e8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="858e8-125">-Name</span></span>
<span data-ttu-id="858e8-126">Имя определенного профиля вы выставления счета.</span><span class="sxs-lookup"><span data-stu-id="858e8-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="858e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858e8-127">CommonParameters</span></span>
<span data-ttu-id="858e8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858e8-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858e8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858e8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="858e8-130">INPUTS</span></span>

### <span data-ttu-id="858e8-131">Нет</span><span class="sxs-lookup"><span data-stu-id="858e8-131">None</span></span>

## <span data-ttu-id="858e8-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="858e8-132">OUTPUTS</span></span>

### <span data-ttu-id="858e8-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="858e8-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="858e8-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="858e8-134">NOTES</span></span>

## <span data-ttu-id="858e8-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="858e8-135">RELATED LINKS</span></span>
