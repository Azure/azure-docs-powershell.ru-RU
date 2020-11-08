---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076052"
---
# <span data-ttu-id="d6dc5-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d6dc5-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="d6dc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dc5-103">Задает свойства виртуальной сети RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="d6dc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6dc5-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6dc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="d6dc5-106">Командлет **Set-AzureRemoteAppVNet** задает свойства виртуальной сети RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="d6dc5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6dc5-107">EXAMPLES</span></span>

### <span data-ttu-id="d6dc5-108">Пример 1: Настройка свойств виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d6dc5-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="d6dc5-109">Эта команда задает свойства виртуальной сети с именем ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="d6dc5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6dc5-110">PARAMETERS</span></span>

### <span data-ttu-id="d6dc5-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6dc5-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="d6dc5-112">Задает IPv4-адреса серверов DNS.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc5-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="d6dc5-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="d6dc5-114">Указывает адресное пространство локальной сети в нотации classes Inter-Domain Routings (CIDR).</span><span class="sxs-lookup"><span data-stu-id="d6dc5-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="d6dc5-115">Это не должно накладываться на адресное пространство виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc5-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6dc5-116">-Profile</span></span>
<span data-ttu-id="d6dc5-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6dc5-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6dc5-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="d6dc5-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="d6dc5-120">Указывает адресное пространство виртуальной сети в нотации CIDR.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="d6dc5-121">Он должен находиться в диапазоне частных IP-адресов и не может перекрывать адресное пространство локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc5-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d6dc5-122">-VNetName</span></span>
<span data-ttu-id="d6dc5-123">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="d6dc5-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6dc5-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="d6dc5-125">Указывает адрес устройства виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="d6dc5-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="d6dc5-126">Это должен быть общедоступный адрес.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dc5-127">CommonParameters</span></span>
<span data-ttu-id="d6dc5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6dc5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dc5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dc5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dc5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6dc5-130">INPUTS</span></span>

## <span data-ttu-id="d6dc5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6dc5-131">OUTPUTS</span></span>

## <span data-ttu-id="d6dc5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6dc5-132">NOTES</span></span>

## <span data-ttu-id="d6dc5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6dc5-133">RELATED LINKS</span></span>

[<span data-ttu-id="d6dc5-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d6dc5-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


