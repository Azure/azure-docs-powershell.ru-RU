---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: c72c4ad67f6096f5ba86924219670be53a725d26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953896"
---
# <span data-ttu-id="3f7dd-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="3f7dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f7dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7dd-103">Создание префикса для общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="3f7dd-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="3f7dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f7dd-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f7dd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f7dd-105">DESCRIPTION</span></span>
<span data-ttu-id="3f7dd-106">Для создания общего IP-префикса создается **cmdlet New-AzPublicIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="3f7dd-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="3f7dd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f7dd-107">EXAMPLES</span></span>

### <span data-ttu-id="3f7dd-108">Пример 1. Создание префикса для общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="3f7dd-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="3f7dd-109">Эта команда создает общедоступный IP-префикс ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="3f7dd-110">Пример 2. Создание нового глобального префикса общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="3f7dd-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="3f7dd-111">Эта команда создает новый глобальный общедоступный IP-префикс ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="3f7dd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f7dd-112">PARAMETERS</span></span>

### <span data-ttu-id="3f7dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f7dd-113">-AsJob</span></span>
<span data-ttu-id="3f7dd-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3f7dd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f7dd-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-115">-CustomIpPrefix</span></span>
<span data-ttu-id="3f7dd-116">CustomIpPrefix, с помощью который будет связан этот PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7dd-117">-DefaultProfile</span></span>
<span data-ttu-id="3f7dd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f7dd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3f7dd-119">-Force</span></span>
<span data-ttu-id="3f7dd-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="3f7dd-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3f7dd-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3f7dd-121">-IpAddressVersion</span></span>
<span data-ttu-id="3f7dd-122">Версия общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-122">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="3f7dd-123">-IpTag</span></span>
<span data-ttu-id="3f7dd-124">Список IPTag.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-125">-Location</span><span class="sxs-lookup"><span data-stu-id="3f7dd-125">-Location</span></span>
<span data-ttu-id="3f7dd-126">Расположение префикса общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="3f7dd-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3f7dd-127">-Name</span></span>
<span data-ttu-id="3f7dd-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-128">The resource name.</span></span>

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

### <span data-ttu-id="3f7dd-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="3f7dd-129">-PrefixLength</span></span>
<span data-ttu-id="3f7dd-130">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f7dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="3f7dd-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-132">The resource group name.</span></span>

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

### <span data-ttu-id="3f7dd-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="3f7dd-133">-Sku</span></span>
<span data-ttu-id="3f7dd-134">Имя SKU префикса общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f7dd-135">-Tag</span></span>
<span data-ttu-id="3f7dd-136">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3f7dd-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="3f7dd-137">-Tier</span></span>
<span data-ttu-id="3f7dd-138">Уровень SKU префикса общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="3f7dd-139">-Zone</span></span>
<span data-ttu-id="3f7dd-140">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7dd-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f7dd-141">-Confirm</span></span>
<span data-ttu-id="3f7dd-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f7dd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f7dd-143">-WhatIf</span></span>
<span data-ttu-id="3f7dd-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f7dd-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f7dd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7dd-146">CommonParameters</span></span>
<span data-ttu-id="3f7dd-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7dd-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f7dd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7dd-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f7dd-149">INPUTS</span></span>

### <span data-ttu-id="3f7dd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="3f7dd-150">System.String</span></span>

### <span data-ttu-id="3f7dd-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="3f7dd-151">System.UInt16</span></span>

### <span data-ttu-id="3f7dd-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="3f7dd-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="3f7dd-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3f7dd-153">System.String[]</span></span>

### <span data-ttu-id="3f7dd-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3f7dd-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3f7dd-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f7dd-155">OUTPUTS</span></span>

### <span data-ttu-id="3f7dd-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="3f7dd-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f7dd-157">NOTES</span></span>

## <span data-ttu-id="3f7dd-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f7dd-158">RELATED LINKS</span></span>

[<span data-ttu-id="3f7dd-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="3f7dd-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="3f7dd-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3f7dd-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
