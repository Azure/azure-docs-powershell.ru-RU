---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417428"
---
# <span data-ttu-id="d2c81-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="d2c81-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="d2c81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c81-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c81-103">Создание конфигурации внешнего сервера в радиусе</span><span class="sxs-lookup"><span data-stu-id="d2c81-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="d2c81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2c81-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2c81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2c81-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c81-106">С New-AzRadiusServer создается конфигурация сервера внешнего радиуса, которая будет использоваться в конфигурации виртуального сетевого шлюза и сервера VPN.</span><span class="sxs-lookup"><span data-stu-id="d2c81-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="d2c81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2c81-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c81-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2c81-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="d2c81-109">Создание нескольких конфигураций серверов с несколькими внешними радиусами для настройки P2S в новом виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="d2c81-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="d2c81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c81-110">PARAMETERS</span></span>

### <span data-ttu-id="d2c81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c81-111">-DefaultProfile</span></span>
<span data-ttu-id="d2c81-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c81-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d2c81-113">-RadiusServerAddress</span></span>
<span data-ttu-id="d2c81-114">Адрес внешнего радиуса сервера</span><span class="sxs-lookup"><span data-stu-id="d2c81-114">External radius server address</span></span>

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

### <span data-ttu-id="d2c81-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="d2c81-115">-RadiusServerScore</span></span>
<span data-ttu-id="d2c81-116">Оценка внешнего радиуса сервера</span><span class="sxs-lookup"><span data-stu-id="d2c81-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c81-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d2c81-117">-RadiusServerSecret</span></span>
<span data-ttu-id="d2c81-118">Секрет внешнего радиуса сервера</span><span class="sxs-lookup"><span data-stu-id="d2c81-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c81-119">CommonParameters</span></span>
<span data-ttu-id="d2c81-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c81-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2c81-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c81-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c81-122">INPUTS</span></span>

### <span data-ttu-id="d2c81-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d2c81-123">System.String</span></span>

### <span data-ttu-id="d2c81-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d2c81-124">System.Security.SecureString</span></span>

### <span data-ttu-id="d2c81-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d2c81-125">System.Int32</span></span>

## <span data-ttu-id="d2c81-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c81-126">OUTPUTS</span></span>

### <span data-ttu-id="d2c81-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="d2c81-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="d2c81-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2c81-128">NOTES</span></span>

## <span data-ttu-id="d2c81-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2c81-129">RELATED LINKS</span></span>
