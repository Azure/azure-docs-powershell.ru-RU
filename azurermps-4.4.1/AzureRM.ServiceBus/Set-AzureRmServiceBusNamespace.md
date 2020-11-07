---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 134e0d20566a8310a381a38297984202b7509250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734518"
---
# <span data-ttu-id="06c39-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="06c39-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="06c39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06c39-102">SYNOPSIS</span></span>
<span data-ttu-id="06c39-103">Обновляет описание существующего пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="06c39-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06c39-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> -Name <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06c39-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06c39-105">DESCRIPTION</span></span>
<span data-ttu-id="06c39-106">Командлет **Set-AzureRmServiceBusNamespace** обновляет описание пространства имен для указанной служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06c39-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="06c39-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06c39-107">EXAMPLES</span></span>

### <span data-ttu-id="06c39-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06c39-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
Status             :
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
Enabled            : False
```

<span data-ttu-id="06c39-109">Обновляет пространство имен служебной шины с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="06c39-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="06c39-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06c39-110">PARAMETERS</span></span>

### <span data-ttu-id="06c39-111">-Location</span><span class="sxs-lookup"><span data-stu-id="06c39-111">-Location</span></span>
<span data-ttu-id="06c39-112">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="06c39-112">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="06c39-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c39-113">-ResourceGroupName</span></span>
<span data-ttu-id="06c39-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06c39-114">The resource group name.</span></span>

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

### <span data-ttu-id="06c39-115">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="06c39-115">-SkuCapacity</span></span>
<span data-ttu-id="06c39-116">Емкость пространства имен SKU.</span><span class="sxs-lookup"><span data-stu-id="06c39-116">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="06c39-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="06c39-117">-SkuName</span></span>
<span data-ttu-id="06c39-118">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="06c39-118">The namespace SKU name.</span></span>

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

### <span data-ttu-id="06c39-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="06c39-119">-Tag</span></span>
<span data-ttu-id="06c39-120">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="06c39-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06c39-121">Например:</span><span class="sxs-lookup"><span data-stu-id="06c39-121">For example:</span></span>

<span data-ttu-id="06c39-122">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="06c39-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="06c39-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06c39-123">-Confirm</span></span>
<span data-ttu-id="06c39-124">Обновляет пространство имен служебной шины указанными данными.</span><span class="sxs-lookup"><span data-stu-id="06c39-124">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="06c39-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06c39-125">-WhatIf</span></span>
<span data-ttu-id="06c39-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06c39-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06c39-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06c39-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06c39-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c39-128">-DefaultProfile</span></span>
<span data-ttu-id="06c39-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06c39-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c39-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06c39-130">-Name</span></span>
<span data-ttu-id="06c39-131">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="06c39-131">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c39-132">CommonParameters</span></span>
<span data-ttu-id="06c39-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06c39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c39-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c39-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c39-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06c39-135">INPUTS</span></span>

### <span data-ttu-id="06c39-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06c39-136">-ResourceGroup</span></span>
 <span data-ttu-id="06c39-137">System. String</span><span class="sxs-lookup"><span data-stu-id="06c39-137">System.String</span></span>

### <span data-ttu-id="06c39-138">-+ +</span><span class="sxs-lookup"><span data-stu-id="06c39-138">-NamespaceName</span></span>
 <span data-ttu-id="06c39-139">System. String</span><span class="sxs-lookup"><span data-stu-id="06c39-139">System.String</span></span>

### <span data-ttu-id="06c39-140">-Location</span><span class="sxs-lookup"><span data-stu-id="06c39-140">-Location</span></span>
 <span data-ttu-id="06c39-141">System. String</span><span class="sxs-lookup"><span data-stu-id="06c39-141">System.String</span></span>

### <span data-ttu-id="06c39-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="06c39-142">-SkuName</span></span>
 <span data-ttu-id="06c39-143">System. String</span><span class="sxs-lookup"><span data-stu-id="06c39-143">System.String</span></span>

### <span data-ttu-id="06c39-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="06c39-144">-Tag</span></span>
 <span data-ttu-id="06c39-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06c39-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06c39-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06c39-146">OUTPUTS</span></span>

### <span data-ttu-id="06c39-147">Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="06c39-147">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="06c39-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="06c39-148">NOTES</span></span>
## <span data-ttu-id="06c39-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06c39-149">RELATED LINKS</span></span>

## <span data-ttu-id="06c39-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06c39-150">RELATED LINKS</span></span>

