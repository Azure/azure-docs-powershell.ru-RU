---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235336"
---
# <span data-ttu-id="c065e-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c065e-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="c065e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c065e-102">SYNOPSIS</span></span>
<span data-ttu-id="c065e-103">Создает новое пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c065e-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="c065e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c065e-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c065e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c065e-105">DESCRIPTION</span></span>
<span data-ttu-id="c065e-106">Командлет **New-AzServiceBusNamespace** создает новое пространство имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c065e-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="c065e-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="c065e-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="c065e-108">Эта операция является idempotent.</span><span class="sxs-lookup"><span data-stu-id="c065e-108">This operation is idempotent.</span></span>

## <span data-ttu-id="c065e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c065e-109">EXAMPLES</span></span>

### <span data-ttu-id="c065e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c065e-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="c065e-111">Создает новое пространство имен служебной шины в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c065e-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="c065e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c065e-112">PARAMETERS</span></span>

### <span data-ttu-id="c065e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c065e-113">-DefaultProfile</span></span>
<span data-ttu-id="c065e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c065e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c065e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="c065e-115">-Location</span></span>
<span data-ttu-id="c065e-116">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c065e-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="c065e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c065e-117">-Name</span></span>
<span data-ttu-id="c065e-118">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="c065e-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="c065e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c065e-119">-ResourceGroupName</span></span>
<span data-ttu-id="c065e-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c065e-120">The resource group name.</span></span>

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

### <span data-ttu-id="c065e-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c065e-121">-SkuCapacity</span></span>
<span data-ttu-id="c065e-122">Пространство имен Premium Service Bus Units, разрешенные значения 1 или 2 или 4</span><span class="sxs-lookup"><span data-stu-id="c065e-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="c065e-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c065e-123">-SkuName</span></span>
<span data-ttu-id="c065e-124">Название SKU пространства имен для служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c065e-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="c065e-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="c065e-125">-Tag</span></span>
<span data-ttu-id="c065e-126">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="c065e-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c065e-127">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="c065e-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c065e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c065e-128">-Confirm</span></span>
<span data-ttu-id="c065e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c065e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c065e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c065e-130">-WhatIf</span></span>
<span data-ttu-id="c065e-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c065e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c065e-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c065e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c065e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c065e-133">CommonParameters</span></span>
<span data-ttu-id="c065e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c065e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c065e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c065e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c065e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c065e-136">INPUTS</span></span>

### <span data-ttu-id="c065e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c065e-137">System.String</span></span>

### <span data-ttu-id="c065e-138">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c065e-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c065e-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c065e-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c065e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c065e-140">OUTPUTS</span></span>

### <span data-ttu-id="c065e-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c065e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c065e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c065e-142">NOTES</span></span>

## <span data-ttu-id="c065e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c065e-143">RELATED LINKS</span></span>
