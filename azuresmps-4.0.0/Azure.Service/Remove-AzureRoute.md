---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076135"
---
# <span data-ttu-id="2a6e5-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="2a6e5-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="2a6e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a6e5-103">Удаляет маршрут из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="2a6e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a6e5-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a6e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a6e5-105">DESCRIPTION</span></span>
<span data-ttu-id="2a6e5-106">Командлет **Remove-AzureRoute** удаляет маршрут из таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="2a6e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a6e5-107">EXAMPLES</span></span>

### <span data-ttu-id="2a6e5-108">Пример 1: Удаление маршрута</span><span class="sxs-lookup"><span data-stu-id="2a6e5-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="2a6e5-109">Эта команда получает таблицу маршрутов с именем ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="2a6e5-110">Команда передает эту таблицу маршрутов в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="2a6e5-111">Текущий командлет удаляет маршрут с именем InternetRoute.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="2a6e5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a6e5-112">PARAMETERS</span></span>

### <span data-ttu-id="2a6e5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2a6e5-113">-Force</span></span>
<span data-ttu-id="2a6e5-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a6e5-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="2a6e5-115">-Profile</span></span>
<span data-ttu-id="2a6e5-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2a6e5-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2a6e5-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="2a6e5-118">-RouteName</span></span>
<span data-ttu-id="2a6e5-119">Указывает имя для нового маршрута, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a6e5-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2a6e5-120">-RouteTable</span></span>
<span data-ttu-id="2a6e5-121">Указывает таблицу маршрутов, из которой этот командлет удаляет маршрут.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a6e5-122">CommonParameters</span></span>
<span data-ttu-id="2a6e5-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a6e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a6e5-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a6e5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a6e5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a6e5-125">INPUTS</span></span>

## <span data-ttu-id="2a6e5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a6e5-126">OUTPUTS</span></span>

## <span data-ttu-id="2a6e5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a6e5-127">NOTES</span></span>

## <span data-ttu-id="2a6e5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a6e5-128">RELATED LINKS</span></span>

[<span data-ttu-id="2a6e5-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="2a6e5-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


