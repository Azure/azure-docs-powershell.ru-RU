---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: cc00afb5dcdd4cc11c61cf96f2ae8ac3bb201bb5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245973"
---
# <span data-ttu-id="9e4ac-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e4ac-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="9e4ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4ac-103">Создание префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="9e4ac-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="9e4ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e4ac-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e4ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e4ac-105">DESCRIPTION</span></span>
<span data-ttu-id="9e4ac-106">Командлет **New-AzPublicIpPrefix** создает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="9e4ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e4ac-107">EXAMPLES</span></span>

### <span data-ttu-id="9e4ac-108">Пример 1: создание нового префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="9e4ac-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="9e4ac-109">Эта команда создает новый ресурс префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="9e4ac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e4ac-110">PARAMETERS</span></span>

### <span data-ttu-id="9e4ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e4ac-111">-AsJob</span></span>
<span data-ttu-id="9e4ac-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9e4ac-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e4ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4ac-113">-DefaultProfile</span></span>
<span data-ttu-id="9e4ac-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4ac-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9e4ac-115">-Force</span></span>
<span data-ttu-id="9e4ac-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="9e4ac-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9e4ac-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9e4ac-117">-IpAddressVersion</span></span>
<span data-ttu-id="9e4ac-118">Версия общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-118">The public IP address version.</span></span>

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

### <span data-ttu-id="9e4ac-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="9e4ac-119">-IpTag</span></span>
<span data-ttu-id="9e4ac-120">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-120">IpTag List.</span></span>

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

### <span data-ttu-id="9e4ac-121">-Location</span><span class="sxs-lookup"><span data-stu-id="9e4ac-121">-Location</span></span>
<span data-ttu-id="9e4ac-122">Расположение префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="9e4ac-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e4ac-123">-Name</span></span>
<span data-ttu-id="9e4ac-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-124">The resource name.</span></span>

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

### <span data-ttu-id="9e4ac-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="9e4ac-125">-PrefixLength</span></span>
<span data-ttu-id="9e4ac-126">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="9e4ac-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="9e4ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e4ac-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-128">The resource group name.</span></span>

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

### <span data-ttu-id="9e4ac-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e4ac-129">-Sku</span></span>
<span data-ttu-id="9e4ac-130">Имя SKU префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="9e4ac-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="9e4ac-131">-Tag</span></span>
<span data-ttu-id="9e4ac-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9e4ac-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="9e4ac-133">-Zone</span></span>
<span data-ttu-id="9e4ac-134">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9e4ac-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e4ac-135">-Confirm</span></span>
<span data-ttu-id="9e4ac-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4ac-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4ac-137">-WhatIf</span></span>
<span data-ttu-id="9e4ac-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e4ac-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4ac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4ac-140">CommonParameters</span></span>
<span data-ttu-id="9e4ac-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e4ac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4ac-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4ac-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4ac-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e4ac-143">INPUTS</span></span>

### <span data-ttu-id="9e4ac-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4ac-144">System.String</span></span>

### <span data-ttu-id="9e4ac-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="9e4ac-145">System.UInt16</span></span>

### <span data-ttu-id="9e4ac-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="9e4ac-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="9e4ac-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="9e4ac-147">System.String[]</span></span>

### <span data-ttu-id="9e4ac-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9e4ac-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e4ac-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e4ac-149">OUTPUTS</span></span>

### <span data-ttu-id="9e4ac-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e4ac-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="9e4ac-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e4ac-151">NOTES</span></span>

## <span data-ttu-id="9e4ac-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e4ac-152">RELATED LINKS</span></span>

[<span data-ttu-id="9e4ac-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e4ac-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="9e4ac-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e4ac-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="9e4ac-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9e4ac-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
