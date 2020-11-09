---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317135"
---
# <span data-ttu-id="f1d07-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1d07-101">New-AzIpGroup</span></span>

## <span data-ttu-id="f1d07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1d07-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d07-103">Создание Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="f1d07-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="f1d07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1d07-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1d07-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1d07-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d07-106">Командлет **New-AzIpGroup** создает Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="f1d07-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="f1d07-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1d07-107">EXAMPLES</span></span>

### <span data-ttu-id="f1d07-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1d07-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="f1d07-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f1d07-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="f1d07-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1d07-110">PARAMETERS</span></span>

### <span data-ttu-id="f1d07-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1d07-111">-AsJob</span></span>
<span data-ttu-id="f1d07-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f1d07-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1d07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d07-113">-DefaultProfile</span></span>
<span data-ttu-id="f1d07-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1d07-115">-Force</span></span>
<span data-ttu-id="f1d07-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="f1d07-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f1d07-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f1d07-117">-IpAddress</span></span>
<span data-ttu-id="f1d07-118">IpAddresses, определенная в IpGroup</span><span class="sxs-lookup"><span data-stu-id="f1d07-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d07-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f1d07-119">-Location</span></span>
<span data-ttu-id="f1d07-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="f1d07-120">The location.</span></span>

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

### <span data-ttu-id="f1d07-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1d07-121">-Name</span></span>
<span data-ttu-id="f1d07-122">Имя IPGroup.</span><span class="sxs-lookup"><span data-stu-id="f1d07-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="f1d07-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d07-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1d07-124">Имя группы ресурсов для IPGroup.</span><span class="sxs-lookup"><span data-stu-id="f1d07-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="f1d07-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="f1d07-125">-Tag</span></span>
<span data-ttu-id="f1d07-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1d07-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d07-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1d07-127">-Confirm</span></span>
<span data-ttu-id="f1d07-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1d07-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d07-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d07-129">-WhatIf</span></span>
<span data-ttu-id="f1d07-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1d07-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d07-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1d07-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d07-132">CommonParameters</span></span>
<span data-ttu-id="f1d07-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1d07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d07-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1d07-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d07-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1d07-135">INPUTS</span></span>

### <span data-ttu-id="f1d07-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f1d07-136">System.String</span></span>

### <span data-ttu-id="f1d07-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1d07-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f1d07-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1d07-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1d07-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1d07-139">OUTPUTS</span></span>

### <span data-ttu-id="f1d07-140">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1d07-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="f1d07-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1d07-141">NOTES</span></span>

## <span data-ttu-id="f1d07-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1d07-142">RELATED LINKS</span></span>
