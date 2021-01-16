---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394191"
---
# <span data-ttu-id="ea29b-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea29b-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="ea29b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea29b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea29b-103">Создание локального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="ea29b-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="ea29b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea29b-104">SYNTAX</span></span>

### <span data-ttu-id="ea29b-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea29b-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea29b-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="ea29b-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea29b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea29b-107">DESCRIPTION</span></span>
<span data-ttu-id="ea29b-108">Локальный сетевой шлюз — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="ea29b-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="ea29b-109">Командлет **New-AzLocalNetworkGateway** создает объект, представляющий ваш собственный шлюз, на основе имени, названия группы ресурсов, расположения и IP-адреса шлюза, а также префикса адреса локальной сети, которая будет подключаться к Azure.</span><span class="sxs-lookup"><span data-stu-id="ea29b-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="ea29b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea29b-110">EXAMPLES</span></span>

### <span data-ttu-id="ea29b-111">Пример 1. Создание локального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="ea29b-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="ea29b-112">Создает объект локального сетевого шлюза с именем myLocalGW в группе ресурсов myRG в расположении "Западная ЧАСТЬ США" с IP-адресом 23.99.221.164 и префиксом адреса "10.5.51.0/24" в локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="ea29b-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="ea29b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea29b-113">PARAMETERS</span></span>

### <span data-ttu-id="ea29b-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ea29b-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea29b-115">-AsJob</span></span>
<span data-ttu-id="ea29b-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ea29b-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="ea29b-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ea29b-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="ea29b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea29b-119">-DefaultProfile</span></span>
<span data-ttu-id="ea29b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea29b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea29b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ea29b-121">-Force</span></span>
<span data-ttu-id="ea29b-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ea29b-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="ea29b-123">-Fqdn</span></span>
<span data-ttu-id="ea29b-124">FQDN локального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="ea29b-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea29b-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ea29b-126">-Location</span></span>
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

### <span data-ttu-id="ea29b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ea29b-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ea29b-128">-PeerWeight</span></span>
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

### <span data-ttu-id="ea29b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea29b-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea29b-130">Группа ресурсов, к которой принадлежит локальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="ea29b-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="ea29b-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea29b-131">-Tag</span></span>
<span data-ttu-id="ea29b-132">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="ea29b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea29b-133">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ea29b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea29b-134">-Confirm</span></span>
<span data-ttu-id="ea29b-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea29b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea29b-136">-WhatIf</span></span>
<span data-ttu-id="ea29b-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea29b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea29b-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea29b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea29b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea29b-139">CommonParameters</span></span>
<span data-ttu-id="ea29b-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea29b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea29b-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea29b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea29b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea29b-142">INPUTS</span></span>

### <span data-ttu-id="ea29b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ea29b-143">System.String</span></span>

### <span data-ttu-id="ea29b-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ea29b-144">System.String[]</span></span>

### <span data-ttu-id="ea29b-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="ea29b-145">System.UInt32</span></span>

### <span data-ttu-id="ea29b-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ea29b-146">System.Int32</span></span>

### <span data-ttu-id="ea29b-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea29b-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ea29b-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea29b-148">OUTPUTS</span></span>

### <span data-ttu-id="ea29b-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea29b-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ea29b-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea29b-150">NOTES</span></span>

## <span data-ttu-id="ea29b-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea29b-151">RELATED LINKS</span></span>

[<span data-ttu-id="ea29b-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea29b-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ea29b-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea29b-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="ea29b-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea29b-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)