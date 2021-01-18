---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517430"
---
# <span data-ttu-id="78ec6-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="78ec6-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="78ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="78ec6-103">Создается новое пространство имен «Шина обслуживания».</span><span class="sxs-lookup"><span data-stu-id="78ec6-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="78ec6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78ec6-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78ec6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="78ec6-106">Для создания пространства имен рабочих автобусов создается **cmdlet New-AzServiceBusNamespace.**</span><span class="sxs-lookup"><span data-stu-id="78ec6-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="78ec6-107">После создания манифеста ресурсов пространства имен будет неанимабельным.</span><span class="sxs-lookup"><span data-stu-id="78ec6-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="78ec6-108">Эта операция является idempotent.</span><span class="sxs-lookup"><span data-stu-id="78ec6-108">This operation is idempotent.</span></span>

## <span data-ttu-id="78ec6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78ec6-109">EXAMPLES</span></span>

### <span data-ttu-id="78ec6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78ec6-110">Example 1</span></span>
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

<span data-ttu-id="78ec6-111">Создание нового пространства имен «Автобус обслуживания» в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78ec6-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="78ec6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78ec6-112">PARAMETERS</span></span>

### <span data-ttu-id="78ec6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ec6-113">-DefaultProfile</span></span>
<span data-ttu-id="78ec6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78ec6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78ec6-115">-Location</span><span class="sxs-lookup"><span data-stu-id="78ec6-115">-Location</span></span>
<span data-ttu-id="78ec6-116">Расположение пространства имен в автобусе обслуживания.</span><span class="sxs-lookup"><span data-stu-id="78ec6-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="78ec6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="78ec6-117">-Name</span></span>
<span data-ttu-id="78ec6-118">Имя пространства имен serviceBus.</span><span class="sxs-lookup"><span data-stu-id="78ec6-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="78ec6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ec6-119">-ResourceGroupName</span></span>
<span data-ttu-id="78ec6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78ec6-120">The resource group name.</span></span>

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

### <span data-ttu-id="78ec6-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="78ec6-121">-SkuCapacity</span></span>
<span data-ttu-id="78ec6-122">Единицы пропускной способности пространства имен «Шина обслуживания премиум, разрешенные значения 1 или 2 или 4).</span><span class="sxs-lookup"><span data-stu-id="78ec6-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="78ec6-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="78ec6-123">-SkuName</span></span>
<span data-ttu-id="78ec6-124">Имя SKU В области имен в области имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="78ec6-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="78ec6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="78ec6-125">-Tag</span></span>
<span data-ttu-id="78ec6-126">Пары "значение ключа" в виде hash table, задаваемой на сервере в качестве тегов.</span><span class="sxs-lookup"><span data-stu-id="78ec6-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="78ec6-127">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="78ec6-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="78ec6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78ec6-128">-Confirm</span></span>
<span data-ttu-id="78ec6-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ec6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ec6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ec6-130">-WhatIf</span></span>
<span data-ttu-id="78ec6-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ec6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78ec6-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78ec6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ec6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ec6-133">CommonParameters</span></span>
<span data-ttu-id="78ec6-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ec6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ec6-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ec6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ec6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78ec6-136">INPUTS</span></span>

### <span data-ttu-id="78ec6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="78ec6-137">System.String</span></span>

### <span data-ttu-id="78ec6-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78ec6-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78ec6-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="78ec6-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="78ec6-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78ec6-140">OUTPUTS</span></span>

### <span data-ttu-id="78ec6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="78ec6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="78ec6-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78ec6-142">NOTES</span></span>

## <span data-ttu-id="78ec6-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78ec6-143">RELATED LINKS</span></span>
