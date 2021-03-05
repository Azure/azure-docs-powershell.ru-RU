---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 0f5cedd29b7dcc296494519fe40f8ea7e0edb445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964248"
---
# <span data-ttu-id="b0b7d-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="b0b7d-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="b0b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b7d-103">Получить связи безопасности IKE с подключением виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="b0b7d-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="b0b7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0b7d-104">SYNTAX</span></span>

### <span data-ttu-id="b0b7d-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b0b7d-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b7d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b0b7d-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b7d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b7d-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b7d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0b7d-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b7d-109">Командлет **Get-AzVirtualNetworkGatewayConnectionIkeSa** возвращает связи безопасности IKE подключения на основе имени подключения и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="b0b7d-110">Если **командлет Get-AzVirtualNetworkGatewayConnection** выдан без указания параметра -Name, выходные данные не будут указывать связи безопасности IKE.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="b0b7d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0b7d-111">EXAMPLES</span></span>

### <span data-ttu-id="b0b7d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0b7d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="b0b7d-113">Возвращает связи безопасности IKE для подключения виртуального сетевого шлюза с именем myTunnel в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="b0b7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b7d-114">PARAMETERS</span></span>

### <span data-ttu-id="b0b7d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b7d-115">-AsJob</span></span>
<span data-ttu-id="b0b7d-116">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-116">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b7d-117">-DefaultProfile</span></span>
<span data-ttu-id="b0b7d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b7d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b7d-119">-InputObject</span></span>
<span data-ttu-id="b0b7d-120">Объект подключения виртуального сетевого шлюза, для которого требуется получить SAS IKE.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b7d-121">-Name</span></span>
<span data-ttu-id="b0b7d-122">Имя подключения виртуального сетевого шлюза, для которого требуется получить SAS IKE.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0b7d-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b7d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b7d-125">-ResourceId</span></span>
<span data-ttu-id="b0b7d-126">ИД ресурса Azure подключения виртуального сетевого шлюза, для которого требуется получить SAS IKE.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b7d-127">CommonParameters</span></span>
<span data-ttu-id="b0b7d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b7d-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b7d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b7d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b7d-130">INPUTS</span></span>

### <span data-ttu-id="b0b7d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b7d-131">System.String</span></span>

## <span data-ttu-id="b0b7d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b7d-132">OUTPUTS</span></span>

### <span data-ttu-id="b0b7d-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="b0b7d-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="b0b7d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0b7d-134">NOTES</span></span>

## <span data-ttu-id="b0b7d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0b7d-135">RELATED LINKS</span></span>
