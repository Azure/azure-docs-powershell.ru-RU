---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734613"
---
# <span data-ttu-id="2ca2d-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ca2d-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="2ca2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ca2d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca2d-103">Создание префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2ca2d-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ca2d-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ca2d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca2d-106">Командлет **New-AzureRmPublicIpPrefix** создает префикс общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="2ca2d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ca2d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca2d-108">1: создание нового префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2ca2d-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="2ca2d-109">Эта команда создает новый ресурс префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="2ca2d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ca2d-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca2d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ca2d-111">-AsJob</span></span>
<span data-ttu-id="2ca2d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2ca2d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca2d-113">-DefaultProfile</span></span>
<span data-ttu-id="2ca2d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2ca2d-115">-Force</span></span>
<span data-ttu-id="2ca2d-116">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="2ca2d-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2ca2d-117">-IpAddressVersion</span></span>
<span data-ttu-id="2ca2d-118">Версия общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="2ca2d-119">-IpTag</span></span>
<span data-ttu-id="2ca2d-120">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2ca2d-121">-Location</span></span>
<span data-ttu-id="2ca2d-122">Расположение префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ca2d-123">-Name</span></span>
<span data-ttu-id="2ca2d-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="2ca2d-125">-PrefixLength</span></span>
<span data-ttu-id="2ca2d-126">Длина PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="2ca2d-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ca2d-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ca2d-129">-Sku</span></span>
<span data-ttu-id="2ca2d-130">Имя SKU префикса общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="2ca2d-131">-Tag</span></span>
<span data-ttu-id="2ca2d-132">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="2ca2d-133">-Zone</span></span>
<span data-ttu-id="2ca2d-134">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ca2d-135">-Confirm</span></span>
<span data-ttu-id="2ca2d-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca2d-137">-WhatIf</span></span>
<span data-ttu-id="2ca2d-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca2d-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca2d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca2d-140">CommonParameters</span></span>
<span data-ttu-id="2ca2d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ca2d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ca2d-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca2d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca2d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ca2d-143">INPUTS</span></span>

### <span data-ttu-id="2ca2d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca2d-144">System.String</span></span>
<span data-ttu-id="2ca2d-145">System. UInt16 System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. String, mscorlib, Version = 4.0.0.0, культура = нейтральная, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ca2d-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="2ca2d-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ca2d-146">OUTPUTS</span></span>

### <span data-ttu-id="2ca2d-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2ca2d-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="2ca2d-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ca2d-148">NOTES</span></span>

## <span data-ttu-id="2ca2d-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ca2d-149">RELATED LINKS</span></span>
