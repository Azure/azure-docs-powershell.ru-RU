---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248425"
---
# <span data-ttu-id="3888b-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="3888b-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="3888b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3888b-102">SYNOPSIS</span></span>
<span data-ttu-id="3888b-103">Получение профилей выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3888b-103">Get billing profiles.</span></span>

## <span data-ttu-id="3888b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3888b-104">SYNTAX</span></span>

### <span data-ttu-id="3888b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3888b-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3888b-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="3888b-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3888b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3888b-107">DESCRIPTION</span></span>
<span data-ttu-id="3888b-108">Командлет **Get-AzBillingProfile** получает профили выставления счетов в соответствии с указанным счетом выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3888b-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="3888b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3888b-109">EXAMPLES</span></span>

### <span data-ttu-id="3888b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3888b-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="3888b-111">Получить все профили выставления счетов в соответствии с заданным счетом выставления счета.</span><span class="sxs-lookup"><span data-stu-id="3888b-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="3888b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3888b-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="3888b-113">Получение профиля выставления счетов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="3888b-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="3888b-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3888b-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="3888b-115">Получить все профили выставления счетов в указанном счете, а затем включить в результат разделы счета.</span><span class="sxs-lookup"><span data-stu-id="3888b-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="3888b-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="3888b-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="3888b-117">Получить профиль выставления счетов с указанным именем и включить в результат разделы счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="3888b-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="3888b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3888b-118">PARAMETERS</span></span>

### <span data-ttu-id="3888b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3888b-119">-DefaultProfile</span></span>
<span data-ttu-id="3888b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3888b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3888b-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="3888b-121">-BillingAccountName</span></span>
<span data-ttu-id="3888b-122">Название определенного счета для выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3888b-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="3888b-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="3888b-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="3888b-124">Включение разделов "счета" в разделе "профиль выставления счетов".</span><span class="sxs-lookup"><span data-stu-id="3888b-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="3888b-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3888b-125">-Name</span></span>
<span data-ttu-id="3888b-126">Название определенного профиля выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3888b-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="3888b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3888b-127">CommonParameters</span></span>
<span data-ttu-id="3888b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3888b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3888b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3888b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3888b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3888b-130">INPUTS</span></span>

### <span data-ttu-id="3888b-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="3888b-131">None</span></span>

## <span data-ttu-id="3888b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3888b-132">OUTPUTS</span></span>

### <span data-ttu-id="3888b-133">Microsoft. Azure. Commands. Bill. Models. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="3888b-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="3888b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3888b-134">NOTES</span></span>

## <span data-ttu-id="3888b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3888b-135">RELATED LINKS</span></span>
