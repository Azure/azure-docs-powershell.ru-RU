---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733797"
---
# <span data-ttu-id="79644-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="79644-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="79644-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79644-102">SYNOPSIS</span></span>
<span data-ttu-id="79644-103">Обновляет описание существующего пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="79644-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79644-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79644-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79644-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79644-105">DESCRIPTION</span></span>
<span data-ttu-id="79644-106">Командлет **Set-AzureRmServiceBusNamespace** обновляет описание пространства имен для указанной служебной шины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79644-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="79644-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79644-107">EXAMPLES</span></span>

### <span data-ttu-id="79644-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79644-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="79644-109">Обновляет пространство имен служебной шины с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="79644-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="79644-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79644-110">PARAMETERS</span></span>

### <span data-ttu-id="79644-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79644-111">-DefaultProfile</span></span>
<span data-ttu-id="79644-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79644-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79644-113">-Location</span><span class="sxs-lookup"><span data-stu-id="79644-113">-Location</span></span>
<span data-ttu-id="79644-114">Расположение пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="79644-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="79644-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79644-115">-Name</span></span>
<span data-ttu-id="79644-116">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="79644-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="79644-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79644-117">-ResourceGroupName</span></span>
<span data-ttu-id="79644-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79644-118">The resource group name.</span></span>

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

### <span data-ttu-id="79644-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="79644-119">-SkuCapacity</span></span>
<span data-ttu-id="79644-120">Емкость пространства имен SKU.</span><span class="sxs-lookup"><span data-stu-id="79644-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="79644-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="79644-121">-SkuName</span></span>
<span data-ttu-id="79644-122">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="79644-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="79644-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="79644-123">-Tag</span></span>
<span data-ttu-id="79644-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="79644-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79644-125">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="79644-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79644-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79644-126">-Confirm</span></span>
<span data-ttu-id="79644-127">Обновляет пространство имен служебной шины указанными данными.</span><span class="sxs-lookup"><span data-stu-id="79644-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="79644-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79644-128">-WhatIf</span></span>
<span data-ttu-id="79644-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79644-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79644-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79644-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79644-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79644-131">CommonParameters</span></span>
<span data-ttu-id="79644-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79644-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79644-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79644-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79644-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79644-134">INPUTS</span></span>

### <span data-ttu-id="79644-135">System. String</span><span class="sxs-lookup"><span data-stu-id="79644-135">System.String</span></span>

### <span data-ttu-id="79644-136">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="79644-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="79644-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="79644-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="79644-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79644-138">OUTPUTS</span></span>

### <span data-ttu-id="79644-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="79644-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="79644-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="79644-140">NOTES</span></span>

## <span data-ttu-id="79644-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79644-141">RELATED LINKS</span></span>
