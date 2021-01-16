---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509510"
---
# <span data-ttu-id="d693e-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="d693e-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="d693e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d693e-102">SYNOPSIS</span></span>
<span data-ttu-id="d693e-103">Получить разделы счета.</span><span class="sxs-lookup"><span data-stu-id="d693e-103">Get invoice sections.</span></span>

## <span data-ttu-id="d693e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d693e-104">SYNTAX</span></span>

### <span data-ttu-id="d693e-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d693e-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d693e-106">Один</span><span class="sxs-lookup"><span data-stu-id="d693e-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d693e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d693e-107">DESCRIPTION</span></span>
<span data-ttu-id="d693e-108">Для этого вы можете получить **разделы** счетов в указанном профиле выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="d693e-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="d693e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d693e-109">EXAMPLES</span></span>

### <span data-ttu-id="d693e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d693e-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="d693e-111">Получить все разделы счетов в указанном профиле выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="d693e-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="d693e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d693e-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="d693e-113">Получить раздел счета с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d693e-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="d693e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d693e-114">PARAMETERS</span></span>

### <span data-ttu-id="d693e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d693e-115">-DefaultProfile</span></span>
<span data-ttu-id="d693e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d693e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d693e-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="d693e-117">-BillingAccountName</span></span>
<span data-ttu-id="d693e-118">Имя определенной учетной записи вы выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="d693e-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="d693e-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="d693e-119">-BillingProfileName</span></span>
<span data-ttu-id="d693e-120">Имя определенного профиля вы выставления счета.</span><span class="sxs-lookup"><span data-stu-id="d693e-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="d693e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d693e-121">-Name</span></span>
<span data-ttu-id="d693e-122">Имя определенного раздела счета.</span><span class="sxs-lookup"><span data-stu-id="d693e-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="d693e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d693e-123">CommonParameters</span></span>
<span data-ttu-id="d693e-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d693e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d693e-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d693e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d693e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d693e-126">INPUTS</span></span>

### <span data-ttu-id="d693e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d693e-127">None</span></span>

## <span data-ttu-id="d693e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d693e-128">OUTPUTS</span></span>

### <span data-ttu-id="d693e-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="d693e-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="d693e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d693e-130">NOTES</span></span>

## <span data-ttu-id="d693e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d693e-131">RELATED LINKS</span></span>
