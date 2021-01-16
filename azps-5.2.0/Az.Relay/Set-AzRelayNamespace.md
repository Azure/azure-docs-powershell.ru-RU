---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325811"
---
# <span data-ttu-id="e5a94-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="e5a94-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="e5a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a94-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a94-103">Обновляет описание существующего пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e5a94-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="e5a94-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5a94-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a94-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5a94-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a94-106">Командлет **Set-AzRelayNamespace** обновляет описание указанного пространства имен ретрансляции в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5a94-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="e5a94-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5a94-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a94-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5a94-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="e5a94-109">Обновляет пространство имен ретрансляции с новым описанием.</span><span class="sxs-lookup"><span data-stu-id="e5a94-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="e5a94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5a94-110">PARAMETERS</span></span>

### <span data-ttu-id="e5a94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a94-111">-DefaultProfile</span></span>
<span data-ttu-id="e5a94-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a94-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a94-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5a94-113">-InputObject</span></span>
<span data-ttu-id="e5a94-114">Объект Relay Namespace.</span><span class="sxs-lookup"><span data-stu-id="e5a94-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="e5a94-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a94-115">-Name</span></span>
<span data-ttu-id="e5a94-116">Имя пространства ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="e5a94-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="e5a94-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a94-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5a94-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5a94-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="e5a94-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5a94-119">-Tag</span></span>
<span data-ttu-id="e5a94-120">Hashtables which represents resource Tag.</span><span class="sxs-lookup"><span data-stu-id="e5a94-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="e5a94-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5a94-121">-Confirm</span></span>
<span data-ttu-id="e5a94-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a94-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a94-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a94-123">-WhatIf</span></span>
<span data-ttu-id="e5a94-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a94-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a94-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5a94-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a94-126">CommonParameters</span></span>
<span data-ttu-id="e5a94-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a94-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a94-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a94-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5a94-129">INPUTS</span></span>

### <span data-ttu-id="e5a94-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e5a94-130">System.String</span></span>

### <span data-ttu-id="e5a94-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5a94-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e5a94-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="e5a94-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="e5a94-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5a94-133">OUTPUTS</span></span>

### <span data-ttu-id="e5a94-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e5a94-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="e5a94-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5a94-135">NOTES</span></span>

## <span data-ttu-id="e5a94-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5a94-136">RELATED LINKS</span></span>
