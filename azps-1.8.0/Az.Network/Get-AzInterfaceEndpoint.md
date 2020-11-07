---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730563"
---
# <span data-ttu-id="ae80b-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae80b-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="ae80b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae80b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae80b-103">Командлет Get-AzInterfaceEndpoint получает конечную точку интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae80b-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="ae80b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae80b-104">SYNTAX</span></span>

### <span data-ttu-id="ae80b-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae80b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae80b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae80b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae80b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae80b-107">DESCRIPTION</span></span>
<span data-ttu-id="ae80b-108">Командлет **Get-AzInterfaceEndpoint** получает конечную точку интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae80b-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="ae80b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae80b-109">EXAMPLES</span></span>

### <span data-ttu-id="ae80b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae80b-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ae80b-111">Эта команда получает конечную точку интерфейса с именем InterfaceEndpoint1, которая относится к группе ресурсов с именем ResourceGroup01, и сохраняет ее в переменной $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="ae80b-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="ae80b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ae80b-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="ae80b-113">Эта команда получает конечную точку интерфейса с resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 и сохраняет ее в переменной $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="ae80b-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="ae80b-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ae80b-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="ae80b-115">Эта команда получает конечные точки интерфейса, которые начинаются с "InterfaceEndpoint".</span><span class="sxs-lookup"><span data-stu-id="ae80b-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="ae80b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae80b-116">PARAMETERS</span></span>

### <span data-ttu-id="ae80b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae80b-117">-DefaultProfile</span></span>
<span data-ttu-id="ae80b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae80b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae80b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae80b-119">-Name</span></span>
<span data-ttu-id="ae80b-120">Имя конечной точки интерфейса</span><span class="sxs-lookup"><span data-stu-id="ae80b-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ae80b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae80b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae80b-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae80b-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae80b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae80b-123">-ResourceId</span></span>
<span data-ttu-id="ae80b-124">Идентификатор конечной точки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae80b-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae80b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae80b-125">-Confirm</span></span>
<span data-ttu-id="ae80b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae80b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae80b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae80b-127">-WhatIf</span></span>
<span data-ttu-id="ae80b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae80b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae80b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae80b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae80b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae80b-130">CommonParameters</span></span>
<span data-ttu-id="ae80b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae80b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae80b-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae80b-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae80b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae80b-133">INPUTS</span></span>

### <span data-ttu-id="ae80b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ae80b-134">System.String</span></span>

## <span data-ttu-id="ae80b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae80b-135">OUTPUTS</span></span>

### <span data-ttu-id="ae80b-136">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae80b-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="ae80b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae80b-137">NOTES</span></span>

## <span data-ttu-id="ae80b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae80b-138">RELATED LINKS</span></span>
