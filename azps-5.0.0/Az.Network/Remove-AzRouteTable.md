---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246883"
---
# <span data-ttu-id="8ead1-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ead1-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="8ead1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ead1-102">SYNOPSIS</span></span>
<span data-ttu-id="8ead1-103">Удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8ead1-103">Removes a route table.</span></span>

## <span data-ttu-id="8ead1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ead1-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ead1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ead1-105">DESCRIPTION</span></span>
<span data-ttu-id="8ead1-106">Командлет **Remove-AzRouteTable** удаляет таблицу маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="8ead1-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="8ead1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ead1-107">EXAMPLES</span></span>

### <span data-ttu-id="8ead1-108">Пример 1: удаление таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="8ead1-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="8ead1-109">Эта команда удаляет таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8ead1-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="8ead1-110">Перед удалением таблицы командлет запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8ead1-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="8ead1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ead1-111">PARAMETERS</span></span>

### <span data-ttu-id="8ead1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ead1-112">-AsJob</span></span>
<span data-ttu-id="8ead1-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8ead1-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ead1-114">-DefaultProfile</span></span>
<span data-ttu-id="8ead1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ead1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8ead1-116">-Force</span></span>
<span data-ttu-id="8ead1-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ead1-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ead1-118">-Name</span></span>
<span data-ttu-id="8ead1-119">Указывает имя таблицы маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8ead1-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ead1-120">-PassThru</span></span>
<span data-ttu-id="8ead1-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8ead1-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ead1-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8ead1-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ead1-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ead1-124">Указывает имя группы ресурсов, содержащей таблицу маршрутов, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8ead1-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ead1-125">-Confirm</span></span>
<span data-ttu-id="8ead1-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ead1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ead1-127">-WhatIf</span></span>
<span data-ttu-id="8ead1-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ead1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ead1-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ead1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ead1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ead1-130">CommonParameters</span></span>
<span data-ttu-id="8ead1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ead1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ead1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ead1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ead1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ead1-133">INPUTS</span></span>

### <span data-ttu-id="8ead1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8ead1-134">System.String</span></span>

## <span data-ttu-id="8ead1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ead1-135">OUTPUTS</span></span>

### <span data-ttu-id="8ead1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ead1-136">System.Boolean</span></span>

## <span data-ttu-id="8ead1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ead1-137">NOTES</span></span>

## <span data-ttu-id="8ead1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ead1-138">RELATED LINKS</span></span>

[<span data-ttu-id="8ead1-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ead1-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="8ead1-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ead1-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="8ead1-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ead1-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


