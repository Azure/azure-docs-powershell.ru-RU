---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400999"
---
# <span data-ttu-id="6aabc-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6aabc-101">New-AzNatGateway</span></span>

## <span data-ttu-id="6aabc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aabc-102">SYNOPSIS</span></span>
<span data-ttu-id="6aabc-103">Создайте новый ресурс NAT шлюза с свойствами Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes и SKU.</span><span class="sxs-lookup"><span data-stu-id="6aabc-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="6aabc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6aabc-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aabc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aabc-105">DESCRIPTION</span></span>
<span data-ttu-id="6aabc-106">Для создания ресурса NAT шлюза создается **cmdlet New-AzNatGateway.**</span><span class="sxs-lookup"><span data-stu-id="6aabc-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="6aabc-107">Для natgateway требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="6aabc-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="6aabc-108">Префикс общедоступных IP-адресов и (или) общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="6aabc-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="6aabc-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6aabc-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="6aabc-110">SKU</span><span class="sxs-lookup"><span data-stu-id="6aabc-110">Sku</span></span>
- <span data-ttu-id="6aabc-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aabc-111">ResourceGroupName</span></span>
- <span data-ttu-id="6aabc-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="6aabc-112">ResourceName</span></span>
- <span data-ttu-id="6aabc-113">Расположение</span><span class="sxs-lookup"><span data-stu-id="6aabc-113">Location</span></span>

## <span data-ttu-id="6aabc-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6aabc-114">EXAMPLES</span></span>

### <span data-ttu-id="6aabc-115">Пример 1. Создание шлюза NAT с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="6aabc-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="6aabc-116">Пример 2. Создание шлюза NAT с префиксом "Общедоступный IP-адрес"</span><span class="sxs-lookup"><span data-stu-id="6aabc-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="6aabc-117">Пример 3. Создание шлюза Nat с общедоступным IP-адресом в зоне доступности 1</span><span class="sxs-lookup"><span data-stu-id="6aabc-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="6aabc-118">Первая команда создает стандартный общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="6aabc-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="6aabc-119">Вторая команда создает шлюз NAT с общедоступным IP-адресом в зоне доступности 1.</span><span class="sxs-lookup"><span data-stu-id="6aabc-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="6aabc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aabc-120">PARAMETERS</span></span>

### <span data-ttu-id="6aabc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aabc-121">-AsJob</span></span>
<span data-ttu-id="6aabc-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6aabc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6aabc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aabc-123">-DefaultProfile</span></span>
<span data-ttu-id="6aabc-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aabc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aabc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6aabc-125">-Force</span></span>
<span data-ttu-id="6aabc-126">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="6aabc-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6aabc-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6aabc-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6aabc-128">Неавратное время ожидания шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6aabc-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="6aabc-129">-Location</span><span class="sxs-lookup"><span data-stu-id="6aabc-129">-Location</span></span>
<span data-ttu-id="6aabc-130">Расположение.</span><span class="sxs-lookup"><span data-stu-id="6aabc-130">The location.</span></span>

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

### <span data-ttu-id="6aabc-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6aabc-131">-Name</span></span>
<span data-ttu-id="6aabc-132">Имя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6aabc-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="6aabc-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6aabc-133">-PublicIpAddress</span></span>
<span data-ttu-id="6aabc-134">Массив общедоступных IP-адресов, связанных с ресурсом nat шлюза.</span><span class="sxs-lookup"><span data-stu-id="6aabc-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="6aabc-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6aabc-135">-PublicIpPrefix</span></span>
<span data-ttu-id="6aabc-136">Массив общедоступных IP-префиксов, связанных с ресурсом nat шлюза.</span><span class="sxs-lookup"><span data-stu-id="6aabc-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="6aabc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aabc-137">-ResourceGroupName</span></span>
<span data-ttu-id="6aabc-138">Имя группы ресурсов шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6aabc-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="6aabc-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="6aabc-139">-Sku</span></span>
<span data-ttu-id="6aabc-140">Имя SKU шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="6aabc-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="6aabc-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="6aabc-141">-Tag</span></span>
<span data-ttu-id="6aabc-142">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="6aabc-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6aabc-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="6aabc-143">-Zone</span></span>
<span data-ttu-id="6aabc-144">Список зон доступности, обозначающий зону, в которой необходимо развернуть шлюз NAT.</span><span class="sxs-lookup"><span data-stu-id="6aabc-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="6aabc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aabc-145">-Confirm</span></span>
<span data-ttu-id="6aabc-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aabc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aabc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aabc-147">-WhatIf</span></span>
<span data-ttu-id="6aabc-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aabc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aabc-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6aabc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aabc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aabc-150">CommonParameters</span></span>
<span data-ttu-id="6aabc-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aabc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aabc-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6aabc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aabc-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6aabc-153">INPUTS</span></span>

### <span data-ttu-id="6aabc-154">System.String</span><span class="sxs-lookup"><span data-stu-id="6aabc-154">System.String</span></span>

### <span data-ttu-id="6aabc-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6aabc-155">System.Int32</span></span>

### <span data-ttu-id="6aabc-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6aabc-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6aabc-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="6aabc-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="6aabc-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6aabc-158">OUTPUTS</span></span>

### <span data-ttu-id="6aabc-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="6aabc-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="6aabc-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6aabc-160">NOTES</span></span>

## <span data-ttu-id="6aabc-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aabc-161">RELATED LINKS</span></span>
