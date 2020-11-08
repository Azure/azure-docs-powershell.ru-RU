---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236046"
---
# <span data-ttu-id="06b40-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="06b40-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="06b40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06b40-102">SYNOPSIS</span></span>
<span data-ttu-id="06b40-103">Создание Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="06b40-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="06b40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06b40-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06b40-105">DESCRIPTION</span></span>
<span data-ttu-id="06b40-106">Командлет **New-AzIpAllocation** создает Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="06b40-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="06b40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06b40-107">EXAMPLES</span></span>

### <span data-ttu-id="06b40-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06b40-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="06b40-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="06b40-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="06b40-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06b40-110">PARAMETERS</span></span>

### <span data-ttu-id="06b40-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06b40-111">-AsJob</span></span>
<span data-ttu-id="06b40-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="06b40-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06b40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b40-113">-DefaultProfile</span></span>
<span data-ttu-id="06b40-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06b40-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b40-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06b40-115">-Force</span></span>
<span data-ttu-id="06b40-116">Не запрашивать подтверждение, если вы хотите переопределить ресурс</span><span class="sxs-lookup"><span data-stu-id="06b40-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="06b40-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="06b40-117">-IpAllocationTag</span></span>
<span data-ttu-id="06b40-118">Теги выделения для IP-адреса</span><span class="sxs-lookup"><span data-stu-id="06b40-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="06b40-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="06b40-119">-IpAllocationType</span></span>
<span data-ttu-id="06b40-120">Тип выделения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="06b40-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="06b40-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="06b40-121">-IpamAllocationId</span></span>
<span data-ttu-id="06b40-122">КОД выделения IPAM для выделения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="06b40-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="06b40-123">-Location</span><span class="sxs-lookup"><span data-stu-id="06b40-123">-Location</span></span>
<span data-ttu-id="06b40-124">поиска.</span><span class="sxs-lookup"><span data-stu-id="06b40-124">location.</span></span>

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

### <span data-ttu-id="06b40-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06b40-125">-Name</span></span>
<span data-ttu-id="06b40-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="06b40-126">The resource name.</span></span>

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

### <span data-ttu-id="06b40-127">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="06b40-127">-Prefix</span></span>
<span data-ttu-id="06b40-128">Префикс выделения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="06b40-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="06b40-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="06b40-129">-PrefixLength</span></span>
<span data-ttu-id="06b40-130">Длина префикса для выделения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="06b40-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="06b40-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="06b40-131">-PrefixType</span></span>
<span data-ttu-id="06b40-132">Тип префикса выделения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="06b40-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="06b40-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b40-133">-ResourceGroupName</span></span>
<span data-ttu-id="06b40-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06b40-134">The resource group name.</span></span>

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

### <span data-ttu-id="06b40-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="06b40-135">-Tag</span></span>
<span data-ttu-id="06b40-136">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06b40-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="06b40-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06b40-137">-Confirm</span></span>
<span data-ttu-id="06b40-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06b40-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b40-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b40-139">-WhatIf</span></span>
<span data-ttu-id="06b40-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06b40-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b40-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06b40-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b40-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b40-142">CommonParameters</span></span>
<span data-ttu-id="06b40-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06b40-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b40-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b40-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b40-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06b40-145">INPUTS</span></span>

### <span data-ttu-id="06b40-146">System. String</span><span class="sxs-lookup"><span data-stu-id="06b40-146">System.String</span></span>

### <span data-ttu-id="06b40-147">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06b40-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="06b40-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06b40-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06b40-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06b40-149">OUTPUTS</span></span>

### <span data-ttu-id="06b40-150">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="06b40-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="06b40-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="06b40-151">NOTES</span></span>

## <span data-ttu-id="06b40-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06b40-152">RELATED LINKS</span></span>
