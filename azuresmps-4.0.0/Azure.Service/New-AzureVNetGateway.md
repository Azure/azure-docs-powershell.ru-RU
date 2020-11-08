---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076187"
---
# <span data-ttu-id="e17d6-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e17d6-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="e17d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e17d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e17d6-103">Создание шлюза VPN в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e17d6-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="e17d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e17d6-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e17d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e17d6-105">DESCRIPTION</span></span>
<span data-ttu-id="e17d6-106">Командлет **New-AzureVNetGateway** создает шлюз виртуальной частной сети (VPN) в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e17d6-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="e17d6-107">Вы также можете указать SKU шлюза: Default, Standard или HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="e17d6-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="e17d6-108">Вы можете указать тип: StaticRouting или DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="e17d6-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="e17d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e17d6-109">EXAMPLES</span></span>

### <span data-ttu-id="e17d6-110">Пример 1: Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e17d6-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="e17d6-111">Эта команда создает шлюз виртуальной сети для виртуальной сети с именем ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="e17d6-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="e17d6-112">Шлюз является КОНФИГУРАЦИей по умолчанию и использует динамическую маршрутизацию.</span><span class="sxs-lookup"><span data-stu-id="e17d6-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="e17d6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e17d6-113">PARAMETERS</span></span>

### <span data-ttu-id="e17d6-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="e17d6-114">-GatewaySKU</span></span>
<span data-ttu-id="e17d6-115">Указывает SKU шлюза виртуальной сети, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e17d6-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="e17d6-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e17d6-116">Valid values are:</span></span> 

- <span data-ttu-id="e17d6-117">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e17d6-117">Default</span></span> 
- <span data-ttu-id="e17d6-118">Стандартная</span><span class="sxs-lookup"><span data-stu-id="e17d6-118">Standard</span></span> 
- <span data-ttu-id="e17d6-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="e17d6-119">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17d6-120">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="e17d6-120">-GatewayType</span></span>
<span data-ttu-id="e17d6-121">Указывает тип шлюза, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e17d6-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="e17d6-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e17d6-122">Valid values are:</span></span> 

- <span data-ttu-id="e17d6-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="e17d6-123">StaticRouting</span></span> 
- <span data-ttu-id="e17d6-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="e17d6-124">DynamicRouting</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17d6-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="e17d6-125">-Profile</span></span>
<span data-ttu-id="e17d6-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e17d6-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e17d6-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e17d6-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e17d6-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e17d6-128">-VNetName</span></span>
<span data-ttu-id="e17d6-129">Указывает виртуальную сеть, в которой этот командлет добавляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e17d6-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="e17d6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17d6-130">CommonParameters</span></span>
<span data-ttu-id="e17d6-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e17d6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17d6-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17d6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17d6-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e17d6-133">INPUTS</span></span>

## <span data-ttu-id="e17d6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e17d6-134">OUTPUTS</span></span>

## <span data-ttu-id="e17d6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e17d6-135">NOTES</span></span>

## <span data-ttu-id="e17d6-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e17d6-136">RELATED LINKS</span></span>

[<span data-ttu-id="e17d6-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e17d6-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="e17d6-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e17d6-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="e17d6-139">Сброс — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e17d6-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="e17d6-140">Изменить размер — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e17d6-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="e17d6-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e17d6-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


