---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: cc00afb5dcdd4cc11c61cf96f2ae8ac3bb201bb5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234983"
---
# <span data-ttu-id="5c218-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c218-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="5c218-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c218-102">SYNOPSIS</span></span>
<span data-ttu-id="5c218-103">Создание префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="5c218-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="5c218-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c218-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c218-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c218-105">DESCRIPTION</span></span>
<span data-ttu-id="5c218-106">Командлет **New-AzPublicIpPrefix** создает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5c218-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="5c218-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c218-107">EXAMPLES</span></span>

### <span data-ttu-id="5c218-108">Пример 1: создание нового префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="5c218-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="5c218-109">Эта команда создает новый ресурс префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5c218-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="5c218-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c218-110">PARAMETERS</span></span>

### <span data-ttu-id="5c218-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c218-111">-AsJob</span></span>
<span data-ttu-id="5c218-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5c218-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c218-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c218-113">-DefaultProfile</span></span>
<span data-ttu-id="5c218-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c218-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c218-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c218-115">-Force</span></span>
<span data-ttu-id="5c218-116">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="5c218-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c218-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5c218-117">-IpAddressVersion</span></span>
<span data-ttu-id="5c218-118">Версия общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5c218-118">The public IP address version.</span></span>

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

### <span data-ttu-id="5c218-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="5c218-119">-IpTag</span></span>
<span data-ttu-id="5c218-120">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="5c218-120">IpTag List.</span></span>

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

### <span data-ttu-id="5c218-121">-Location</span><span class="sxs-lookup"><span data-stu-id="5c218-121">-Location</span></span>
<span data-ttu-id="5c218-122">Расположение префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5c218-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="5c218-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c218-123">-Name</span></span>
<span data-ttu-id="5c218-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5c218-124">The resource name.</span></span>

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

### <span data-ttu-id="5c218-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="5c218-125">-PrefixLength</span></span>
<span data-ttu-id="5c218-126">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="5c218-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="5c218-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c218-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c218-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c218-128">The resource group name.</span></span>

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

### <span data-ttu-id="5c218-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="5c218-129">-Sku</span></span>
<span data-ttu-id="5c218-130">Имя SKU префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5c218-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="5c218-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="5c218-131">-Tag</span></span>
<span data-ttu-id="5c218-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c218-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5c218-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="5c218-133">-Zone</span></span>
<span data-ttu-id="5c218-134">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="5c218-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5c218-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c218-135">-Confirm</span></span>
<span data-ttu-id="5c218-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c218-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c218-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c218-137">-WhatIf</span></span>
<span data-ttu-id="5c218-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c218-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c218-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c218-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c218-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c218-140">CommonParameters</span></span>
<span data-ttu-id="5c218-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c218-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c218-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c218-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c218-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c218-143">INPUTS</span></span>

### <span data-ttu-id="5c218-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5c218-144">System.String</span></span>

### <span data-ttu-id="5c218-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="5c218-145">System.UInt16</span></span>

### <span data-ttu-id="5c218-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="5c218-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="5c218-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="5c218-147">System.String[]</span></span>

### <span data-ttu-id="5c218-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5c218-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5c218-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c218-149">OUTPUTS</span></span>

### <span data-ttu-id="5c218-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c218-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="5c218-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c218-151">NOTES</span></span>

## <span data-ttu-id="5c218-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c218-152">RELATED LINKS</span></span>

[<span data-ttu-id="5c218-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c218-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="5c218-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c218-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="5c218-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c218-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
