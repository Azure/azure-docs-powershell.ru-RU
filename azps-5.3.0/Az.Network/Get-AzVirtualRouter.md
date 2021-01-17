---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422100"
---
# <span data-ttu-id="4b1e9-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4b1e9-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="4b1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1e9-103">Получить Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4b1e9-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="4b1e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b1e9-104">SYNTAX</span></span>

### <span data-ttu-id="4b1e9-105">VirtualRouterSubscriptionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b1e9-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b1e9-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b1e9-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b1e9-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b1e9-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b1e9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b1e9-108">DESCRIPTION</span></span>
<span data-ttu-id="4b1e9-109">**Cmdlet Get-AzVirtualRouter** получает azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4b1e9-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="4b1e9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b1e9-110">EXAMPLES</span></span>

### <span data-ttu-id="4b1e9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b1e9-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="4b1e9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b1e9-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="4b1e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b1e9-113">PARAMETERS</span></span>

### <span data-ttu-id="4b1e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1e9-114">-DefaultProfile</span></span>
<span data-ttu-id="4b1e9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b1e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b1e9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b1e9-116">-ResourceGroupName</span></span>
<span data-ttu-id="4b1e9-117">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="4b1e9-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1e9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b1e9-118">-ResourceId</span></span>
<span data-ttu-id="4b1e9-119">ResourceId виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="4b1e9-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1e9-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="4b1e9-120">-RouterName</span></span>
<span data-ttu-id="4b1e9-121">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="4b1e9-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b1e9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1e9-122">CommonParameters</span></span>
<span data-ttu-id="4b1e9-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b1e9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1e9-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b1e9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1e9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b1e9-125">INPUTS</span></span>

### <span data-ttu-id="4b1e9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4b1e9-126">System.String</span></span>

## <span data-ttu-id="4b1e9-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b1e9-127">OUTPUTS</span></span>

### <span data-ttu-id="4b1e9-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4b1e9-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="4b1e9-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b1e9-129">NOTES</span></span>

## <span data-ttu-id="4b1e9-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b1e9-130">RELATED LINKS</span></span>
