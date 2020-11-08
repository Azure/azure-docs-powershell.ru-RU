---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075542"
---
# <span data-ttu-id="f1954-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1954-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="f1954-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1954-102">SYNOPSIS</span></span>
<span data-ttu-id="f1954-103">Возвращает таблицу маршрутов для подсети.</span><span class="sxs-lookup"><span data-stu-id="f1954-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="f1954-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1954-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f1954-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1954-105">DESCRIPTION</span></span>
<span data-ttu-id="f1954-106">Командлет **Get-AzureSubnetRouteTable** получает таблицу маршрутов, связанную с подсетью.</span><span class="sxs-lookup"><span data-stu-id="f1954-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="f1954-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1954-107">EXAMPLES</span></span>

### <span data-ttu-id="f1954-108">Пример 1: отображение маршрутов для подсети</span><span class="sxs-lookup"><span data-stu-id="f1954-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="f1954-109">Эта команда отображает маршруты в имени таблицы маршрутов, связанной с подсетью с именем ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="f1954-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="f1954-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1954-110">PARAMETERS</span></span>

### <span data-ttu-id="f1954-111">-Подробно</span><span class="sxs-lookup"><span data-stu-id="f1954-111">-Detailed</span></span>
<span data-ttu-id="f1954-112">Указывает на то, что этот командлет выводит маршруты в таблице маршрутов, связанной с подсетью.</span><span class="sxs-lookup"><span data-stu-id="f1954-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="f1954-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="f1954-113">-Profile</span></span>
<span data-ttu-id="f1954-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f1954-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f1954-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1954-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1954-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f1954-116">-SubnetName</span></span>
<span data-ttu-id="f1954-117">Указывает подсеть, для которой этот командлет получает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f1954-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="f1954-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f1954-118">-VirtualNetworkName</span></span>
<span data-ttu-id="f1954-119">Указывает имя виртуальной сети, содержащей подсеть, для которой этот командлет получает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f1954-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="f1954-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1954-120">CommonParameters</span></span>
<span data-ttu-id="f1954-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1954-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1954-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1954-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1954-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1954-123">INPUTS</span></span>

## <span data-ttu-id="f1954-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1954-124">OUTPUTS</span></span>

## <span data-ttu-id="f1954-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1954-125">NOTES</span></span>

## <span data-ttu-id="f1954-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1954-126">RELATED LINKS</span></span>

[<span data-ttu-id="f1954-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1954-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="f1954-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1954-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


