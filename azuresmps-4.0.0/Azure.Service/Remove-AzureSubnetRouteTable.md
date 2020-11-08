---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076456"
---
# <span data-ttu-id="23148-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="23148-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="23148-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23148-102">SYNOPSIS</span></span>
<span data-ttu-id="23148-103">Удаляет связь между таблицами маршрутов из подсети.</span><span class="sxs-lookup"><span data-stu-id="23148-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="23148-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23148-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23148-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23148-105">DESCRIPTION</span></span>
<span data-ttu-id="23148-106">Командлет **Remove-AzureSubnetRouteTable** удаляет связь между таблицами маршрутов из подсети.</span><span class="sxs-lookup"><span data-stu-id="23148-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="23148-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23148-107">EXAMPLES</span></span>

### <span data-ttu-id="23148-108">Пример 1: Удаление связи между таблицей маршрутов и подсетью</span><span class="sxs-lookup"><span data-stu-id="23148-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="23148-109">Эта команда удаляет связь таблицы маршрутов с именем PublicRouteTable и подсети с именем ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="23148-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="23148-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23148-110">PARAMETERS</span></span>

### <span data-ttu-id="23148-111">-Force</span><span class="sxs-lookup"><span data-stu-id="23148-111">-Force</span></span>
<span data-ttu-id="23148-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="23148-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23148-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23148-113">-PassThru</span></span>
<span data-ttu-id="23148-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="23148-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="23148-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="23148-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23148-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="23148-116">-Profile</span></span>
<span data-ttu-id="23148-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23148-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="23148-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23148-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23148-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="23148-119">-SubnetName</span></span>
<span data-ttu-id="23148-120">Указывает подсеть, для которой этот командлет удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="23148-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="23148-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="23148-121">-VirtualNetworkName</span></span>
<span data-ttu-id="23148-122">Указывает имя виртуальной сети, содержащей подсеть, для которой этот командлет удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="23148-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="23148-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23148-123">CommonParameters</span></span>
<span data-ttu-id="23148-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23148-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23148-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23148-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23148-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23148-126">INPUTS</span></span>

## <span data-ttu-id="23148-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23148-127">OUTPUTS</span></span>

## <span data-ttu-id="23148-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="23148-128">NOTES</span></span>

## <span data-ttu-id="23148-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23148-129">RELATED LINKS</span></span>

[<span data-ttu-id="23148-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="23148-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="23148-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="23148-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


