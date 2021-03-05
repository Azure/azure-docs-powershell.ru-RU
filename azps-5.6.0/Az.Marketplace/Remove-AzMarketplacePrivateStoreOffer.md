---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 829f6b4e95e1d45d68f12ed6dbd8ad7c7987eba3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003763"
---
# <span data-ttu-id="b3821-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b3821-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="b3821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3821-102">SYNOPSIS</span></span>
<span data-ttu-id="b3821-103">Удаление предложения из частного магазина.</span><span class="sxs-lookup"><span data-stu-id="b3821-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="b3821-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3821-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3821-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3821-105">DESCRIPTION</span></span>
<span data-ttu-id="b3821-106">Удалите предложение из частного магазина, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="b3821-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="b3821-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3821-107">EXAMPLES</span></span>

### <span data-ttu-id="b3821-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3821-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="b3821-109">Удалите предложение из частного магазина, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="b3821-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="b3821-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3821-110">PARAMETERS</span></span>

### <span data-ttu-id="b3821-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3821-111">-DefaultProfile</span></span>
<span data-ttu-id="b3821-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3821-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3821-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b3821-113">-OfferId</span></span>
<span data-ttu-id="b3821-114">Требуемая возможность предложения из частного Магазина Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="b3821-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="b3821-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3821-115">-PassThru</span></span>
<span data-ttu-id="b3821-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b3821-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b3821-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="b3821-117">-PrivateStoreId</span></span>
<span data-ttu-id="b3821-118">Требуемая частная магазина Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="b3821-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="b3821-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3821-119">-Confirm</span></span>
<span data-ttu-id="b3821-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3821-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3821-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3821-121">-WhatIf</span></span>
<span data-ttu-id="b3821-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3821-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3821-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3821-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3821-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3821-124">CommonParameters</span></span>
<span data-ttu-id="b3821-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3821-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3821-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3821-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3821-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3821-127">INPUTS</span></span>

### <span data-ttu-id="b3821-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b3821-128">None</span></span>

## <span data-ttu-id="b3821-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3821-129">OUTPUTS</span></span>

### <span data-ttu-id="b3821-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3821-130">System.Boolean</span></span>

## <span data-ttu-id="b3821-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3821-131">NOTES</span></span>

## <span data-ttu-id="b3821-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3821-132">RELATED LINKS</span></span>
