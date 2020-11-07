---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: 37e641516ffc21a0984f97cb84f94d2564033fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729504"
---
# <span data-ttu-id="92d94-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="92d94-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="92d94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92d94-102">SYNOPSIS</span></span>
<span data-ttu-id="92d94-103">Создание нового пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="92d94-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="92d94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92d94-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d94-105">DESCRIPTION</span></span>
<span data-ttu-id="92d94-106">Командлет **New-AzRelayNamespace** создает новое пространство имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="92d94-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="92d94-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="92d94-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="92d94-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92d94-108">EXAMPLES</span></span>

### <span data-ttu-id="92d94-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92d94-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="92d94-110">Создание нового пространства имен ретрансляции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92d94-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="92d94-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92d94-111">PARAMETERS</span></span>

### <span data-ttu-id="92d94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d94-112">-DefaultProfile</span></span>
<span data-ttu-id="92d94-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92d94-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d94-114">-Location</span><span class="sxs-lookup"><span data-stu-id="92d94-114">-Location</span></span>
<span data-ttu-id="92d94-115">Расположение пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="92d94-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="92d94-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92d94-116">-Name</span></span>
<span data-ttu-id="92d94-117">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="92d94-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="92d94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d94-118">-ResourceGroupName</span></span>
<span data-ttu-id="92d94-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92d94-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="92d94-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="92d94-120">-Tag</span></span>
<span data-ttu-id="92d94-121">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92d94-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="92d94-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92d94-122">-Confirm</span></span>
<span data-ttu-id="92d94-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92d94-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d94-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d94-124">-WhatIf</span></span>
<span data-ttu-id="92d94-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92d94-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92d94-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92d94-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d94-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d94-127">CommonParameters</span></span>
<span data-ttu-id="92d94-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92d94-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d94-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d94-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d94-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92d94-130">INPUTS</span></span>

### <span data-ttu-id="92d94-131">System. String</span><span class="sxs-lookup"><span data-stu-id="92d94-131">System.String</span></span>

### <span data-ttu-id="92d94-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92d94-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="92d94-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d94-133">OUTPUTS</span></span>

### <span data-ttu-id="92d94-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="92d94-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="92d94-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="92d94-135">NOTES</span></span>

## <span data-ttu-id="92d94-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92d94-136">RELATED LINKS</span></span>
