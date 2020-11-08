---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244826"
---
# <span data-ttu-id="ceed4-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ceed4-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="ceed4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceed4-102">SYNOPSIS</span></span>
<span data-ttu-id="ceed4-103">Создание шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="ceed4-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="ceed4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceed4-104">SYNTAX</span></span>

### <span data-ttu-id="ceed4-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="ceed4-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceed4-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="ceed4-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ceed4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceed4-107">DESCRIPTION</span></span>
<span data-ttu-id="ceed4-108">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="ceed4-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="ceed4-109">Командлет **New-AzLocalNetworkGateway** создает объект, представляющий локальный шлюз, на основе имени, имени группы ресурсов, расположения и IP-адреса шлюза, а также префикса адреса локальной сети, которая будет подключаться к Azure.</span><span class="sxs-lookup"><span data-stu-id="ceed4-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="ceed4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceed4-110">EXAMPLES</span></span>

### <span data-ttu-id="ceed4-111">Пример 1: Создание шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="ceed4-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="ceed4-112">Создает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG" в расположении "Западная часть США" с IP-адресом "23.99.221.164" и префиксом адреса "10.5.51.0/24" в локальной среде.</span><span class="sxs-lookup"><span data-stu-id="ceed4-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="ceed4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceed4-113">PARAMETERS</span></span>

### <span data-ttu-id="ceed4-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ceed4-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="ceed4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceed4-115">-AsJob</span></span>
<span data-ttu-id="ceed4-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ceed4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ceed4-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="ceed4-117">-Asn</span></span>
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

### <span data-ttu-id="ceed4-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ceed4-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="ceed4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceed4-119">-DefaultProfile</span></span>
<span data-ttu-id="ceed4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceed4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceed4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ceed4-121">-Force</span></span>
<span data-ttu-id="ceed4-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceed4-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ceed4-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="ceed4-123">-Fqdn</span></span>
<span data-ttu-id="ceed4-124">Полное доменное имя шлюза локальной сети.</span><span class="sxs-lookup"><span data-stu-id="ceed4-124">FQDN of local network gateway.</span></span>

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

### <span data-ttu-id="ceed4-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="ceed4-125">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="ceed4-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ceed4-126">-Location</span></span>
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

### <span data-ttu-id="ceed4-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ceed4-127">-Name</span></span>
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

### <span data-ttu-id="ceed4-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ceed4-128">-PeerWeight</span></span>
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

### <span data-ttu-id="ceed4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceed4-129">-ResourceGroupName</span></span>
<span data-ttu-id="ceed4-130">Указывает группу ресурсов, к которой относится шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="ceed4-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="ceed4-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="ceed4-131">-Tag</span></span>
<span data-ttu-id="ceed4-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="ceed4-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ceed4-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="ceed4-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ceed4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceed4-134">-Confirm</span></span>
<span data-ttu-id="ceed4-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ceed4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceed4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceed4-136">-WhatIf</span></span>
<span data-ttu-id="ceed4-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ceed4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceed4-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ceed4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceed4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceed4-139">CommonParameters</span></span>
<span data-ttu-id="ceed4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceed4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceed4-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ceed4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceed4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceed4-142">INPUTS</span></span>

### <span data-ttu-id="ceed4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ceed4-143">System.String</span></span>

### <span data-ttu-id="ceed4-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="ceed4-144">System.String[]</span></span>

### <span data-ttu-id="ceed4-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="ceed4-145">System.UInt32</span></span>

### <span data-ttu-id="ceed4-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ceed4-146">System.Int32</span></span>

### <span data-ttu-id="ceed4-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ceed4-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ceed4-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceed4-148">OUTPUTS</span></span>

### <span data-ttu-id="ceed4-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ceed4-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ceed4-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceed4-150">NOTES</span></span>

## <span data-ttu-id="ceed4-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceed4-151">RELATED LINKS</span></span>

[<span data-ttu-id="ceed4-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ceed4-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ceed4-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ceed4-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="ceed4-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ceed4-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
