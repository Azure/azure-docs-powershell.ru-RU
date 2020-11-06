---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562216"
---
# <span data-ttu-id="415e4-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="415e4-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="415e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="415e4-102">SYNOPSIS</span></span>
<span data-ttu-id="415e4-103">Обновляет описание существующего пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="415e4-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="415e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="415e4-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="415e4-105">DESCRIPTION</span></span>
<span data-ttu-id="415e4-106">Командлет **Set-AzureRmRelayNamespace** обновляет описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415e4-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="415e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="415e4-107">EXAMPLES</span></span>

### <span data-ttu-id="415e4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="415e4-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="415e4-109">Обновляет пространство имен ретрансляции с помощью нового описания.</span><span class="sxs-lookup"><span data-stu-id="415e4-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="415e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="415e4-110">PARAMETERS</span></span>

### <span data-ttu-id="415e4-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415e4-111">-ResourceGroupName</span></span>
<span data-ttu-id="415e4-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="415e4-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="415e4-113">-Тег</span><span class="sxs-lookup"><span data-stu-id="415e4-113">-Tag</span></span>
<span data-ttu-id="415e4-114">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="415e4-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="415e4-115">Например:</span><span class="sxs-lookup"><span data-stu-id="415e4-115">For example:</span></span>

<span data-ttu-id="415e4-116">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="415e4-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="415e4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="415e4-117">-Confirm</span></span>
<span data-ttu-id="415e4-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="415e4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415e4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415e4-119">-WhatIf</span></span>
<span data-ttu-id="415e4-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="415e4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415e4-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="415e4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415e4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415e4-122">-DefaultProfile</span></span>
<span data-ttu-id="415e4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="415e4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="415e4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="415e4-124">-InputObject</span></span>
<span data-ttu-id="415e4-125">Объект пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="415e4-125">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="415e4-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="415e4-126">-Name</span></span>
<span data-ttu-id="415e4-127">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="415e4-127">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="415e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415e4-128">CommonParameters</span></span>
<span data-ttu-id="415e4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="415e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415e4-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415e4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415e4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="415e4-131">INPUTS</span></span>

### <span data-ttu-id="415e4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415e4-132">-ResourceGroupName</span></span>
 <span data-ttu-id="415e4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="415e4-133">System.String</span></span>

### <span data-ttu-id="415e4-134">-+ +</span><span class="sxs-lookup"><span data-stu-id="415e4-134">-NamespaceName</span></span>
 <span data-ttu-id="415e4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="415e4-135">System.String</span></span>

### <span data-ttu-id="415e4-136">-Location</span><span class="sxs-lookup"><span data-stu-id="415e4-136">-Location</span></span>
 <span data-ttu-id="415e4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="415e4-137">System.String</span></span>

### <span data-ttu-id="415e4-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="415e4-138">-Tag</span></span>
 <span data-ttu-id="415e4-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="415e4-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="415e4-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="415e4-140">OUTPUTS</span></span>

### <span data-ttu-id="415e4-141">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="415e4-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="415e4-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="415e4-142">NOTES</span></span>

## <span data-ttu-id="415e4-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="415e4-143">RELATED LINKS</span></span>

