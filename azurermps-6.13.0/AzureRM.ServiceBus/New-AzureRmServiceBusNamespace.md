---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 532135578418a90e9ce6887602723c2165f28aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566405"
---
# <span data-ttu-id="5f062-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5f062-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="5f062-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f062-102">SYNOPSIS</span></span>
<span data-ttu-id="5f062-103">Создает новое пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="5f062-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f062-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f062-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f062-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f062-105">DESCRIPTION</span></span>
<span data-ttu-id="5f062-106">Командлет **New-AzureRmServiceBusNamespace** создает новое пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="5f062-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="5f062-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="5f062-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="5f062-108">Эта операция является idempotent.</span><span class="sxs-lookup"><span data-stu-id="5f062-108">This operation is idempotent.</span></span>

## <span data-ttu-id="5f062-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f062-109">EXAMPLES</span></span>

### <span data-ttu-id="5f062-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f062-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="5f062-111">Создает новое пространство имен служебной шины в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f062-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="5f062-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f062-112">PARAMETERS</span></span>

### <span data-ttu-id="5f062-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f062-113">-DefaultProfile</span></span>
<span data-ttu-id="5f062-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f062-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-115">-Location</span><span class="sxs-lookup"><span data-stu-id="5f062-115">-Location</span></span>
<span data-ttu-id="5f062-116">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="5f062-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f062-117">-Name</span></span>
<span data-ttu-id="5f062-118">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="5f062-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f062-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f062-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f062-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5f062-121">-SkuCapacity</span></span>
<span data-ttu-id="5f062-122">Пространство имен Premium Service Bus Units, разрешенные значения 1 или 2 или 4</span><span class="sxs-lookup"><span data-stu-id="5f062-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5f062-123">-SkuName</span></span>
<span data-ttu-id="5f062-124">Название SKU пространства имен для служебной шины.</span><span class="sxs-lookup"><span data-stu-id="5f062-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="5f062-125">-Tag</span></span>
<span data-ttu-id="5f062-126">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="5f062-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="5f062-127">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5f062-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5f062-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f062-128">-Confirm</span></span>
<span data-ttu-id="5f062-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f062-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f062-130">-WhatIf</span></span>
<span data-ttu-id="5f062-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f062-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f062-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f062-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f062-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f062-133">CommonParameters</span></span>
<span data-ttu-id="5f062-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f062-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f062-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f062-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f062-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f062-136">INPUTS</span></span>

### <span data-ttu-id="5f062-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5f062-137">System.String</span></span>

### <span data-ttu-id="5f062-138">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5f062-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5f062-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f062-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5f062-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f062-140">OUTPUTS</span></span>

### <span data-ttu-id="5f062-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5f062-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5f062-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f062-142">NOTES</span></span>

## <span data-ttu-id="5f062-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f062-143">RELATED LINKS</span></span>
