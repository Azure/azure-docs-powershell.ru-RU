---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076414"
---
# <span data-ttu-id="b2d17-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b2d17-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="b2d17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2d17-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d17-103">Включение или отключение VPN-шлюза для виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d17-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="b2d17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2d17-104">SYNTAX</span></span>

### <span data-ttu-id="b2d17-105">Connect (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2d17-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2d17-106">Соединения</span><span class="sxs-lookup"><span data-stu-id="b2d17-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2d17-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2d17-107">DESCRIPTION</span></span>
<span data-ttu-id="b2d17-108">Командлет **Set-AzureVNetGateway** включает или отключает шлюз виртуальной частной сети (VPN) для виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d17-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="b2d17-109">Шлюз виртуальной сети — это конечная точка VPN для подключения к виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2d17-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="b2d17-110">Укажите параметр *подключения* или *отключения* , чтобы включить или отключить VPN-подключение между локальным сайтом локальной сети и виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="b2d17-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="b2d17-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2d17-111">EXAMPLES</span></span>

### <span data-ttu-id="b2d17-112">Пример 1: Включение шлюза виртуальной сети для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b2d17-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="b2d17-113">Эта команда включает шлюз виртуальной сети между виртуальной сетью Azure с именем ContosoProdNet и VPN-устройством для сайта локальной сети с именем ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="b2d17-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="b2d17-114">Пример 2: Отключение шлюза виртуальной сети для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b2d17-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="b2d17-115">Эта команда отключает шлюз виртуальной сети между виртуальной сетью Azure с именем ContosoProdNet и VPN-устройством для сайта локальной сети с именем ContosoBranchOffice.</span><span class="sxs-lookup"><span data-stu-id="b2d17-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="b2d17-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2d17-116">PARAMETERS</span></span>

### <span data-ttu-id="b2d17-117">-Connect</span><span class="sxs-lookup"><span data-stu-id="b2d17-117">-Connect</span></span>
<span data-ttu-id="b2d17-118">Указывает на то, что этот командлет разрешает VPN-подключение между виртуальной сетью и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2d17-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d17-119">-Отключение</span><span class="sxs-lookup"><span data-stu-id="b2d17-119">-Disconnect</span></span>
<span data-ttu-id="b2d17-120">Указывает, что этот командлет отключает VPN-подключение между виртуальной сетью и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2d17-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d17-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="b2d17-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="b2d17-122">Задает имя локального сайта локальной сети, для которого этот командлет включит или отключит VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="b2d17-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d17-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="b2d17-123">-Profile</span></span>
<span data-ttu-id="b2d17-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b2d17-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b2d17-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2d17-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2d17-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b2d17-126">-VNetName</span></span>
<span data-ttu-id="b2d17-127">Указывает виртуальную сеть, для которой этот командлет включит или отключит VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="b2d17-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d17-128">CommonParameters</span></span>
<span data-ttu-id="b2d17-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2d17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d17-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d17-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d17-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2d17-131">INPUTS</span></span>

## <span data-ttu-id="b2d17-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2d17-132">OUTPUTS</span></span>

## <span data-ttu-id="b2d17-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2d17-133">NOTES</span></span>

## <span data-ttu-id="b2d17-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2d17-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2d17-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b2d17-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="b2d17-136">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b2d17-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="b2d17-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b2d17-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="b2d17-138">Сброс — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b2d17-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="b2d17-139">Изменить размер — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="b2d17-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


