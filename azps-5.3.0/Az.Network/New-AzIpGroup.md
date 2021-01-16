---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507881"
---
# <span data-ttu-id="f1bfa-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1bfa-101">New-AzIpGroup</span></span>

## <span data-ttu-id="f1bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="f1bfa-103">Создает IpGroup Azure.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="f1bfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1bfa-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1bfa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="f1bfa-106">Для **создания ipGroup** создается новая группа Azure AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="f1bfa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1bfa-107">EXAMPLES</span></span>

### <span data-ttu-id="f1bfa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1bfa-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="f1bfa-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f1bfa-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="f1bfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1bfa-110">PARAMETERS</span></span>

### <span data-ttu-id="f1bfa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1bfa-111">-AsJob</span></span>
<span data-ttu-id="f1bfa-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f1bfa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1bfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1bfa-113">-DefaultProfile</span></span>
<span data-ttu-id="f1bfa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1bfa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1bfa-115">-Force</span></span>
<span data-ttu-id="f1bfa-116">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="f1bfa-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f1bfa-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f1bfa-117">-IpAddress</span></span>
<span data-ttu-id="f1bfa-118">IpAddresses, определенные в IpGroup</span><span class="sxs-lookup"><span data-stu-id="f1bfa-118">IpAddresses defined in the IpGroup</span></span>

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

### <span data-ttu-id="f1bfa-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f1bfa-119">-Location</span></span>
<span data-ttu-id="f1bfa-120">Расположение.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-120">The location.</span></span>

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

### <span data-ttu-id="f1bfa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1bfa-121">-Name</span></span>
<span data-ttu-id="f1bfa-122">Имя ipgroup.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="f1bfa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1bfa-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1bfa-124">Имя группы ресурсов ipgroup.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="f1bfa-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1bfa-125">-Tag</span></span>
<span data-ttu-id="f1bfa-126">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f1bfa-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1bfa-127">-Confirm</span></span>
<span data-ttu-id="f1bfa-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1bfa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1bfa-129">-WhatIf</span></span>
<span data-ttu-id="f1bfa-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1bfa-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1bfa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1bfa-132">CommonParameters</span></span>
<span data-ttu-id="f1bfa-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1bfa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1bfa-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1bfa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1bfa-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1bfa-135">INPUTS</span></span>

### <span data-ttu-id="f1bfa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f1bfa-136">System.String</span></span>

### <span data-ttu-id="f1bfa-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1bfa-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f1bfa-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1bfa-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1bfa-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1bfa-139">OUTPUTS</span></span>

### <span data-ttu-id="f1bfa-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1bfa-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="f1bfa-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1bfa-141">NOTES</span></span>

## <span data-ttu-id="f1bfa-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1bfa-142">RELATED LINKS</span></span>
