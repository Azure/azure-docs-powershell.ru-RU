---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: f4a94823ba0ff615a68a9e17703ba7e8193b0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566102"
---
# <span data-ttu-id="bff76-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="bff76-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="bff76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bff76-102">SYNOPSIS</span></span>
<span data-ttu-id="bff76-103">Обновляет описание существующего пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bff76-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bff76-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff76-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff76-105">DESCRIPTION</span></span>
<span data-ttu-id="bff76-106">Командлет **Set-AzureRmServiceBusNamespace** обновляет описание пространства имен для указанной служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bff76-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="bff76-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bff76-107">EXAMPLES</span></span>

### <span data-ttu-id="bff76-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bff76-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="bff76-109">Обновляет пространство имен служебной шины с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="bff76-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="bff76-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bff76-110">PARAMETERS</span></span>

### <span data-ttu-id="bff76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff76-111">-DefaultProfile</span></span>
<span data-ttu-id="bff76-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bff76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff76-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bff76-113">-Location</span></span>
<span data-ttu-id="bff76-114">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bff76-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="bff76-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bff76-115">-Name</span></span>
<span data-ttu-id="bff76-116">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bff76-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="bff76-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff76-117">-ResourceGroupName</span></span>
<span data-ttu-id="bff76-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bff76-118">The resource group name.</span></span>

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

### <span data-ttu-id="bff76-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bff76-119">-SkuCapacity</span></span>
<span data-ttu-id="bff76-120">Емкость пространства имен SKU.</span><span class="sxs-lookup"><span data-stu-id="bff76-120">Namespace Sku Capacity.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff76-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bff76-121">-SkuName</span></span>
<span data-ttu-id="bff76-122">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bff76-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="bff76-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="bff76-123">-Tag</span></span>
<span data-ttu-id="bff76-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="bff76-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bff76-125">Например:</span><span class="sxs-lookup"><span data-stu-id="bff76-125">For example:</span></span>

<span data-ttu-id="bff76-126">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="bff76-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bff76-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bff76-127">-Confirm</span></span>
<span data-ttu-id="bff76-128">Обновляет пространство имен служебной шины указанными данными.</span><span class="sxs-lookup"><span data-stu-id="bff76-128">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="bff76-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff76-129">-WhatIf</span></span>
<span data-ttu-id="bff76-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bff76-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff76-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bff76-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff76-132">CommonParameters</span></span>
<span data-ttu-id="bff76-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bff76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff76-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff76-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff76-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bff76-135">INPUTS</span></span>

### <span data-ttu-id="bff76-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bff76-136">-ResourceGroup</span></span>
 <span data-ttu-id="bff76-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bff76-137">System.String</span></span>

### <span data-ttu-id="bff76-138">-+ +</span><span class="sxs-lookup"><span data-stu-id="bff76-138">-NamespaceName</span></span>
 <span data-ttu-id="bff76-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bff76-139">System.String</span></span>

### <span data-ttu-id="bff76-140">-Location</span><span class="sxs-lookup"><span data-stu-id="bff76-140">-Location</span></span>
 <span data-ttu-id="bff76-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bff76-141">System.String</span></span>

### <span data-ttu-id="bff76-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bff76-142">-SkuName</span></span>
 <span data-ttu-id="bff76-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bff76-143">System.String</span></span>

### <span data-ttu-id="bff76-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="bff76-144">-Tag</span></span>
 <span data-ttu-id="bff76-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bff76-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bff76-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff76-146">OUTPUTS</span></span>

### <span data-ttu-id="bff76-147">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bff76-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="bff76-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="bff76-148">NOTES</span></span>


## <span data-ttu-id="bff76-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bff76-149">RELATED LINKS</span></span>

