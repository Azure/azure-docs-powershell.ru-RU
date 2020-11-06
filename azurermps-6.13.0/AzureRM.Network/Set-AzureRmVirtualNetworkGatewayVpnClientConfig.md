---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562772"
---
# <span data-ttu-id="ae7a3-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="ae7a3-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="ae7a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7a3-103">Установка пула адресов VPN-клиентов для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae7a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae7a3-104">SYNTAX</span></span>

### <span data-ttu-id="ae7a3-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae7a3-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae7a3-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae7a3-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae7a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae7a3-107">DESCRIPTION</span></span>
<span data-ttu-id="ae7a3-108">Командлет **Set-AzureRmVirtualNetworkVpnClientConfig** настраивает пул клиентских адресов для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="ae7a3-109">Клиентам виртуальных частных сетей (VPN), которые подключаются к этому шлюзу, будет назначен IP-адрес из этого пула адресов.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="ae7a3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae7a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ae7a3-111">Пример 1: назначение пула адресов VPN-клиентов для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ae7a3-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="ae7a3-112">В этом примере пул адресов VPN-клиентов назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ae7a3-113">Первая команда создает ссылку на объект для шлюза, а объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ae7a3-114">Вторая команда в примере использует командлет **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** , чтобы назначить пулу адресов 10.0.0.0/16 для ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="ae7a3-115">Пример 2: Настройка проверки подлинности на основе внешней RADIUS на существующем шлюзе</span><span class="sxs-lookup"><span data-stu-id="ae7a3-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="ae7a3-116">В этом примере пул адресов VPN-клиентов назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ae7a3-117">Первая команда создает ссылку на объект для шлюза, а объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ae7a3-118">Вторая команда в примере использует командлет **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** , чтобы назначить пулу адресов 10.0.0.0/16 для ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="ae7a3-119">Кроме того, он настраивает внешний сервер RADIUS "TestRadiusServer", который будет использоваться для проверки подлинности для клиентов VPN.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="ae7a3-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae7a3-120">PARAMETERS</span></span>

### <span data-ttu-id="ae7a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7a3-121">-DefaultProfile</span></span>
<span data-ttu-id="ae7a3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae7a3-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="ae7a3-123">-RadiusServerAddress</span></span>
<span data-ttu-id="ae7a3-124">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a3-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="ae7a3-125">-RadiusServerSecret</span></span>
<span data-ttu-id="ae7a3-126">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a3-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae7a3-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ae7a3-128">Указывает ссылку на объект шлюза виртуальной сети, который содержит параметры конфигурации VPN-клиента, изменяемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="ae7a3-129">Вы можете создать ссылку на объект для шлюза виртуальной сети, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a3-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="ae7a3-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="ae7a3-131">Задает IP-адреса, назначаемые клиентам, которые подключаются к этому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7a3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae7a3-132">-Confirm</span></span>
<span data-ttu-id="ae7a3-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae7a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7a3-134">-WhatIf</span></span>
<span data-ttu-id="ae7a3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae7a3-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae7a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7a3-137">CommonParameters</span></span>
<span data-ttu-id="ae7a3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae7a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7a3-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7a3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7a3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae7a3-140">INPUTS</span></span>

### <span data-ttu-id="ae7a3-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae7a3-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ae7a3-142">Параметры: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae7a3-142">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="ae7a3-143">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ae7a3-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ae7a3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ae7a3-144">System.String</span></span>

### <span data-ttu-id="ae7a3-145">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ae7a3-145">System.Security.SecureString</span></span>

## <span data-ttu-id="ae7a3-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae7a3-146">OUTPUTS</span></span>

### <span data-ttu-id="ae7a3-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae7a3-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ae7a3-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae7a3-148">NOTES</span></span>

## <span data-ttu-id="ae7a3-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae7a3-149">RELATED LINKS</span></span>

[<span data-ttu-id="ae7a3-150">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="ae7a3-150">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="ae7a3-151">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae7a3-151">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ae7a3-152">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ae7a3-152">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


