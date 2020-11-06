---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562799"
---
# <span data-ttu-id="8764c-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8764c-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8764c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8764c-102">SYNOPSIS</span></span>
<span data-ttu-id="8764c-103">Удаление настраиваемой политики IPSec VPN, установленной на ресурсе шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8764c-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8764c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8764c-104">SYNTAX</span></span>

### <span data-ttu-id="8764c-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8764c-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8764c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8764c-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8764c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8764c-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8764c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8764c-108">DESCRIPTION</span></span>
<span data-ttu-id="8764c-109">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="8764c-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8764c-110">Командлет **Remove-AzureRmVpnClientIpsecParameter** удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, который в свою очередь задает политику IPSec по умолчанию для VPN-шлюза на основе имени VirtualNetworkGateway и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8764c-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="8764c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8764c-111">EXAMPLES</span></span>

### <span data-ttu-id="8764c-112">1: удаление параметров VPN-IPSec, заданных для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8764c-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="8764c-113">Удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="8764c-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="8764c-114">Эта команда возвращает логический объект, который отображается, если удаление прошло успешно или завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="8764c-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="8764c-115">Примечание. в результате будет задана политика IPSec по умолчанию для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8764c-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="8764c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8764c-116">PARAMETERS</span></span>

### <span data-ttu-id="8764c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8764c-117">-DefaultProfile</span></span>
<span data-ttu-id="8764c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8764c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8764c-119">-InputObject</span></span>
<span data-ttu-id="8764c-120">Объект Gateaway виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8764c-120">The virtual network gateaway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8764c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8764c-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8764c-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8764c-123">-ResourceId</span></span>
<span data-ttu-id="8764c-124">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8764c-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8764c-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8764c-126">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8764c-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8764c-127">-Confirm</span></span>
<span data-ttu-id="8764c-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8764c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8764c-129">-WhatIf</span></span>
<span data-ttu-id="8764c-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8764c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8764c-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8764c-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8764c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8764c-132">CommonParameters</span></span>
<span data-ttu-id="8764c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8764c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8764c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8764c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8764c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8764c-135">INPUTS</span></span>

### <span data-ttu-id="8764c-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8764c-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8764c-137">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8764c-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8764c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8764c-138">System.String</span></span>

## <span data-ttu-id="8764c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8764c-139">OUTPUTS</span></span>

### <span data-ttu-id="8764c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8764c-140">System.Boolean</span></span>

## <span data-ttu-id="8764c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8764c-141">NOTES</span></span>

## <span data-ttu-id="8764c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8764c-142">RELATED LINKS</span></span>
