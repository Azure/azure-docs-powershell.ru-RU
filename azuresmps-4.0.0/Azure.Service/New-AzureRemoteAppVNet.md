---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075994"
---
# <span data-ttu-id="a5870-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a5870-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="a5870-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5870-102">SYNOPSIS</span></span>
<span data-ttu-id="a5870-103">Создает виртуальную сеть RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="a5870-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="a5870-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5870-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a5870-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5870-105">DESCRIPTION</span></span>
<span data-ttu-id="a5870-106">Командлет **New-AzureRemoteAppVNet** создает виртуальную сеть RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="a5870-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="a5870-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5870-107">EXAMPLES</span></span>

### <span data-ttu-id="a5870-108">Пример 1: создание виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a5870-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="a5870-109">Эта команда создает виртуальную сеть с именем ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="a5870-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="a5870-110">Чтобы определить состояние операции, используйте командлет **Get-AzureRemoteAppOperationResult** с идентификатором отслеживания, возвращаемым этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a5870-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="a5870-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5870-111">PARAMETERS</span></span>

### <span data-ttu-id="a5870-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5870-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="a5870-113">Задает массив IPv4-адресов серверов DNS.</span><span class="sxs-lookup"><span data-stu-id="a5870-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-114">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="a5870-114">-GatewayType</span></span>
<span data-ttu-id="a5870-115">Указывает тип маршрутизации шлюза для использования.</span><span class="sxs-lookup"><span data-stu-id="a5870-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="a5870-116">Допустимые значения этого параметра: StaticRouting или DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="a5870-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="a5870-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="a5870-118">Задает массив строк, задающих адресное пространство локальной сети (в нотации CIDR междоменной маршрутизации).</span><span class="sxs-lookup"><span data-stu-id="a5870-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="a5870-119">Это адресное пространство не должно пересекаться с адресным пространством виртуальной сети, которое указывает параметр *VirtualNetworkAddressSpace* .</span><span class="sxs-lookup"><span data-stu-id="a5870-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a5870-120">-Location</span></span>
<span data-ttu-id="a5870-121">Задает расположение, в котором нужно создать виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a5870-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="a5870-122">-Profile</span></span>
<span data-ttu-id="a5870-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a5870-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5870-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5870-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="a5870-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="a5870-126">Задает массив строк, указывающий адресное пространство виртуальной сети в нотации CIDR.</span><span class="sxs-lookup"><span data-stu-id="a5870-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="a5870-127">Это значение должно находиться в диапазоне частных IP-адресов и не может перекрываться с адресным пространством локальной сети, которое указывает параметр *LocalNetworkAddressSpace* .</span><span class="sxs-lookup"><span data-stu-id="a5870-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a5870-128">-VNetName</span></span>
<span data-ttu-id="a5870-129">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="a5870-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5870-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="a5870-131">Указывает адрес устройства виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="a5870-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="a5870-132">Это должен быть общедоступный адрес.</span><span class="sxs-lookup"><span data-stu-id="a5870-132">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5870-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5870-133">CommonParameters</span></span>
<span data-ttu-id="a5870-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5870-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5870-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5870-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5870-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5870-136">INPUTS</span></span>

## <span data-ttu-id="a5870-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5870-137">OUTPUTS</span></span>

## <span data-ttu-id="a5870-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5870-138">NOTES</span></span>

## <span data-ttu-id="a5870-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5870-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5870-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="a5870-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="a5870-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a5870-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="a5870-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a5870-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="a5870-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a5870-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


