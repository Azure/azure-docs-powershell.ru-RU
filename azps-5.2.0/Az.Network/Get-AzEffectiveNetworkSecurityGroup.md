---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416124"
---
# <span data-ttu-id="c6002-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6002-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="c6002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6002-102">SYNOPSIS</span></span>
<span data-ttu-id="c6002-103">Получает эффективную группу безопасности сети в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c6002-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="c6002-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6002-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6002-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6002-105">DESCRIPTION</span></span>
<span data-ttu-id="c6002-106">Командлет **Get-AzEffectiveNetworkSecurityGroup** возвращает эффективную группу безопасности сети, примененную в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c6002-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="c6002-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6002-107">EXAMPLES</span></span>

### <span data-ttu-id="c6002-108">Пример 1. Получите эффективную группу безопасности сети в сетевом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="c6002-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="c6002-109">Эта команда получает все эффективные правила безопасности сети, связанные с сетевым интерфейсом MyNetworkInterface в группе ресурсов myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c6002-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="c6002-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6002-110">PARAMETERS</span></span>

### <span data-ttu-id="c6002-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6002-111">-DefaultProfile</span></span>
<span data-ttu-id="c6002-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6002-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6002-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c6002-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="c6002-114">Имя сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c6002-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="c6002-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6002-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6002-116">Группа ресурсов в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c6002-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="c6002-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6002-117">CommonParameters</span></span>
<span data-ttu-id="c6002-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6002-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6002-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6002-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6002-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6002-120">INPUTS</span></span>

### <span data-ttu-id="c6002-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c6002-121">System.String</span></span>

## <span data-ttu-id="c6002-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6002-122">OUTPUTS</span></span>

### <span data-ttu-id="c6002-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6002-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="c6002-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6002-124">NOTES</span></span>

## <span data-ttu-id="c6002-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6002-125">RELATED LINKS</span></span>

[<span data-ttu-id="c6002-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6002-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


