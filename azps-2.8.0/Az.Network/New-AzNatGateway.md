---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: f62b7bb2b338247305c53199b7f1e7087f195ffd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902134"
---
# <span data-ttu-id="22d98-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="22d98-101">New-AzNatGateway</span></span>

## <span data-ttu-id="22d98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22d98-102">SYNOPSIS</span></span>
<span data-ttu-id="22d98-103">Создайте новый ресурс шлюза NAT со свойствами public IP-адрес/public IP-префикс, IdleTimeoutInMinutes и SKU.</span><span class="sxs-lookup"><span data-stu-id="22d98-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="22d98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22d98-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22d98-105">DESCRIPTION</span></span>
<span data-ttu-id="22d98-106">Командлет **New-AzNatGateway** создает ресурс шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="22d98-107">Для natgateway требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="22d98-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="22d98-108">Общедоступный IP-адрес и/или префикс публичного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="22d98-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="22d98-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="22d98-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="22d98-110">Кратки</span><span class="sxs-lookup"><span data-stu-id="22d98-110">Sku</span></span>
- <span data-ttu-id="22d98-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d98-111">ResourceGroupName</span></span>
- <span data-ttu-id="22d98-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="22d98-112">ResourceName</span></span>
- <span data-ttu-id="22d98-113">Поиска</span><span class="sxs-lookup"><span data-stu-id="22d98-113">Location</span></span>

## <span data-ttu-id="22d98-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22d98-114">EXAMPLES</span></span>

### <span data-ttu-id="22d98-115">Пример 1: Создание шлюза NAT с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="22d98-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="22d98-116">Пример 2: Создание шлюза NAT с префиксом общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="22d98-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="22d98-117">Пример 3: Создание шлюза NAT с общедоступным IP-адресом в зоне доступности 1</span><span class="sxs-lookup"><span data-stu-id="22d98-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="22d98-118">Первая команда создает стандартный общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="22d98-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="22d98-119">Вторая команда создает шлюз NAT с общедоступным IP-адресом в зоне доступности 1.</span><span class="sxs-lookup"><span data-stu-id="22d98-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="22d98-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22d98-120">PARAMETERS</span></span>

### <span data-ttu-id="22d98-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22d98-121">-AsJob</span></span>
<span data-ttu-id="22d98-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="22d98-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22d98-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d98-123">-DefaultProfile</span></span>
<span data-ttu-id="22d98-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22d98-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d98-125">-Force</span><span class="sxs-lookup"><span data-stu-id="22d98-125">-Force</span></span>
<span data-ttu-id="22d98-126">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="22d98-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="22d98-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="22d98-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="22d98-128">Тайм-аут простоя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="22d98-129">-Location</span><span class="sxs-lookup"><span data-stu-id="22d98-129">-Location</span></span>
<span data-ttu-id="22d98-130">Расположение.</span><span class="sxs-lookup"><span data-stu-id="22d98-130">The location.</span></span>

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

### <span data-ttu-id="22d98-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22d98-131">-Name</span></span>
<span data-ttu-id="22d98-132">Имя шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="22d98-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22d98-133">-PublicIpAddress</span></span>
<span data-ttu-id="22d98-134">Массив общедоступных IP-адресов, связанных с ресурсом шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="22d98-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="22d98-135">-PublicIpPrefix</span></span>
<span data-ttu-id="22d98-136">Массив общедоступных IP-префиксов, связанных с ресурсом шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="22d98-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d98-137">-ResourceGroupName</span></span>
<span data-ttu-id="22d98-138">Имя группы ресурсов для шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="22d98-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="22d98-139">-Sku</span></span>
<span data-ttu-id="22d98-140">Имя SKU шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="22d98-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="22d98-141">-Tag</span></span>
<span data-ttu-id="22d98-142">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22d98-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="22d98-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="22d98-143">-Zone</span></span>
<span data-ttu-id="22d98-144">Список зон доступности, обозначающих зону, в которой должен быть развернут шлюз NAT.</span><span class="sxs-lookup"><span data-stu-id="22d98-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="22d98-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22d98-145">-Confirm</span></span>
<span data-ttu-id="22d98-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22d98-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d98-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d98-147">-WhatIf</span></span>
<span data-ttu-id="22d98-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22d98-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d98-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22d98-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d98-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d98-150">CommonParameters</span></span>
<span data-ttu-id="22d98-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22d98-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d98-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22d98-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d98-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22d98-153">INPUTS</span></span>

### <span data-ttu-id="22d98-154">System. String</span><span class="sxs-lookup"><span data-stu-id="22d98-154">System.String</span></span>

### <span data-ttu-id="22d98-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="22d98-155">System.Int32</span></span>

### <span data-ttu-id="22d98-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22d98-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="22d98-157">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="22d98-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="22d98-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22d98-158">OUTPUTS</span></span>

### <span data-ttu-id="22d98-159">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="22d98-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="22d98-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="22d98-160">NOTES</span></span>

## <span data-ttu-id="22d98-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22d98-161">RELATED LINKS</span></span>
