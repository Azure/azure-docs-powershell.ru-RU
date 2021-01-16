---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391543"
---
# <span data-ttu-id="53571-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="53571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53571-102">SYNOPSIS</span></span>
<span data-ttu-id="53571-103">Создание префикса для общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="53571-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="53571-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53571-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53571-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53571-105">DESCRIPTION</span></span>
<span data-ttu-id="53571-106">Для создания общего IP-префикса создается **cmdlet New-AzPublicIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="53571-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="53571-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53571-107">EXAMPLES</span></span>

### <span data-ttu-id="53571-108">Пример 1. Создание префикса для общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="53571-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="53571-109">Эта команда создает общедоступный IP-префикс ресурса.</span><span class="sxs-lookup"><span data-stu-id="53571-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="53571-110">Пример 2. Создание нового глобального префикса общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="53571-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="53571-111">Эта команда создает новый глобальный общедоступный IP-префикс ресурса.</span><span class="sxs-lookup"><span data-stu-id="53571-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="53571-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53571-112">PARAMETERS</span></span>

### <span data-ttu-id="53571-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53571-113">-AsJob</span></span>
<span data-ttu-id="53571-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="53571-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53571-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-115">-CustomIpPrefix</span></span>
<span data-ttu-id="53571-116">CustomIpPrefix, с помощью который будет связан этот PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

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

### <span data-ttu-id="53571-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53571-117">-DefaultProfile</span></span>
<span data-ttu-id="53571-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53571-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53571-119">-Force</span><span class="sxs-lookup"><span data-stu-id="53571-119">-Force</span></span>
<span data-ttu-id="53571-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="53571-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="53571-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="53571-121">-IpAddressVersion</span></span>
<span data-ttu-id="53571-122">Версия общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="53571-122">The public IP address version.</span></span>

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

### <span data-ttu-id="53571-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="53571-123">-IpTag</span></span>
<span data-ttu-id="53571-124">Список IPTag.</span><span class="sxs-lookup"><span data-stu-id="53571-124">IpTag List.</span></span>

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

### <span data-ttu-id="53571-125">-Location</span><span class="sxs-lookup"><span data-stu-id="53571-125">-Location</span></span>
<span data-ttu-id="53571-126">Расположение префикса общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="53571-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="53571-127">-Name</span><span class="sxs-lookup"><span data-stu-id="53571-127">-Name</span></span>
<span data-ttu-id="53571-128">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="53571-128">The resource name.</span></span>

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

### <span data-ttu-id="53571-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="53571-129">-PrefixLength</span></span>
<span data-ttu-id="53571-130">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-130">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="53571-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53571-131">-ResourceGroupName</span></span>
<span data-ttu-id="53571-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53571-132">The resource group name.</span></span>

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

### <span data-ttu-id="53571-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="53571-133">-Sku</span></span>
<span data-ttu-id="53571-134">Имя SKU префикса общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="53571-134">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="53571-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="53571-135">-Tag</span></span>
<span data-ttu-id="53571-136">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="53571-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="53571-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="53571-137">-Tier</span></span>
<span data-ttu-id="53571-138">Уровень SKU префикса общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="53571-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="53571-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="53571-139">-Zone</span></span>
<span data-ttu-id="53571-140">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="53571-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="53571-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53571-141">-Confirm</span></span>
<span data-ttu-id="53571-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="53571-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53571-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53571-143">-WhatIf</span></span>
<span data-ttu-id="53571-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53571-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53571-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53571-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53571-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53571-146">CommonParameters</span></span>
<span data-ttu-id="53571-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53571-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53571-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53571-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53571-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53571-149">INPUTS</span></span>

### <span data-ttu-id="53571-150">System.String</span><span class="sxs-lookup"><span data-stu-id="53571-150">System.String</span></span>

### <span data-ttu-id="53571-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="53571-151">System.UInt16</span></span>

### <span data-ttu-id="53571-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="53571-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="53571-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="53571-153">System.String[]</span></span>

### <span data-ttu-id="53571-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53571-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53571-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53571-155">OUTPUTS</span></span>

### <span data-ttu-id="53571-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="53571-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53571-157">NOTES</span></span>

## <span data-ttu-id="53571-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53571-158">RELATED LINKS</span></span>

[<span data-ttu-id="53571-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="53571-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="53571-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="53571-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
