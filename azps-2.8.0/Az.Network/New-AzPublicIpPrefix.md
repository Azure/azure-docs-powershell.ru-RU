---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 28c359c6d9ad9ebfa0d19d7fa4f8d5a72e4884dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902097"
---
# <span data-ttu-id="b5089-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b5089-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="b5089-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5089-102">SYNOPSIS</span></span>
<span data-ttu-id="b5089-103">Создание префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="b5089-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="b5089-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5089-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5089-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5089-105">DESCRIPTION</span></span>
<span data-ttu-id="b5089-106">Командлет **New-AzPublicIpPrefix** создает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b5089-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="b5089-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5089-107">EXAMPLES</span></span>

### <span data-ttu-id="b5089-108">1: создание нового префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="b5089-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="b5089-109">Эта команда создает новый ресурс префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b5089-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="b5089-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5089-110">PARAMETERS</span></span>

### <span data-ttu-id="b5089-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5089-111">-AsJob</span></span>
<span data-ttu-id="b5089-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b5089-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5089-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5089-113">-DefaultProfile</span></span>
<span data-ttu-id="b5089-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5089-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5089-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5089-115">-Force</span></span>
<span data-ttu-id="b5089-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="b5089-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b5089-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b5089-117">-IpAddressVersion</span></span>
<span data-ttu-id="b5089-118">Версия общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b5089-118">The public IP address version.</span></span>

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

### <span data-ttu-id="b5089-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="b5089-119">-IpTag</span></span>
<span data-ttu-id="b5089-120">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="b5089-120">IpTag List.</span></span>

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

### <span data-ttu-id="b5089-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b5089-121">-Location</span></span>
<span data-ttu-id="b5089-122">Расположение префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b5089-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="b5089-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5089-123">-Name</span></span>
<span data-ttu-id="b5089-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5089-124">The resource name.</span></span>

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

### <span data-ttu-id="b5089-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="b5089-125">-PrefixLength</span></span>
<span data-ttu-id="b5089-126">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="b5089-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="b5089-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5089-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5089-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5089-128">The resource group name.</span></span>

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

### <span data-ttu-id="b5089-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="b5089-129">-Sku</span></span>
<span data-ttu-id="b5089-130">Имя SKU префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b5089-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="b5089-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="b5089-131">-Tag</span></span>
<span data-ttu-id="b5089-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5089-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b5089-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="b5089-133">-Zone</span></span>
<span data-ttu-id="b5089-134">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="b5089-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b5089-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5089-135">-Confirm</span></span>
<span data-ttu-id="b5089-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5089-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5089-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5089-137">-WhatIf</span></span>
<span data-ttu-id="b5089-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5089-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5089-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5089-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5089-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5089-140">CommonParameters</span></span>
<span data-ttu-id="b5089-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5089-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5089-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5089-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5089-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5089-143">INPUTS</span></span>

### <span data-ttu-id="b5089-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b5089-144">System.String</span></span>

### <span data-ttu-id="b5089-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="b5089-145">System.UInt16</span></span>

### <span data-ttu-id="b5089-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="b5089-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="b5089-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="b5089-147">System.String[]</span></span>

### <span data-ttu-id="b5089-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b5089-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5089-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5089-149">OUTPUTS</span></span>

### <span data-ttu-id="b5089-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b5089-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="b5089-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5089-151">NOTES</span></span>

## <span data-ttu-id="b5089-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5089-152">RELATED LINKS</span></span>

[<span data-ttu-id="b5089-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b5089-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="b5089-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b5089-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="b5089-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b5089-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
