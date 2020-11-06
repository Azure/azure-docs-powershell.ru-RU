---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566141"
---
# <span data-ttu-id="2706b-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2706b-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="2706b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2706b-102">SYNOPSIS</span></span>
<span data-ttu-id="2706b-103">Создание нового пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="2706b-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2706b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2706b-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2706b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2706b-105">DESCRIPTION</span></span>
<span data-ttu-id="2706b-106">Командлет **New-AzureRmRelayNamespace** создает новое пространство имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="2706b-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="2706b-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="2706b-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="2706b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2706b-108">EXAMPLES</span></span>

### <span data-ttu-id="2706b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2706b-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="2706b-110">Создание нового пространства имен ретрансляции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2706b-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="2706b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2706b-111">PARAMETERS</span></span>

### <span data-ttu-id="2706b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2706b-112">-DefaultProfile</span></span>
<span data-ttu-id="2706b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2706b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2706b-114">-Location</span><span class="sxs-lookup"><span data-stu-id="2706b-114">-Location</span></span>
<span data-ttu-id="2706b-115">Расположение пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="2706b-115">Relay Namespace Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2706b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2706b-116">-Name</span></span>
<span data-ttu-id="2706b-117">Имя пространства имен ретрансляции</span><span class="sxs-lookup"><span data-stu-id="2706b-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="2706b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2706b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2706b-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2706b-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2706b-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="2706b-120">-Tag</span></span>
<span data-ttu-id="2706b-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2706b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2706b-122">Например:</span><span class="sxs-lookup"><span data-stu-id="2706b-122">For example:</span></span>

<span data-ttu-id="2706b-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2706b-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2706b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2706b-124">-Confirm</span></span>
<span data-ttu-id="2706b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2706b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2706b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2706b-126">-WhatIf</span></span>
<span data-ttu-id="2706b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2706b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2706b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2706b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2706b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2706b-129">CommonParameters</span></span>
<span data-ttu-id="2706b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2706b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2706b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2706b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2706b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2706b-132">INPUTS</span></span>

### <span data-ttu-id="2706b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2706b-133">-ResourceGroupName</span></span>
 <span data-ttu-id="2706b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2706b-134">System.String</span></span>

### <span data-ttu-id="2706b-135">-+ +</span><span class="sxs-lookup"><span data-stu-id="2706b-135">-NamespaceName</span></span>
 <span data-ttu-id="2706b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2706b-136">System.String</span></span>

### <span data-ttu-id="2706b-137">-Location</span><span class="sxs-lookup"><span data-stu-id="2706b-137">-Location</span></span>
 <span data-ttu-id="2706b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2706b-138">System.String</span></span>

### <span data-ttu-id="2706b-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2706b-139">-SkuName</span></span>
 <span data-ttu-id="2706b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2706b-140">System.String</span></span>

### <span data-ttu-id="2706b-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="2706b-141">-Tag</span></span>
 <span data-ttu-id="2706b-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2706b-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2706b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2706b-143">OUTPUTS</span></span>

### <span data-ttu-id="2706b-144">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2706b-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="2706b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2706b-145">NOTES</span></span>

## <span data-ttu-id="2706b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2706b-146">RELATED LINKS</span></span>

