---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064817"
---
# <span data-ttu-id="61636-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="61636-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="61636-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61636-102">SYNOPSIS</span></span>
<span data-ttu-id="61636-103">Удаляет удостоверение из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="61636-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="61636-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61636-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61636-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61636-105">DESCRIPTION</span></span>
<span data-ttu-id="61636-106">Командлет **Remove-AzApplicationGatewayIdentity** удаляет удостоверение из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="61636-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="61636-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61636-107">EXAMPLES</span></span>

### <span data-ttu-id="61636-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61636-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="61636-109">В этом примере мы удалим удостоверение из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="61636-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="61636-110">Примечание. Если шлюз ссылается на секрет keyvault, важно также удалить эти ссылки на сертификаты SSL в этой операции.</span><span class="sxs-lookup"><span data-stu-id="61636-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="61636-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61636-111">PARAMETERS</span></span>

### <span data-ttu-id="61636-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61636-112">-ApplicationGateway</span></span>
<span data-ttu-id="61636-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61636-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61636-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61636-114">-DefaultProfile</span></span>
<span data-ttu-id="61636-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61636-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61636-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61636-116">-Confirm</span></span>
<span data-ttu-id="61636-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61636-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61636-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61636-118">-WhatIf</span></span>
<span data-ttu-id="61636-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61636-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61636-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61636-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61636-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61636-121">CommonParameters</span></span>
<span data-ttu-id="61636-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61636-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61636-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61636-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61636-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61636-124">INPUTS</span></span>

### <span data-ttu-id="61636-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61636-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61636-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61636-126">OUTPUTS</span></span>

### <span data-ttu-id="61636-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61636-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61636-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="61636-128">NOTES</span></span>

## <span data-ttu-id="61636-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61636-129">RELATED LINKS</span></span>
