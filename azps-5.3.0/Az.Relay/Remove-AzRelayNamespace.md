---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421095"
---
# <span data-ttu-id="f5296-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="f5296-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="f5296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5296-102">SYNOPSIS</span></span>
<span data-ttu-id="f5296-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5296-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="f5296-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5296-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5296-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5296-105">DESCRIPTION</span></span>
<span data-ttu-id="f5296-106">При **этом из указанной** группы ресурсов удаляется пространство имен.</span><span class="sxs-lookup"><span data-stu-id="f5296-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="f5296-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5296-107">EXAMPLES</span></span>

### <span data-ttu-id="f5296-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5296-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="f5296-109">Удаляет пространство имен ретрансляции из указанной группы `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5296-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="f5296-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5296-110">PARAMETERS</span></span>

### <span data-ttu-id="f5296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5296-111">-DefaultProfile</span></span>
<span data-ttu-id="f5296-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5296-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5296-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f5296-113">-Name</span></span>
<span data-ttu-id="f5296-114">Имя пространства ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="f5296-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="f5296-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5296-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5296-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5296-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="f5296-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5296-117">-Confirm</span></span>
<span data-ttu-id="f5296-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f5296-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5296-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5296-119">-WhatIf</span></span>
<span data-ttu-id="f5296-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5296-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5296-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f5296-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5296-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5296-122">CommonParameters</span></span>
<span data-ttu-id="f5296-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5296-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5296-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5296-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5296-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5296-125">INPUTS</span></span>

### <span data-ttu-id="f5296-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f5296-126">System.String</span></span>

## <span data-ttu-id="f5296-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5296-127">OUTPUTS</span></span>

### <span data-ttu-id="f5296-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="f5296-128">System.Void</span></span>

## <span data-ttu-id="f5296-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5296-129">NOTES</span></span>

## <span data-ttu-id="f5296-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5296-130">RELATED LINKS</span></span>
