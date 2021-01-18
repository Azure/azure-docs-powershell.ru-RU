---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517357"
---
# <span data-ttu-id="aa928-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="aa928-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="aa928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa928-102">SYNOPSIS</span></span>
<span data-ttu-id="aa928-103">Обновляет описание существующего пространства имен «Автобус обслуживания».</span><span class="sxs-lookup"><span data-stu-id="aa928-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="aa928-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa928-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa928-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa928-105">DESCRIPTION</span></span>
<span data-ttu-id="aa928-106">В **этом же проектлете Set-AzServiceBusNamespace** обновляется описание указанного пространства имен "Автобус обслуживания" в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa928-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="aa928-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa928-107">EXAMPLES</span></span>

### <span data-ttu-id="aa928-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa928-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="aa928-109">Обновляет пространство имен автобусов обслуживания с новым описанием.</span><span class="sxs-lookup"><span data-stu-id="aa928-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="aa928-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa928-110">PARAMETERS</span></span>

### <span data-ttu-id="aa928-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa928-111">-DefaultProfile</span></span>
<span data-ttu-id="aa928-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa928-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa928-113">-Location</span><span class="sxs-lookup"><span data-stu-id="aa928-113">-Location</span></span>
<span data-ttu-id="aa928-114">Расположение пространства имен в автобусе обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aa928-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="aa928-115">-Name</span><span class="sxs-lookup"><span data-stu-id="aa928-115">-Name</span></span>
<span data-ttu-id="aa928-116">Имя пространства имен serviceBus.</span><span class="sxs-lookup"><span data-stu-id="aa928-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="aa928-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa928-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa928-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa928-118">The resource group name.</span></span>

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

### <span data-ttu-id="aa928-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="aa928-119">-SkuCapacity</span></span>
<span data-ttu-id="aa928-120">Емкость SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="aa928-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="aa928-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aa928-121">-SkuName</span></span>
<span data-ttu-id="aa928-122">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="aa928-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="aa928-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa928-123">-Tag</span></span>
<span data-ttu-id="aa928-124">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="aa928-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aa928-125">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="aa928-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aa928-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa928-126">-Confirm</span></span>
<span data-ttu-id="aa928-127">Обновляет пространство имен автобусов обслуживания, внося в нее указанные сведения.</span><span class="sxs-lookup"><span data-stu-id="aa928-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="aa928-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa928-128">-WhatIf</span></span>
<span data-ttu-id="aa928-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa928-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa928-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa928-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa928-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa928-131">CommonParameters</span></span>
<span data-ttu-id="aa928-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa928-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa928-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa928-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa928-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa928-134">INPUTS</span></span>

### <span data-ttu-id="aa928-135">System.String</span><span class="sxs-lookup"><span data-stu-id="aa928-135">System.String</span></span>

### <span data-ttu-id="aa928-136">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aa928-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aa928-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aa928-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aa928-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa928-138">OUTPUTS</span></span>

### <span data-ttu-id="aa928-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="aa928-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="aa928-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa928-140">NOTES</span></span>

## <span data-ttu-id="aa928-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa928-141">RELATED LINKS</span></span>
