---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520012"
---
# <span data-ttu-id="0a8c7-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0a8c7-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="0a8c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8c7-103">Получает политику брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="0a8c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a8c7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8c7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a8c7-105">DESCRIPTION</span></span>
<span data-ttu-id="0a8c7-106">Для **шлюза get-AzApplicationGatewayFirewallPolicy** политика брандмауэра шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="0a8c7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a8c7-107">EXAMPLES</span></span>

### <span data-ttu-id="0a8c7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a8c7-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0a8c7-109">Эта команда получает политику брандмауэра шлюза приложения FirewallPolicy1, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="0a8c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a8c7-110">PARAMETERS</span></span>

### <span data-ttu-id="0a8c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8c7-111">-DefaultProfile</span></span>
<span data-ttu-id="0a8c7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a8c7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0a8c7-113">-Name</span></span>
<span data-ttu-id="0a8c7-114">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-114">The resource name.</span></span>

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

### <span data-ttu-id="0a8c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a8c7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8c7-117">CommonParameters</span></span>
<span data-ttu-id="0a8c7-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8c7-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a8c7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8c7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a8c7-120">INPUTS</span></span>

### <span data-ttu-id="0a8c7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0a8c7-121">System.String</span></span>

## <span data-ttu-id="0a8c7-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a8c7-122">OUTPUTS</span></span>

### <span data-ttu-id="0a8c7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0a8c7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="0a8c7-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a8c7-124">NOTES</span></span>

## <span data-ttu-id="0a8c7-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a8c7-125">RELATED LINKS</span></span>
