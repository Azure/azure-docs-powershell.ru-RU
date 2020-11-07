---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: ddd1ab1ce748def345604447988d0fc53b5989fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734170"
---
# <span data-ttu-id="0d86e-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d86e-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="0d86e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d86e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d86e-103">Удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0d86e-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d86e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d86e-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d86e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d86e-105">DESCRIPTION</span></span>
<span data-ttu-id="0d86e-106">Командлет **Remove-AzureRmRouteTable** удаляет таблицу маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="0d86e-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="0d86e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d86e-107">EXAMPLES</span></span>

### <span data-ttu-id="0d86e-108">Пример 1: удаление таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="0d86e-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="0d86e-109">Эта команда удаляет таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0d86e-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="0d86e-110">Перед удалением таблицы командлет запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0d86e-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="0d86e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d86e-111">PARAMETERS</span></span>

### <span data-ttu-id="0d86e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d86e-112">-AsJob</span></span>
<span data-ttu-id="0d86e-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0d86e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d86e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d86e-114">-DefaultProfile</span></span>
<span data-ttu-id="0d86e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d86e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d86e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0d86e-116">-Force</span></span>
<span data-ttu-id="0d86e-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d86e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d86e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d86e-118">-Name</span></span>
<span data-ttu-id="0d86e-119">Указывает имя таблицы маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d86e-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d86e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d86e-120">-PassThru</span></span>
<span data-ttu-id="0d86e-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0d86e-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d86e-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0d86e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d86e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d86e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d86e-124">Указывает имя группы ресурсов, содержащей таблицу маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d86e-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d86e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d86e-125">-Confirm</span></span>
<span data-ttu-id="0d86e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d86e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d86e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d86e-127">-WhatIf</span></span>
<span data-ttu-id="0d86e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d86e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d86e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d86e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d86e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d86e-130">CommonParameters</span></span>
<span data-ttu-id="0d86e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d86e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d86e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d86e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d86e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d86e-133">INPUTS</span></span>

### <span data-ttu-id="0d86e-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="0d86e-134">None</span></span>
<span data-ttu-id="0d86e-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0d86e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d86e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d86e-136">OUTPUTS</span></span>

## <span data-ttu-id="0d86e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d86e-137">NOTES</span></span>

## <span data-ttu-id="0d86e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d86e-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d86e-139">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d86e-139">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="0d86e-140">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d86e-140">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="0d86e-141">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d86e-141">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


