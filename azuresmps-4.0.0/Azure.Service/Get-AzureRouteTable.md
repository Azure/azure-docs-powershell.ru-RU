---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076313"
---
# <span data-ttu-id="a2452-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2452-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="a2452-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2452-102">SYNOPSIS</span></span>
<span data-ttu-id="a2452-103">Возвращает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a2452-103">Gets a route table.</span></span>

## <span data-ttu-id="a2452-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2452-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2452-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2452-105">DESCRIPTION</span></span>
<span data-ttu-id="a2452-106">Командлет **Get-AzureRouteTable** получает таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a2452-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="a2452-107">Укажите *подробный* параметр для списка маршрутов в таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a2452-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="a2452-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2452-108">EXAMPLES</span></span>

### <span data-ttu-id="a2452-109">Пример 1: получение сведений о таблице маршрутов</span><span class="sxs-lookup"><span data-stu-id="a2452-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="a2452-110">Эта команда получает сведения о таблице маршрутов с именем ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a2452-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="a2452-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2452-111">PARAMETERS</span></span>

### <span data-ttu-id="a2452-112">-Подробно</span><span class="sxs-lookup"><span data-stu-id="a2452-112">-Detailed</span></span>
<span data-ttu-id="a2452-113">Указывает на то, что этот командлет отображает маршруты в таблице маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a2452-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="a2452-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2452-114">-Name</span></span>
<span data-ttu-id="a2452-115">Указывает имя таблицы маршрутов, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2452-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a2452-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="a2452-116">-Profile</span></span>
<span data-ttu-id="a2452-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2452-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a2452-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2452-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2452-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2452-119">CommonParameters</span></span>
<span data-ttu-id="a2452-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2452-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2452-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2452-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2452-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2452-122">INPUTS</span></span>

## <span data-ttu-id="a2452-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2452-123">OUTPUTS</span></span>

## <span data-ttu-id="a2452-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2452-124">NOTES</span></span>

## <span data-ttu-id="a2452-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2452-125">RELATED LINKS</span></span>

[<span data-ttu-id="a2452-126">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2452-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="a2452-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2452-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


