---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233561"
---
# <span data-ttu-id="192ff-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="192ff-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="192ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="192ff-102">SYNOPSIS</span></span>
<span data-ttu-id="192ff-103">Получить профили вы выставления счета.</span><span class="sxs-lookup"><span data-stu-id="192ff-103">Get billing profiles.</span></span>

## <span data-ttu-id="192ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="192ff-104">SYNTAX</span></span>

### <span data-ttu-id="192ff-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="192ff-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="192ff-106">Один</span><span class="sxs-lookup"><span data-stu-id="192ff-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="192ff-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="192ff-107">DESCRIPTION</span></span>
<span data-ttu-id="192ff-108">Для **этого с его учетной** записью вы получаете профили счетов.</span><span class="sxs-lookup"><span data-stu-id="192ff-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="192ff-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="192ff-109">EXAMPLES</span></span>

### <span data-ttu-id="192ff-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="192ff-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="192ff-111">Получить все профили вы выставления счетов, указанные в указанной учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="192ff-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="192ff-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="192ff-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="192ff-113">Получите профиль вы выставления счета с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="192ff-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="192ff-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="192ff-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="192ff-115">Получите все профили выставления счетов, указанные в указанной учетной записи выставления счетов, и включим в результат разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="192ff-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="192ff-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="192ff-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="192ff-117">Получите профиль выставления счетов с указанным именем и включим в результат разделы счетов.</span><span class="sxs-lookup"><span data-stu-id="192ff-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="192ff-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="192ff-118">PARAMETERS</span></span>

### <span data-ttu-id="192ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192ff-119">-DefaultProfile</span></span>
<span data-ttu-id="192ff-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="192ff-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="192ff-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="192ff-121">-BillingAccountName</span></span>
<span data-ttu-id="192ff-122">Имя определенной учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="192ff-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="192ff-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="192ff-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="192ff-124">Включать разделы счетов в профиль выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="192ff-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="192ff-125">-Name</span><span class="sxs-lookup"><span data-stu-id="192ff-125">-Name</span></span>
<span data-ttu-id="192ff-126">Имя определенного профиля вы выставления счета.</span><span class="sxs-lookup"><span data-stu-id="192ff-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="192ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192ff-127">CommonParameters</span></span>
<span data-ttu-id="192ff-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192ff-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="192ff-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192ff-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="192ff-130">INPUTS</span></span>

### <span data-ttu-id="192ff-131">Нет</span><span class="sxs-lookup"><span data-stu-id="192ff-131">None</span></span>

## <span data-ttu-id="192ff-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="192ff-132">OUTPUTS</span></span>

### <span data-ttu-id="192ff-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="192ff-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="192ff-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="192ff-134">NOTES</span></span>

## <span data-ttu-id="192ff-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="192ff-135">RELATED LINKS</span></span>
