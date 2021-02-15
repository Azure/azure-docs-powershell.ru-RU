---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223780"
---
# <span data-ttu-id="8fd73-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8fd73-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="8fd73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd73-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd73-103">Отображает общий ключ, используемый для подключения.</span><span class="sxs-lookup"><span data-stu-id="8fd73-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="8fd73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8fd73-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd73-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fd73-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd73-106">Отображает общий ключ, используемый для подключения.</span><span class="sxs-lookup"><span data-stu-id="8fd73-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="8fd73-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8fd73-107">EXAMPLES</span></span>

### <span data-ttu-id="8fd73-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8fd73-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="8fd73-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fd73-109">PARAMETERS</span></span>

### <span data-ttu-id="8fd73-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd73-110">-DefaultProfile</span></span>
<span data-ttu-id="8fd73-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd73-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd73-112">-Name</span><span class="sxs-lookup"><span data-stu-id="8fd73-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd73-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd73-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd73-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd73-114">CommonParameters</span></span>
<span data-ttu-id="8fd73-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd73-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd73-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fd73-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd73-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fd73-117">INPUTS</span></span>

### <span data-ttu-id="8fd73-118">System.String</span><span class="sxs-lookup"><span data-stu-id="8fd73-118">System.String</span></span>

## <span data-ttu-id="8fd73-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8fd73-119">OUTPUTS</span></span>

### <span data-ttu-id="8fd73-120">System.String</span><span class="sxs-lookup"><span data-stu-id="8fd73-120">System.String</span></span>

## <span data-ttu-id="8fd73-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8fd73-121">NOTES</span></span>

## <span data-ttu-id="8fd73-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fd73-122">RELATED LINKS</span></span>

[<span data-ttu-id="8fd73-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8fd73-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="8fd73-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8fd73-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
