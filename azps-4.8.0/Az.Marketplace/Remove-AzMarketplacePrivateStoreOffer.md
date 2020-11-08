---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078187"
---
# <span data-ttu-id="ce47d-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="ce47d-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="ce47d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce47d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce47d-103">Удаление предложения из частного магазина.</span><span class="sxs-lookup"><span data-stu-id="ce47d-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="ce47d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce47d-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce47d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce47d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce47d-106">Удаление предложения из закрытого хранилища, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="ce47d-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="ce47d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce47d-107">EXAMPLES</span></span>

### <span data-ttu-id="ce47d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce47d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="ce47d-109">Удаление предложения из закрытого хранилища, созданного в области клиента.</span><span class="sxs-lookup"><span data-stu-id="ce47d-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="ce47d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce47d-110">PARAMETERS</span></span>

### <span data-ttu-id="ce47d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce47d-111">-DefaultProfile</span></span>
<span data-ttu-id="ce47d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce47d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce47d-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="ce47d-113">-OfferId</span></span>
<span data-ttu-id="ce47d-114">Обязательное предложение Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="ce47d-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="ce47d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce47d-115">-PassThru</span></span>
<span data-ttu-id="ce47d-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ce47d-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ce47d-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="ce47d-117">-PrivateStoreId</span></span>
<span data-ttu-id="ce47d-118">Обязательный каталог Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="ce47d-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="ce47d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce47d-119">-Confirm</span></span>
<span data-ttu-id="ce47d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce47d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce47d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce47d-121">-WhatIf</span></span>
<span data-ttu-id="ce47d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce47d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce47d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce47d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce47d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce47d-124">CommonParameters</span></span>
<span data-ttu-id="ce47d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce47d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce47d-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce47d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce47d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce47d-127">INPUTS</span></span>

### <span data-ttu-id="ce47d-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="ce47d-128">None</span></span>

## <span data-ttu-id="ce47d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce47d-129">OUTPUTS</span></span>

### <span data-ttu-id="ce47d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce47d-130">System.Boolean</span></span>

## <span data-ttu-id="ce47d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce47d-131">NOTES</span></span>

## <span data-ttu-id="ce47d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce47d-132">RELATED LINKS</span></span>
