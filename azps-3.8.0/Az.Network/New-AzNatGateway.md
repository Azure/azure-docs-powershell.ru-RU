---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 49a6a7d817a6b84626b200faada5c36525dc1c91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073105"
---
# <span data-ttu-id="b368e-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b368e-101">New-AzNatGateway</span></span>

## <span data-ttu-id="b368e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b368e-102">SYNOPSIS</span></span>
<span data-ttu-id="b368e-103">Создайте новый ресурс шлюза NAT со свойствами public IP-адрес/public IP-префикс, IdleTimeoutInMinutes и SKU.</span><span class="sxs-lookup"><span data-stu-id="b368e-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="b368e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b368e-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b368e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b368e-105">DESCRIPTION</span></span>
<span data-ttu-id="b368e-106">Командлет **New-AzNatGateway** создает ресурс шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="b368e-107">Для natgateway требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="b368e-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="b368e-108">Общедоступный IP-адрес и/или префикс публичного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="b368e-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="b368e-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b368e-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="b368e-110">Кратки</span><span class="sxs-lookup"><span data-stu-id="b368e-110">Sku</span></span>
- <span data-ttu-id="b368e-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b368e-111">ResourceGroupName</span></span>
- <span data-ttu-id="b368e-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="b368e-112">ResourceName</span></span>
- <span data-ttu-id="b368e-113">Поиска</span><span class="sxs-lookup"><span data-stu-id="b368e-113">Location</span></span>

## <span data-ttu-id="b368e-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b368e-114">EXAMPLES</span></span>

### <span data-ttu-id="b368e-115">Пример 1: Создание шлюза NAT с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="b368e-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="b368e-116">Пример 2: Создание шлюза NAT с префиксом общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="b368e-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="b368e-117">Пример 3: Создание шлюза NAT с общедоступным IP-адресом в зоне доступности 1</span><span class="sxs-lookup"><span data-stu-id="b368e-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="b368e-118">Первая команда создает стандартный общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b368e-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="b368e-119">Вторая команда создает шлюз NAT с общедоступным IP-адресом в зоне доступности 1.</span><span class="sxs-lookup"><span data-stu-id="b368e-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="b368e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b368e-120">PARAMETERS</span></span>

### <span data-ttu-id="b368e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b368e-121">-AsJob</span></span>
<span data-ttu-id="b368e-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b368e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b368e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b368e-123">-DefaultProfile</span></span>
<span data-ttu-id="b368e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b368e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b368e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b368e-125">-Force</span></span>
<span data-ttu-id="b368e-126">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="b368e-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b368e-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b368e-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b368e-128">Тайм-аут простоя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="b368e-129">-Location</span><span class="sxs-lookup"><span data-stu-id="b368e-129">-Location</span></span>
<span data-ttu-id="b368e-130">Расположение.</span><span class="sxs-lookup"><span data-stu-id="b368e-130">The location.</span></span>

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

### <span data-ttu-id="b368e-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b368e-131">-Name</span></span>
<span data-ttu-id="b368e-132">Имя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="b368e-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b368e-133">-PublicIpAddress</span></span>
<span data-ttu-id="b368e-134">Массив общедоступных IP-адресов, связанных с ресурсом шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="b368e-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b368e-135">-PublicIpPrefix</span></span>
<span data-ttu-id="b368e-136">Массив общедоступных IP-префиксов, связанных с ресурсом шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="b368e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b368e-137">-ResourceGroupName</span></span>
<span data-ttu-id="b368e-138">Имя группы ресурсов для шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="b368e-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="b368e-139">-Sku</span></span>
<span data-ttu-id="b368e-140">Имя SKU шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="b368e-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="b368e-141">-Tag</span></span>
<span data-ttu-id="b368e-142">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b368e-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b368e-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="b368e-143">-Zone</span></span>
<span data-ttu-id="b368e-144">Список зон доступности, обозначающих зону, в которой должен быть развернут шлюз NAT.</span><span class="sxs-lookup"><span data-stu-id="b368e-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="b368e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b368e-145">-Confirm</span></span>
<span data-ttu-id="b368e-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b368e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b368e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b368e-147">-WhatIf</span></span>
<span data-ttu-id="b368e-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b368e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b368e-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b368e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b368e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b368e-150">CommonParameters</span></span>
<span data-ttu-id="b368e-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b368e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b368e-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b368e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b368e-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b368e-153">INPUTS</span></span>

### <span data-ttu-id="b368e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b368e-154">System.String</span></span>

### <span data-ttu-id="b368e-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b368e-155">System.Int32</span></span>

### <span data-ttu-id="b368e-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b368e-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b368e-157">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="b368e-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="b368e-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b368e-158">OUTPUTS</span></span>

### <span data-ttu-id="b368e-159">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="b368e-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="b368e-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="b368e-160">NOTES</span></span>

## <span data-ttu-id="b368e-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b368e-161">RELATED LINKS</span></span>
