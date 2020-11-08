---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 1f6931c294d26fbade402f2efefb4b722ef8203e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073252"
---
# <span data-ttu-id="42954-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="42954-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="42954-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42954-102">SYNOPSIS</span></span>
<span data-ttu-id="42954-103">Создание префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="42954-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="42954-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42954-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42954-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42954-105">DESCRIPTION</span></span>
<span data-ttu-id="42954-106">Командлет **New-AzPublicIpPrefix** создает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42954-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="42954-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42954-107">EXAMPLES</span></span>

### <span data-ttu-id="42954-108">1: создание нового префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="42954-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="42954-109">Эта команда создает новый ресурс префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42954-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="42954-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42954-110">PARAMETERS</span></span>

### <span data-ttu-id="42954-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42954-111">-AsJob</span></span>
<span data-ttu-id="42954-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42954-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42954-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42954-113">-DefaultProfile</span></span>
<span data-ttu-id="42954-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42954-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42954-115">-Force</span><span class="sxs-lookup"><span data-stu-id="42954-115">-Force</span></span>
<span data-ttu-id="42954-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="42954-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="42954-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="42954-117">-IpAddressVersion</span></span>
<span data-ttu-id="42954-118">Версия общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42954-118">The public IP address version.</span></span>

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

### <span data-ttu-id="42954-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="42954-119">-IpTag</span></span>
<span data-ttu-id="42954-120">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="42954-120">IpTag List.</span></span>

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

### <span data-ttu-id="42954-121">-Location</span><span class="sxs-lookup"><span data-stu-id="42954-121">-Location</span></span>
<span data-ttu-id="42954-122">Расположение префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42954-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="42954-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42954-123">-Name</span></span>
<span data-ttu-id="42954-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="42954-124">The resource name.</span></span>

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

### <span data-ttu-id="42954-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="42954-125">-PrefixLength</span></span>
<span data-ttu-id="42954-126">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="42954-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="42954-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42954-127">-ResourceGroupName</span></span>
<span data-ttu-id="42954-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42954-128">The resource group name.</span></span>

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

### <span data-ttu-id="42954-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="42954-129">-Sku</span></span>
<span data-ttu-id="42954-130">Имя SKU префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42954-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="42954-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="42954-131">-Tag</span></span>
<span data-ttu-id="42954-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42954-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="42954-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="42954-133">-Zone</span></span>
<span data-ttu-id="42954-134">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="42954-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="42954-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42954-135">-Confirm</span></span>
<span data-ttu-id="42954-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42954-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42954-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42954-137">-WhatIf</span></span>
<span data-ttu-id="42954-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42954-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42954-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42954-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42954-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42954-140">CommonParameters</span></span>
<span data-ttu-id="42954-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42954-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42954-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42954-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42954-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42954-143">INPUTS</span></span>

### <span data-ttu-id="42954-144">System. String</span><span class="sxs-lookup"><span data-stu-id="42954-144">System.String</span></span>

### <span data-ttu-id="42954-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="42954-145">System.UInt16</span></span>

### <span data-ttu-id="42954-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="42954-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="42954-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="42954-147">System.String[]</span></span>

### <span data-ttu-id="42954-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42954-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="42954-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42954-149">OUTPUTS</span></span>

### <span data-ttu-id="42954-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="42954-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="42954-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="42954-151">NOTES</span></span>

## <span data-ttu-id="42954-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42954-152">RELATED LINKS</span></span>

[<span data-ttu-id="42954-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="42954-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="42954-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="42954-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="42954-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="42954-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
