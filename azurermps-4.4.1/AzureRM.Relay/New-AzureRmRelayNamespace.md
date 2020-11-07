---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 365a80e1ddf5673be5c45c5d17b24490c277a365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733636"
---
# <span data-ttu-id="e8933-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="e8933-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="e8933-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8933-102">SYNOPSIS</span></span>
<span data-ttu-id="e8933-103">Создание нового пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e8933-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8933-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8933-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8933-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8933-105">DESCRIPTION</span></span>
<span data-ttu-id="e8933-106">Командлет **New-AzureRmRelayNamespace** создает новое пространство имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e8933-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="e8933-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="e8933-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="e8933-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8933-108">EXAMPLES</span></span>

### <span data-ttu-id="e8933-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8933-109">Example 1</span></span>
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

<span data-ttu-id="e8933-110">Создание нового пространства имен ретрансляции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8933-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="e8933-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8933-111">PARAMETERS</span></span>

### <span data-ttu-id="e8933-112">-Location</span><span class="sxs-lookup"><span data-stu-id="e8933-112">-Location</span></span>
<span data-ttu-id="e8933-113">Расположение пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e8933-113">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8933-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8933-114">-ResourceGroupName</span></span>
<span data-ttu-id="e8933-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8933-115">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8933-116">-Тег</span><span class="sxs-lookup"><span data-stu-id="e8933-116">-Tag</span></span>
<span data-ttu-id="e8933-117">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e8933-117">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e8933-118">Например:</span><span class="sxs-lookup"><span data-stu-id="e8933-118">For example:</span></span>

<span data-ttu-id="e8933-119">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e8933-119">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e8933-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8933-120">-Confirm</span></span>
<span data-ttu-id="e8933-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8933-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8933-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8933-122">-WhatIf</span></span>
<span data-ttu-id="e8933-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8933-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8933-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8933-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8933-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8933-125">-DefaultProfile</span></span>
<span data-ttu-id="e8933-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8933-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8933-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8933-127">-Name</span></span>
<span data-ttu-id="e8933-128">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e8933-128">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8933-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8933-129">CommonParameters</span></span>
<span data-ttu-id="e8933-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8933-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8933-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8933-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8933-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8933-132">INPUTS</span></span>

### <span data-ttu-id="e8933-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8933-133">-ResourceGroupName</span></span>
 <span data-ttu-id="e8933-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e8933-134">System.String</span></span>

### <span data-ttu-id="e8933-135">-+ +</span><span class="sxs-lookup"><span data-stu-id="e8933-135">-NamespaceName</span></span>
 <span data-ttu-id="e8933-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e8933-136">System.String</span></span>

### <span data-ttu-id="e8933-137">-Location</span><span class="sxs-lookup"><span data-stu-id="e8933-137">-Location</span></span>
 <span data-ttu-id="e8933-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e8933-138">System.String</span></span>

### <span data-ttu-id="e8933-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e8933-139">-SkuName</span></span>
 <span data-ttu-id="e8933-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e8933-140">System.String</span></span>

### <span data-ttu-id="e8933-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="e8933-141">-Tag</span></span>
 <span data-ttu-id="e8933-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8933-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8933-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8933-143">OUTPUTS</span></span>

### <span data-ttu-id="e8933-144">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e8933-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="e8933-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8933-145">NOTES</span></span>

## <span data-ttu-id="e8933-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8933-146">RELATED LINKS</span></span>

