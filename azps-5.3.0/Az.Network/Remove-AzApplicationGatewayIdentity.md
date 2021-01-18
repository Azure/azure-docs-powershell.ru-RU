---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518074"
---
# <span data-ttu-id="12635-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="12635-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="12635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12635-102">SYNOPSIS</span></span>
<span data-ttu-id="12635-103">Удаляет удостоверение из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="12635-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="12635-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12635-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12635-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12635-105">DESCRIPTION</span></span>
<span data-ttu-id="12635-106">**Cmdlet Remove-AzApplicationGatewayIdentity** удаляет удостоверение из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="12635-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="12635-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12635-107">EXAMPLES</span></span>

### <span data-ttu-id="12635-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12635-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="12635-109">В этом примере мы удаляем удостоверения из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="12635-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="12635-110">Примечание. Если шлюз ссылается на секрет keyvault, важно также удалить эти ссылки на SSL-сертификаты в ходе этой операции.</span><span class="sxs-lookup"><span data-stu-id="12635-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="12635-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12635-111">PARAMETERS</span></span>

### <span data-ttu-id="12635-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12635-112">-ApplicationGateway</span></span>
<span data-ttu-id="12635-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12635-113">The applicationGateway</span></span>

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

### <span data-ttu-id="12635-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12635-114">-DefaultProfile</span></span>
<span data-ttu-id="12635-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12635-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12635-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12635-116">-Confirm</span></span>
<span data-ttu-id="12635-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="12635-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12635-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12635-118">-WhatIf</span></span>
<span data-ttu-id="12635-119">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12635-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12635-120">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12635-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12635-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12635-121">CommonParameters</span></span>
<span data-ttu-id="12635-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12635-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12635-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12635-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12635-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12635-124">INPUTS</span></span>

### <span data-ttu-id="12635-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12635-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12635-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12635-126">OUTPUTS</span></span>

### <span data-ttu-id="12635-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12635-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12635-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12635-128">NOTES</span></span>

## <span data-ttu-id="12635-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12635-129">RELATED LINKS</span></span>
