---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227708"
---
# <span data-ttu-id="9b657-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9b657-101">New-AzNatGateway</span></span>

## <span data-ttu-id="9b657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b657-102">SYNOPSIS</span></span>
<span data-ttu-id="9b657-103">Создайте новый ресурс NAT шлюза с свойствами Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes и SKU.</span><span class="sxs-lookup"><span data-stu-id="9b657-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="9b657-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b657-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b657-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b657-105">DESCRIPTION</span></span>
<span data-ttu-id="9b657-106">Для создания ресурса nat шлюза создается **cmdlet New-AzNatGateway.**</span><span class="sxs-lookup"><span data-stu-id="9b657-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="9b657-107">Для natgateway требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="9b657-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="9b657-108">Префикс общедоступных IP-адресов и (или) общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="9b657-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="9b657-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9b657-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="9b657-110">SKU</span><span class="sxs-lookup"><span data-stu-id="9b657-110">Sku</span></span>
- <span data-ttu-id="9b657-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b657-111">ResourceGroupName</span></span>
- <span data-ttu-id="9b657-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="9b657-112">ResourceName</span></span>
- <span data-ttu-id="9b657-113">Расположение</span><span class="sxs-lookup"><span data-stu-id="9b657-113">Location</span></span>

## <span data-ttu-id="9b657-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b657-114">EXAMPLES</span></span>

### <span data-ttu-id="9b657-115">Пример 1. Создание шлюза NAT с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="9b657-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="9b657-116">Пример 2. Создание шлюза NAT с префиксом "Общедоступный IP-адрес"</span><span class="sxs-lookup"><span data-stu-id="9b657-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="9b657-117">Пример 3. Создание шлюза Nat с общедоступным IP-адресом в зоне доступности 1</span><span class="sxs-lookup"><span data-stu-id="9b657-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="9b657-118">Первая команда создает стандартный общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9b657-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="9b657-119">Вторая команда создает шлюз NAT с общедоступным IP-адресом в зоне доступности 1.</span><span class="sxs-lookup"><span data-stu-id="9b657-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="9b657-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b657-120">PARAMETERS</span></span>

### <span data-ttu-id="9b657-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b657-121">-AsJob</span></span>
<span data-ttu-id="9b657-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9b657-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b657-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b657-123">-DefaultProfile</span></span>
<span data-ttu-id="9b657-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b657-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b657-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9b657-125">-Force</span></span>
<span data-ttu-id="9b657-126">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="9b657-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9b657-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9b657-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9b657-128">Время ожидания неавратного времени ожидания шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="9b657-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-129">-Location</span><span class="sxs-lookup"><span data-stu-id="9b657-129">-Location</span></span>
<span data-ttu-id="9b657-130">Расположение.</span><span class="sxs-lookup"><span data-stu-id="9b657-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9b657-131">-Name</span></span>
<span data-ttu-id="9b657-132">Имя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="9b657-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b657-133">-PublicIpAddress</span></span>
<span data-ttu-id="9b657-134">Массив общедоступных IP-адресов, связанных с ресурсом nat шлюза.</span><span class="sxs-lookup"><span data-stu-id="9b657-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9b657-135">-PublicIpPrefix</span></span>
<span data-ttu-id="9b657-136">Массив общедоступных IP-префиксов, связанных с ресурсом nat шлюза.</span><span class="sxs-lookup"><span data-stu-id="9b657-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b657-137">-ResourceGroupName</span></span>
<span data-ttu-id="9b657-138">Имя группы ресурсов шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="9b657-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="9b657-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="9b657-139">-Sku</span></span>
<span data-ttu-id="9b657-140">Имя SKU шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="9b657-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b657-141">-Tag</span></span>
<span data-ttu-id="9b657-142">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="9b657-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="9b657-143">-Zone</span></span>
<span data-ttu-id="9b657-144">Список зон доступности, обозначающий зону, в которой необходимо развернуть шлюз Nat.</span><span class="sxs-lookup"><span data-stu-id="9b657-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b657-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b657-145">-Confirm</span></span>
<span data-ttu-id="9b657-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b657-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b657-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b657-147">-WhatIf</span></span>
<span data-ttu-id="9b657-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b657-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b657-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b657-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b657-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b657-150">CommonParameters</span></span>
<span data-ttu-id="9b657-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b657-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b657-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b657-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b657-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b657-153">INPUTS</span></span>

### <span data-ttu-id="9b657-154">System.String</span><span class="sxs-lookup"><span data-stu-id="9b657-154">System.String</span></span>

### <span data-ttu-id="9b657-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9b657-155">System.Int32</span></span>

### <span data-ttu-id="9b657-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b657-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9b657-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="9b657-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="9b657-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b657-158">OUTPUTS</span></span>

### <span data-ttu-id="9b657-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="9b657-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="9b657-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b657-160">NOTES</span></span>

## <span data-ttu-id="9b657-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b657-161">RELATED LINKS</span></span>
