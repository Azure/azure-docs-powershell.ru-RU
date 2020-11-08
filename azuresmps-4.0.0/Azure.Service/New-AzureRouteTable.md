---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075989"
---
# <span data-ttu-id="8d77e-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d77e-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="8d77e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d77e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d77e-103">Создание таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8d77e-103">Creates a route table.</span></span>

## <span data-ttu-id="8d77e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d77e-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d77e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d77e-105">DESCRIPTION</span></span>
<span data-ttu-id="8d77e-106">Командлет **New-AzureRouteTable** создает таблицу маршрутов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="8d77e-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="8d77e-107">Вы можете добавить пользовательские маршруты к таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8d77e-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="8d77e-108">Таблицу маршрутов можно связать с подсетью в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8d77e-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="8d77e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d77e-109">EXAMPLES</span></span>

## <span data-ttu-id="8d77e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d77e-110">PARAMETERS</span></span>

### <span data-ttu-id="8d77e-111">-Label</span><span class="sxs-lookup"><span data-stu-id="8d77e-111">-Label</span></span>
<span data-ttu-id="8d77e-112">Задает описание новой таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8d77e-112">Specifies a description for the new route table.</span></span>

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

### <span data-ttu-id="8d77e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8d77e-113">-Location</span></span>
<span data-ttu-id="8d77e-114">Указывает расположение, в котором этот командлет создает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8d77e-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="8d77e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d77e-115">-Name</span></span>
<span data-ttu-id="8d77e-116">Указывает имя таблицы маршрутов, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8d77e-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8d77e-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="8d77e-117">-Profile</span></span>
<span data-ttu-id="8d77e-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8d77e-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8d77e-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d77e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d77e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d77e-120">CommonParameters</span></span>
<span data-ttu-id="8d77e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d77e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d77e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d77e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d77e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d77e-123">INPUTS</span></span>

## <span data-ttu-id="8d77e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d77e-124">OUTPUTS</span></span>

## <span data-ttu-id="8d77e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d77e-125">NOTES</span></span>

## <span data-ttu-id="8d77e-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d77e-126">RELATED LINKS</span></span>

[<span data-ttu-id="8d77e-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d77e-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="8d77e-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d77e-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


