---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566117"
---
# <span data-ttu-id="ad9b2-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ad9b2-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="ad9b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9b2-103">Создает новое пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad9b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad9b2-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad9b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad9b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ad9b2-106">Командлет **New-AzureRmServiceBusNamespace** создает новое пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="ad9b2-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="ad9b2-108">Эта операция является idempotent.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-108">This operation is idempotent.</span></span>

## <span data-ttu-id="ad9b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad9b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ad9b2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad9b2-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="ad9b2-111">Создает новое пространство имен служебной шины в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="ad9b2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad9b2-112">PARAMETERS</span></span>

### <span data-ttu-id="ad9b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9b2-113">-DefaultProfile</span></span>
<span data-ttu-id="ad9b2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad9b2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ad9b2-115">-Location</span></span>
<span data-ttu-id="ad9b2-116">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-116">The Service Bus namespace location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9b2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad9b2-117">-Name</span></span>
<span data-ttu-id="ad9b2-118">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad9b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad9b2-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9b2-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ad9b2-121">-SkuName</span></span>
<span data-ttu-id="ad9b2-122">Название SKU пространства имен для служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-122">The Service Bus namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9b2-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="ad9b2-123">-Tag</span></span>
<span data-ttu-id="ad9b2-124">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ad9b2-125">Например:</span><span class="sxs-lookup"><span data-stu-id="ad9b2-125">For example:</span></span>

<span data-ttu-id="ad9b2-126">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="ad9b2-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ad9b2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad9b2-127">-Confirm</span></span>
<span data-ttu-id="ad9b2-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9b2-129">-WhatIf</span></span>
<span data-ttu-id="ad9b2-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad9b2-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9b2-132">CommonParameters</span></span>
<span data-ttu-id="ad9b2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9b2-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad9b2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9b2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad9b2-135">INPUTS</span></span>

### <span data-ttu-id="ad9b2-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad9b2-136">-ResourceGroup</span></span>
 <span data-ttu-id="ad9b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9b2-137">System.String</span></span>

### <span data-ttu-id="ad9b2-138">-+ +</span><span class="sxs-lookup"><span data-stu-id="ad9b2-138">-NamespaceName</span></span>
 <span data-ttu-id="ad9b2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9b2-139">System.String</span></span>

### <span data-ttu-id="ad9b2-140">-Location</span><span class="sxs-lookup"><span data-stu-id="ad9b2-140">-Location</span></span>
 <span data-ttu-id="ad9b2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9b2-141">System.String</span></span>

### <span data-ttu-id="ad9b2-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ad9b2-142">-SkuName</span></span>
 <span data-ttu-id="ad9b2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ad9b2-143">System.String</span></span>

### <span data-ttu-id="ad9b2-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="ad9b2-144">-Tag</span></span>
 <span data-ttu-id="ad9b2-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad9b2-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad9b2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad9b2-146">OUTPUTS</span></span>

### <span data-ttu-id="ad9b2-147">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ad9b2-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ad9b2-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad9b2-148">NOTES</span></span>

## <span data-ttu-id="ad9b2-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad9b2-149">RELATED LINKS</span></span>

