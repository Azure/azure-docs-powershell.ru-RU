---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506525"
---
# <span data-ttu-id="a8d5b-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a8d5b-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a8d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d5b-103">Получить удостоверение, назначенное шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a8d5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8d5b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8d5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d5b-106">**Cmdlet Get-AzApplicationGatewayIdentity** получает удостоверение, назначенное шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="a8d5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="a8d5b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8d5b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="a8d5b-109">В этих примерах показано, как получить удостоверение шлюза приложения у шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="a8d5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8d5b-110">PARAMETERS</span></span>

### <span data-ttu-id="a8d5b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8d5b-111">-ApplicationGateway</span></span>
<span data-ttu-id="a8d5b-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8d5b-112">The applicationGateway</span></span>

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

### <span data-ttu-id="a8d5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d5b-113">-DefaultProfile</span></span>
<span data-ttu-id="a8d5b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d5b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d5b-115">CommonParameters</span></span>
<span data-ttu-id="a8d5b-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d5b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d5b-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8d5b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d5b-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d5b-118">INPUTS</span></span>

### <span data-ttu-id="a8d5b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8d5b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8d5b-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8d5b-120">OUTPUTS</span></span>

### <span data-ttu-id="a8d5b-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a8d5b-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="a8d5b-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8d5b-122">NOTES</span></span>

## <span data-ttu-id="a8d5b-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8d5b-123">RELATED LINKS</span></span>
