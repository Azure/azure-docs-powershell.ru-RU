---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c6f0fc3d8a0ef96a8b54b954e07fb1a9d1c644e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000504"
---
# <span data-ttu-id="a393f-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a393f-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="a393f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a393f-102">SYNOPSIS</span></span>
<span data-ttu-id="a393f-103">Создает новое пространство имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="a393f-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="a393f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a393f-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a393f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a393f-105">DESCRIPTION</span></span>
<span data-ttu-id="a393f-106">Командлет **New-AzRelayNamespace** создает новое пространство имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="a393f-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="a393f-107">После создания манифеста ресурсов пространства имен будет неанимабельным.</span><span class="sxs-lookup"><span data-stu-id="a393f-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="a393f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a393f-108">EXAMPLES</span></span>

### <span data-ttu-id="a393f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a393f-109">Example 1</span></span>
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

<span data-ttu-id="a393f-110">Создает новое пространство имен ретрансляции в пределах указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a393f-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="a393f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a393f-111">PARAMETERS</span></span>

### <span data-ttu-id="a393f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a393f-112">-DefaultProfile</span></span>
<span data-ttu-id="a393f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a393f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a393f-114">-Location</span><span class="sxs-lookup"><span data-stu-id="a393f-114">-Location</span></span>
<span data-ttu-id="a393f-115">Расположение пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="a393f-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="a393f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a393f-116">-Name</span></span>
<span data-ttu-id="a393f-117">Имя пространства ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="a393f-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a393f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a393f-118">-ResourceGroupName</span></span>
<span data-ttu-id="a393f-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a393f-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="a393f-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="a393f-120">-Tag</span></span>
<span data-ttu-id="a393f-121">Hashtables which represents resource Tags.</span><span class="sxs-lookup"><span data-stu-id="a393f-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="a393f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a393f-122">-Confirm</span></span>
<span data-ttu-id="a393f-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a393f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a393f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a393f-124">-WhatIf</span></span>
<span data-ttu-id="a393f-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a393f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a393f-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a393f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a393f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a393f-127">CommonParameters</span></span>
<span data-ttu-id="a393f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a393f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a393f-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a393f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a393f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a393f-130">INPUTS</span></span>

### <span data-ttu-id="a393f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a393f-131">System.String</span></span>

### <span data-ttu-id="a393f-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a393f-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a393f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a393f-133">OUTPUTS</span></span>

### <span data-ttu-id="a393f-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a393f-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="a393f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a393f-135">NOTES</span></span>

## <span data-ttu-id="a393f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a393f-136">RELATED LINKS</span></span>
