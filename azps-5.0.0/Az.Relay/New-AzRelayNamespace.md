---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317768"
---
# <span data-ttu-id="1ceec-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="1ceec-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="1ceec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ceec-102">SYNOPSIS</span></span>
<span data-ttu-id="1ceec-103">Создание нового пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1ceec-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="1ceec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ceec-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ceec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ceec-105">DESCRIPTION</span></span>
<span data-ttu-id="1ceec-106">Командлет **New-AzRelayNamespace** создает новое пространство имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1ceec-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="1ceec-107">Созданный манифест ресурсов пространства имен является неизменным.</span><span class="sxs-lookup"><span data-stu-id="1ceec-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="1ceec-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ceec-108">EXAMPLES</span></span>

### <span data-ttu-id="1ceec-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ceec-109">Example 1</span></span>
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

<span data-ttu-id="1ceec-110">Создание нового пространства имен ретрансляции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ceec-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="1ceec-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ceec-111">PARAMETERS</span></span>

### <span data-ttu-id="1ceec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ceec-112">-DefaultProfile</span></span>
<span data-ttu-id="1ceec-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ceec-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ceec-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1ceec-114">-Location</span></span>
<span data-ttu-id="1ceec-115">Расположение пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1ceec-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="1ceec-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ceec-116">-Name</span></span>
<span data-ttu-id="1ceec-117">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="1ceec-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="1ceec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ceec-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ceec-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ceec-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ceec-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="1ceec-120">-Tag</span></span>
<span data-ttu-id="1ceec-121">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ceec-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="1ceec-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ceec-122">-Confirm</span></span>
<span data-ttu-id="1ceec-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ceec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ceec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ceec-124">-WhatIf</span></span>
<span data-ttu-id="1ceec-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ceec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ceec-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ceec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ceec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ceec-127">CommonParameters</span></span>
<span data-ttu-id="1ceec-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ceec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ceec-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ceec-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ceec-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ceec-130">INPUTS</span></span>

### <span data-ttu-id="1ceec-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1ceec-131">System.String</span></span>

### <span data-ttu-id="1ceec-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ceec-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ceec-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ceec-133">OUTPUTS</span></span>

### <span data-ttu-id="1ceec-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1ceec-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="1ceec-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ceec-135">NOTES</span></span>

## <span data-ttu-id="1ceec-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ceec-136">RELATED LINKS</span></span>
