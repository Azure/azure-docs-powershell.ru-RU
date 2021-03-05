---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 105097f30ea87637cd0ad4bd16e0b8da922c2f4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001171"
---
# <span data-ttu-id="f830f-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f830f-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f830f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f830f-102">SYNOPSIS</span></span>
<span data-ttu-id="f830f-103">Получение удостоверений, назначенных шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="f830f-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="f830f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f830f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f830f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f830f-105">DESCRIPTION</span></span>
<span data-ttu-id="f830f-106">Для **шлюза приложения удостоверение get-AzApplicationGatewayIdentity** назначено.</span><span class="sxs-lookup"><span data-stu-id="f830f-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="f830f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f830f-107">EXAMPLES</span></span>

### <span data-ttu-id="f830f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f830f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="f830f-109">В этих примерах показано, как получить удостоверение шлюза приложения у шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f830f-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="f830f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f830f-110">PARAMETERS</span></span>

### <span data-ttu-id="f830f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f830f-111">-ApplicationGateway</span></span>
<span data-ttu-id="f830f-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f830f-112">The applicationGateway</span></span>

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

### <span data-ttu-id="f830f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f830f-113">-DefaultProfile</span></span>
<span data-ttu-id="f830f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f830f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f830f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f830f-115">CommonParameters</span></span>
<span data-ttu-id="f830f-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f830f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f830f-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f830f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f830f-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f830f-118">INPUTS</span></span>

### <span data-ttu-id="f830f-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f830f-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f830f-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f830f-120">OUTPUTS</span></span>

### <span data-ttu-id="f830f-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f830f-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f830f-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f830f-122">NOTES</span></span>

## <span data-ttu-id="f830f-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f830f-123">RELATED LINKS</span></span>
