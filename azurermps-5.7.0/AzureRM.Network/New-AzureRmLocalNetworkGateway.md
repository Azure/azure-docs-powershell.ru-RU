---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 6db2d9defaed434aa74f64d6f13af4f029edf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732730"
---
# <span data-ttu-id="43ca0-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43ca0-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="43ca0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="43ca0-103">Создание шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="43ca0-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43ca0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43ca0-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ca0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="43ca0-106">Шлюз локальной сети — это объект, представляющий локальное устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="43ca0-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="43ca0-107">Командлет **New-AzureRmLocalNetworkGateway** создает объект, представляющий локальный шлюз, на основе имени, имени группы ресурсов, расположения и IP-адреса шлюза, а также префикса адреса локальной сети, которая будет подключаться к Azure.</span><span class="sxs-lookup"><span data-stu-id="43ca0-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="43ca0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43ca0-108">EXAMPLES</span></span>

### <span data-ttu-id="43ca0-109">1: Создание шлюза локальной сети</span><span class="sxs-lookup"><span data-stu-id="43ca0-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="43ca0-110">Создает объект шлюза локальной сети с именем "myLocalGW" в группе ресурсов "myRG" в расположении "Западная часть США" с IP-адресом "23.99.221.164" и префиксом адреса "10.5.51.0/24" в локальной среде.</span><span class="sxs-lookup"><span data-stu-id="43ca0-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="43ca0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43ca0-111">PARAMETERS</span></span>

### <span data-ttu-id="43ca0-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43ca0-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43ca0-113">-AsJob</span></span>
<span data-ttu-id="43ca0-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43ca0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43ca0-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="43ca0-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="43ca0-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ca0-117">-DefaultProfile</span></span>
<span data-ttu-id="43ca0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43ca0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="43ca0-119">-Force</span></span>
<span data-ttu-id="43ca0-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="43ca0-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43ca0-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="43ca0-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-122">-Location</span><span class="sxs-lookup"><span data-stu-id="43ca0-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43ca0-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="43ca0-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ca0-125">-ResourceGroupName</span></span>
<span data-ttu-id="43ca0-126">Указывает группу ресурсов, к которой относится шлюз локальной сети.</span><span class="sxs-lookup"><span data-stu-id="43ca0-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="43ca0-127">-Tag</span></span>
<span data-ttu-id="43ca0-128">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="43ca0-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="43ca0-129">Например:</span><span class="sxs-lookup"><span data-stu-id="43ca0-129">For example:</span></span>

<span data-ttu-id="43ca0-130">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="43ca0-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43ca0-131">-Confirm</span></span>
<span data-ttu-id="43ca0-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43ca0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ca0-133">-WhatIf</span></span>
<span data-ttu-id="43ca0-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43ca0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ca0-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43ca0-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ca0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ca0-136">CommonParameters</span></span>
<span data-ttu-id="43ca0-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43ca0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ca0-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ca0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ca0-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43ca0-139">INPUTS</span></span>

### <span data-ttu-id="43ca0-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="43ca0-140">None</span></span>
<span data-ttu-id="43ca0-141">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="43ca0-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43ca0-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ca0-142">OUTPUTS</span></span>

### <span data-ttu-id="43ca0-143">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43ca0-143">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="43ca0-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="43ca0-144">NOTES</span></span>

## <span data-ttu-id="43ca0-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43ca0-145">RELATED LINKS</span></span>

[<span data-ttu-id="43ca0-146">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43ca0-146">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="43ca0-147">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43ca0-147">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="43ca0-148">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="43ca0-148">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
