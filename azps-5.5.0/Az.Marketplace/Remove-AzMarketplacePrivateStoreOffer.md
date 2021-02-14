---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221489"
---
# <span data-ttu-id="0362b-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="0362b-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="0362b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0362b-102">SYNOPSIS</span></span>
<span data-ttu-id="0362b-103">Удалить предложение из частного магазина.</span><span class="sxs-lookup"><span data-stu-id="0362b-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="0362b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0362b-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0362b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0362b-105">DESCRIPTION</span></span>
<span data-ttu-id="0362b-106">Удалите предложение из частного магазина, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="0362b-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="0362b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0362b-107">EXAMPLES</span></span>

### <span data-ttu-id="0362b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0362b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="0362b-109">Удалите предложение из частного магазина, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="0362b-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="0362b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0362b-110">PARAMETERS</span></span>

### <span data-ttu-id="0362b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0362b-111">-DefaultProfile</span></span>
<span data-ttu-id="0362b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0362b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0362b-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="0362b-113">-OfferId</span></span>
<span data-ttu-id="0362b-114">Обязательное предложение privateStore для Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="0362b-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="0362b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0362b-115">-PassThru</span></span>
<span data-ttu-id="0362b-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0362b-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0362b-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="0362b-117">-PrivateStoreId</span></span>
<span data-ttu-id="0362b-118">Требуемая частная магазина Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="0362b-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="0362b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0362b-119">-Confirm</span></span>
<span data-ttu-id="0362b-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0362b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0362b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0362b-121">-WhatIf</span></span>
<span data-ttu-id="0362b-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0362b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0362b-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0362b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0362b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0362b-124">CommonParameters</span></span>
<span data-ttu-id="0362b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0362b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0362b-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0362b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0362b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0362b-127">INPUTS</span></span>

### <span data-ttu-id="0362b-128">Нет</span><span class="sxs-lookup"><span data-stu-id="0362b-128">None</span></span>

## <span data-ttu-id="0362b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0362b-129">OUTPUTS</span></span>

### <span data-ttu-id="0362b-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0362b-130">System.Boolean</span></span>

## <span data-ttu-id="0362b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0362b-131">NOTES</span></span>

## <span data-ttu-id="0362b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0362b-132">RELATED LINKS</span></span>
