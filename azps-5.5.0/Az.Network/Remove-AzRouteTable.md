---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227529"
---
# <span data-ttu-id="2db84-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db84-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="2db84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db84-102">SYNOPSIS</span></span>
<span data-ttu-id="2db84-103">Удаляет таблицу маршрутов.</span><span class="sxs-lookup"><span data-stu-id="2db84-103">Removes a route table.</span></span>

## <span data-ttu-id="2db84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2db84-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db84-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2db84-105">DESCRIPTION</span></span>
<span data-ttu-id="2db84-106">При этом таблица маршрутов Azure удаляется с использованием **cmdlet Remove-AzRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="2db84-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="2db84-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2db84-107">EXAMPLES</span></span>

### <span data-ttu-id="2db84-108">Пример 1. Удаление таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="2db84-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2db84-109">Эта команда удаляет таблицу маршрутов с именем RouteTable01 в группе ресурсов "Группа ресурсов11".</span><span class="sxs-lookup"><span data-stu-id="2db84-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="2db84-110">Перед удалением таблицы будет предложено подтвердить удаление.</span><span class="sxs-lookup"><span data-stu-id="2db84-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="2db84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db84-111">PARAMETERS</span></span>

### <span data-ttu-id="2db84-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2db84-112">-AsJob</span></span>
<span data-ttu-id="2db84-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2db84-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2db84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db84-114">-DefaultProfile</span></span>
<span data-ttu-id="2db84-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2db84-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2db84-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2db84-116">-Force</span></span>
<span data-ttu-id="2db84-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2db84-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2db84-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2db84-118">-Name</span></span>
<span data-ttu-id="2db84-119">Указывает имя таблицы маршрутов, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2db84-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2db84-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2db84-120">-PassThru</span></span>
<span data-ttu-id="2db84-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2db84-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2db84-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2db84-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2db84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db84-123">-ResourceGroupName</span></span>
<span data-ttu-id="2db84-124">Имя группы ресурсов, которая содержит таблицу маршрутов, удаляемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2db84-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2db84-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2db84-125">-Confirm</span></span>
<span data-ttu-id="2db84-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2db84-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db84-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db84-127">-WhatIf</span></span>
<span data-ttu-id="2db84-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2db84-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db84-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2db84-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db84-130">CommonParameters</span></span>
<span data-ttu-id="2db84-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db84-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db84-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db84-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2db84-133">INPUTS</span></span>

### <span data-ttu-id="2db84-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2db84-134">System.String</span></span>

## <span data-ttu-id="2db84-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2db84-135">OUTPUTS</span></span>

### <span data-ttu-id="2db84-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2db84-136">System.Boolean</span></span>

## <span data-ttu-id="2db84-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2db84-137">NOTES</span></span>

## <span data-ttu-id="2db84-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2db84-138">RELATED LINKS</span></span>

[<span data-ttu-id="2db84-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db84-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="2db84-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db84-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="2db84-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db84-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


