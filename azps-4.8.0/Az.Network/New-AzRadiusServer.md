---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079459"
---
# <span data-ttu-id="3ec37-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="3ec37-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="3ec37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ec37-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec37-103">Создание конфигурации внешнего RADIUS-сервера</span><span class="sxs-lookup"><span data-stu-id="3ec37-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="3ec37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ec37-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ec37-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ec37-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec37-106">Командлет New-AzRadiusServer создает конфигурацию внешнего сервера RADIUS для использования в конфигурации шлюза виртуальной сети и VPN-сервера.</span><span class="sxs-lookup"><span data-stu-id="3ec37-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="3ec37-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ec37-107">EXAMPLES</span></span>

### <span data-ttu-id="3ec37-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ec37-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="3ec37-109">Создание нескольких внешних конфигураций RADIUS-серверов, используемых для настройки P2S на новом шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3ec37-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="3ec37-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ec37-110">PARAMETERS</span></span>

### <span data-ttu-id="3ec37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec37-111">-DefaultProfile</span></span>
<span data-ttu-id="3ec37-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec37-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ec37-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="3ec37-113">-RadiusServerAddress</span></span>
<span data-ttu-id="3ec37-114">Адрес внешнего RADIUS-сервера</span><span class="sxs-lookup"><span data-stu-id="3ec37-114">External radius server address</span></span>

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

### <span data-ttu-id="3ec37-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="3ec37-115">-RadiusServerScore</span></span>
<span data-ttu-id="3ec37-116">Оценка внешнего RADIUS-сервера</span><span class="sxs-lookup"><span data-stu-id="3ec37-116">External radius server score</span></span>

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

### <span data-ttu-id="3ec37-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="3ec37-117">-RadiusServerSecret</span></span>
<span data-ttu-id="3ec37-118">Секрет внешний RADIUS-сервер</span><span class="sxs-lookup"><span data-stu-id="3ec37-118">External radius server secret</span></span>

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

### <span data-ttu-id="3ec37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec37-119">CommonParameters</span></span>
<span data-ttu-id="3ec37-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ec37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec37-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ec37-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec37-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ec37-122">INPUTS</span></span>

### <span data-ttu-id="3ec37-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3ec37-123">System.String</span></span>

### <span data-ttu-id="3ec37-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3ec37-124">System.Security.SecureString</span></span>

### <span data-ttu-id="3ec37-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3ec37-125">System.Int32</span></span>

## <span data-ttu-id="3ec37-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ec37-126">OUTPUTS</span></span>

### <span data-ttu-id="3ec37-127">Microsoft. Azure. Commands. Network. Models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="3ec37-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="3ec37-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ec37-128">NOTES</span></span>

## <span data-ttu-id="3ec37-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ec37-129">RELATED LINKS</span></span>
