---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248417"
---
# <span data-ttu-id="ff73c-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="ff73c-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="ff73c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff73c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff73c-103">Получить разделы счета.</span><span class="sxs-lookup"><span data-stu-id="ff73c-103">Get invoice sections.</span></span>

## <span data-ttu-id="ff73c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff73c-104">SYNTAX</span></span>

### <span data-ttu-id="ff73c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff73c-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff73c-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="ff73c-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff73c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff73c-107">DESCRIPTION</span></span>
<span data-ttu-id="ff73c-108">Командлет **Get-AzInvoiceSection** получает разделы счета в соответствии с заданным профилем выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="ff73c-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="ff73c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff73c-109">EXAMPLES</span></span>

### <span data-ttu-id="ff73c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff73c-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="ff73c-111">Получить все разделы счета в соответствии с заданным профилем выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="ff73c-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="ff73c-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ff73c-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="ff73c-113">Получить раздел счета с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="ff73c-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="ff73c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff73c-114">PARAMETERS</span></span>

### <span data-ttu-id="ff73c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff73c-115">-DefaultProfile</span></span>
<span data-ttu-id="ff73c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff73c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff73c-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="ff73c-117">-BillingAccountName</span></span>
<span data-ttu-id="ff73c-118">Название определенного счета для выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="ff73c-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="ff73c-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="ff73c-119">-BillingProfileName</span></span>
<span data-ttu-id="ff73c-120">Название определенного профиля выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="ff73c-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="ff73c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff73c-121">-Name</span></span>
<span data-ttu-id="ff73c-122">Название определенного раздела счета.</span><span class="sxs-lookup"><span data-stu-id="ff73c-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="ff73c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff73c-123">CommonParameters</span></span>
<span data-ttu-id="ff73c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff73c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff73c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff73c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff73c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff73c-126">INPUTS</span></span>

### <span data-ttu-id="ff73c-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="ff73c-127">None</span></span>

## <span data-ttu-id="ff73c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff73c-128">OUTPUTS</span></span>

### <span data-ttu-id="ff73c-129">Microsoft. Azure. Commands. Bill. Models. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="ff73c-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="ff73c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff73c-130">NOTES</span></span>

## <span data-ttu-id="ff73c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff73c-131">RELATED LINKS</span></span>
