---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244812"
---
# <span data-ttu-id="031ef-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="031ef-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="031ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="031ef-102">SYNOPSIS</span></span>
<span data-ttu-id="031ef-103">Создание Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="031ef-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="031ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="031ef-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="031ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="031ef-105">DESCRIPTION</span></span>
<span data-ttu-id="031ef-106">Командлет **New-AzVirtualRouter** создает Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="031ef-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="031ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="031ef-107">EXAMPLES</span></span>

### <span data-ttu-id="031ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="031ef-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="031ef-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="031ef-109">PARAMETERS</span></span>

### <span data-ttu-id="031ef-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="031ef-110">-AsJob</span></span>
<span data-ttu-id="031ef-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="031ef-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="031ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031ef-112">-DefaultProfile</span></span>
<span data-ttu-id="031ef-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="031ef-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="031ef-114">-Force</span><span class="sxs-lookup"><span data-stu-id="031ef-114">-Force</span></span>
<span data-ttu-id="031ef-115">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="031ef-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="031ef-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="031ef-116">-HostedSubnet</span></span>
<span data-ttu-id="031ef-117">Подсеть, в которой размещен виртуальный маршрутизатор.</span><span class="sxs-lookup"><span data-stu-id="031ef-117">The subnet where the virtual router is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031ef-118">-Location</span><span class="sxs-lookup"><span data-stu-id="031ef-118">-Location</span></span>
<span data-ttu-id="031ef-119">Расположение.</span><span class="sxs-lookup"><span data-stu-id="031ef-119">The location.</span></span>

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

### <span data-ttu-id="031ef-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="031ef-120">-Name</span></span>
<span data-ttu-id="031ef-121">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="031ef-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="031ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="031ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="031ef-123">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="031ef-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="031ef-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="031ef-124">-Tag</span></span>
<span data-ttu-id="031ef-125">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="031ef-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031ef-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="031ef-126">-Confirm</span></span>
<span data-ttu-id="031ef-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="031ef-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="031ef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="031ef-128">-WhatIf</span></span>
<span data-ttu-id="031ef-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="031ef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="031ef-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="031ef-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="031ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031ef-131">CommonParameters</span></span>
<span data-ttu-id="031ef-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="031ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031ef-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="031ef-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031ef-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="031ef-134">INPUTS</span></span>

### <span data-ttu-id="031ef-135">System. String</span><span class="sxs-lookup"><span data-stu-id="031ef-135">System.String</span></span>

### <span data-ttu-id="031ef-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="031ef-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="031ef-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="031ef-137">OUTPUTS</span></span>

### <span data-ttu-id="031ef-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="031ef-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="031ef-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="031ef-139">NOTES</span></span>

## <span data-ttu-id="031ef-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="031ef-140">RELATED LINKS</span></span>
