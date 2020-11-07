---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: f78b888e75db758f254924dee9fbf501050717b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915078"
---
# <span data-ttu-id="69394-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="69394-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="69394-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69394-102">SYNOPSIS</span></span>
<span data-ttu-id="69394-103">Удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="69394-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69394-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69394-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69394-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69394-105">DESCRIPTION</span></span>
<span data-ttu-id="69394-106">Командлет **Remove-AzureRmRouteTable** удаляет таблицу маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="69394-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="69394-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69394-107">EXAMPLES</span></span>

### <span data-ttu-id="69394-108">Пример 1: удаление таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="69394-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="69394-109">Эта команда удаляет таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="69394-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="69394-110">Перед удалением таблицы командлет запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="69394-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="69394-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69394-111">PARAMETERS</span></span>

### <span data-ttu-id="69394-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69394-112">-AsJob</span></span>
<span data-ttu-id="69394-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="69394-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69394-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69394-114">-DefaultProfile</span></span>
<span data-ttu-id="69394-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69394-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69394-116">-Force</span><span class="sxs-lookup"><span data-stu-id="69394-116">-Force</span></span>
<span data-ttu-id="69394-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="69394-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69394-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69394-118">-Name</span></span>
<span data-ttu-id="69394-119">Указывает имя таблицы маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69394-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69394-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69394-120">-PassThru</span></span>
<span data-ttu-id="69394-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="69394-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69394-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="69394-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69394-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69394-123">-ResourceGroupName</span></span>
<span data-ttu-id="69394-124">Указывает имя группы ресурсов, содержащей таблицу маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69394-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69394-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69394-125">-Confirm</span></span>
<span data-ttu-id="69394-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="69394-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69394-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69394-127">-WhatIf</span></span>
<span data-ttu-id="69394-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="69394-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69394-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69394-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69394-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69394-130">CommonParameters</span></span>
<span data-ttu-id="69394-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69394-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69394-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69394-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69394-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69394-133">INPUTS</span></span>

## <span data-ttu-id="69394-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69394-134">OUTPUTS</span></span>

## <span data-ttu-id="69394-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="69394-135">NOTES</span></span>

## <span data-ttu-id="69394-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69394-136">RELATED LINKS</span></span>

[<span data-ttu-id="69394-137">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="69394-137">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="69394-138">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="69394-138">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="69394-139">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="69394-139">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


