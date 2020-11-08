---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075812"
---
# <span data-ttu-id="a4b94-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a4b94-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="a4b94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4b94-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b94-103">Связывание таблицы маршрутов с подсетью.</span><span class="sxs-lookup"><span data-stu-id="a4b94-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="a4b94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4b94-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a4b94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b94-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b94-106">Командлет **Set-AzureSubnetRouteTable** связывает таблицу маршрутов с подсетью.</span><span class="sxs-lookup"><span data-stu-id="a4b94-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="a4b94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4b94-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b94-108">Пример 1: связывание таблицы маршрутов с подсетью</span><span class="sxs-lookup"><span data-stu-id="a4b94-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="a4b94-109">Эта команда связывает таблицу маршрутов с именем PublicRouteTable и подсеть с именем ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="a4b94-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="a4b94-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4b94-110">PARAMETERS</span></span>

### <span data-ttu-id="a4b94-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4b94-111">-PassThru</span></span>
<span data-ttu-id="a4b94-112">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a4b94-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a4b94-113">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a4b94-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4b94-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="a4b94-114">-Profile</span></span>
<span data-ttu-id="a4b94-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4b94-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4b94-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4b94-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4b94-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="a4b94-117">-RouteTableName</span></span>
<span data-ttu-id="a4b94-118">Указывает имя таблицы маршрутов, которую этот командлет свяжет с подсетью.</span><span class="sxs-lookup"><span data-stu-id="a4b94-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="a4b94-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a4b94-119">-SubnetName</span></span>
<span data-ttu-id="a4b94-120">Указывает подсеть, к которой этот командлет связывает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a4b94-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="a4b94-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a4b94-121">-VirtualNetworkName</span></span>
<span data-ttu-id="a4b94-122">Указывает имя виртуальной сети, содержащей подсеть, в которую этот командлет связывает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a4b94-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="a4b94-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b94-123">CommonParameters</span></span>
<span data-ttu-id="a4b94-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4b94-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b94-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b94-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b94-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4b94-126">INPUTS</span></span>

## <span data-ttu-id="a4b94-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b94-127">OUTPUTS</span></span>

## <span data-ttu-id="a4b94-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4b94-128">NOTES</span></span>

## <span data-ttu-id="a4b94-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4b94-129">RELATED LINKS</span></span>

[<span data-ttu-id="a4b94-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a4b94-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="a4b94-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a4b94-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
