---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421695"
---
# <span data-ttu-id="ad555-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="ad555-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="ad555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad555-102">SYNOPSIS</span></span>
<span data-ttu-id="ad555-103">Создает Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="ad555-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="ad555-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad555-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad555-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad555-105">DESCRIPTION</span></span>
<span data-ttu-id="ad555-106">Для **создания службы IpAllocation** в Azure создается cmdlet New-AzIpAllocation.</span><span class="sxs-lookup"><span data-stu-id="ad555-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="ad555-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad555-107">EXAMPLES</span></span>

### <span data-ttu-id="ad555-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad555-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="ad555-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ad555-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="ad555-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad555-110">PARAMETERS</span></span>

### <span data-ttu-id="ad555-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad555-111">-AsJob</span></span>
<span data-ttu-id="ad555-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ad555-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad555-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad555-113">-DefaultProfile</span></span>
<span data-ttu-id="ad555-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad555-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad555-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ad555-115">-Force</span></span>
<span data-ttu-id="ad555-116">Не спрашивайте подтверждения, если вы хотите переопреировать ресурс</span><span class="sxs-lookup"><span data-stu-id="ad555-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="ad555-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="ad555-117">-IpAllocationTag</span></span>
<span data-ttu-id="ad555-118">Теги выделения для выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="ad555-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="ad555-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="ad555-119">-IpAllocationType</span></span>
<span data-ttu-id="ad555-120">Тип выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="ad555-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad555-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="ad555-121">-IpamAllocationId</span></span>
<span data-ttu-id="ad555-122">Ipam allocation ID of the IP allocation</span><span class="sxs-lookup"><span data-stu-id="ad555-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad555-123">-Location</span><span class="sxs-lookup"><span data-stu-id="ad555-123">-Location</span></span>
<span data-ttu-id="ad555-124">расположение.</span><span class="sxs-lookup"><span data-stu-id="ad555-124">location.</span></span>

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

### <span data-ttu-id="ad555-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ad555-125">-Name</span></span>
<span data-ttu-id="ad555-126">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="ad555-126">The resource name.</span></span>

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

### <span data-ttu-id="ad555-127">-Префикс</span><span class="sxs-lookup"><span data-stu-id="ad555-127">-Prefix</span></span>
<span data-ttu-id="ad555-128">Префикс выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="ad555-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad555-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="ad555-129">-PrefixLength</span></span>
<span data-ttu-id="ad555-130">Длина префикса выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="ad555-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad555-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="ad555-131">-PrefixType</span></span>
<span data-ttu-id="ad555-132">Тип префикса выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="ad555-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad555-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad555-133">-ResourceGroupName</span></span>
<span data-ttu-id="ad555-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad555-134">The resource group name.</span></span>

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

### <span data-ttu-id="ad555-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad555-135">-Tag</span></span>
<span data-ttu-id="ad555-136">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="ad555-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ad555-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad555-137">-Confirm</span></span>
<span data-ttu-id="ad555-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad555-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad555-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad555-139">-WhatIf</span></span>
<span data-ttu-id="ad555-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad555-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad555-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad555-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad555-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad555-142">CommonParameters</span></span>
<span data-ttu-id="ad555-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad555-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad555-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad555-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad555-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad555-145">INPUTS</span></span>

### <span data-ttu-id="ad555-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ad555-146">System.String</span></span>

### <span data-ttu-id="ad555-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ad555-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ad555-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad555-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad555-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad555-149">OUTPUTS</span></span>

### <span data-ttu-id="ad555-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="ad555-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="ad555-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad555-151">NOTES</span></span>

## <span data-ttu-id="ad555-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad555-152">RELATED LINKS</span></span>
