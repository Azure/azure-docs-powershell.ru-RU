---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074308"
---
# <span data-ttu-id="2db01-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="2db01-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="2db01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2db01-102">SYNOPSIS</span></span>
<span data-ttu-id="2db01-103">Обновляет описание существующего пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2db01-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="2db01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2db01-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2db01-105">DESCRIPTION</span></span>
<span data-ttu-id="2db01-106">Командлет **Set-AzServiceBusNamespace** обновляет описание пространства имен для указанной служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2db01-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="2db01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2db01-107">EXAMPLES</span></span>

### <span data-ttu-id="2db01-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2db01-108">Example 1</span></span>
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

<span data-ttu-id="2db01-109">Обновляет пространство имен служебной шины с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="2db01-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="2db01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2db01-110">PARAMETERS</span></span>

### <span data-ttu-id="2db01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db01-111">-DefaultProfile</span></span>
<span data-ttu-id="2db01-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2db01-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2db01-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2db01-113">-Location</span></span>
<span data-ttu-id="2db01-114">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2db01-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="2db01-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2db01-115">-Name</span></span>
<span data-ttu-id="2db01-116">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="2db01-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="2db01-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db01-117">-ResourceGroupName</span></span>
<span data-ttu-id="2db01-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2db01-118">The resource group name.</span></span>

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

### <span data-ttu-id="2db01-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2db01-119">-SkuCapacity</span></span>
<span data-ttu-id="2db01-120">Емкость пространства имен SKU.</span><span class="sxs-lookup"><span data-stu-id="2db01-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="2db01-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2db01-121">-SkuName</span></span>
<span data-ttu-id="2db01-122">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2db01-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="2db01-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="2db01-123">-Tag</span></span>
<span data-ttu-id="2db01-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2db01-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2db01-125">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2db01-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2db01-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2db01-126">-Confirm</span></span>
<span data-ttu-id="2db01-127">Обновляет пространство имен служебной шины указанными данными.</span><span class="sxs-lookup"><span data-stu-id="2db01-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="2db01-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db01-128">-WhatIf</span></span>
<span data-ttu-id="2db01-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2db01-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db01-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2db01-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db01-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db01-131">CommonParameters</span></span>
<span data-ttu-id="2db01-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2db01-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db01-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db01-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db01-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2db01-134">INPUTS</span></span>

### <span data-ttu-id="2db01-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2db01-135">System.String</span></span>

### <span data-ttu-id="2db01-136">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2db01-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2db01-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2db01-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2db01-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2db01-138">OUTPUTS</span></span>

### <span data-ttu-id="2db01-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2db01-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2db01-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="2db01-140">NOTES</span></span>

## <span data-ttu-id="2db01-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2db01-141">RELATED LINKS</span></span>
