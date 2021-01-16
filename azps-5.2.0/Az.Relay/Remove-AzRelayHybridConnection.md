---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409167"
---
# <span data-ttu-id="d181e-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="d181e-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="d181e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d181e-102">SYNOPSIS</span></span>
<span data-ttu-id="d181e-103">Удаляет Гибриднуюсоединение из указанного пространства имен HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="d181e-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="d181e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d181e-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d181e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d181e-105">DESCRIPTION</span></span>
<span data-ttu-id="d181e-106">Командлет **Remove-AzRelayHybridConnection** удаляет HybridConnection из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="d181e-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="d181e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d181e-107">EXAMPLES</span></span>

### <span data-ttu-id="d181e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d181e-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="d181e-109">Гибридное подключение удаляется `TestHybridConnection` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="d181e-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="d181e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d181e-110">PARAMETERS</span></span>

### <span data-ttu-id="d181e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d181e-111">-DefaultProfile</span></span>
<span data-ttu-id="d181e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d181e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d181e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d181e-113">-Name</span></span>
<span data-ttu-id="d181e-114">Имя HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="d181e-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="d181e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d181e-115">-Namespace</span></span>
<span data-ttu-id="d181e-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d181e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="d181e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d181e-117">-ResourceGroupName</span></span>
<span data-ttu-id="d181e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d181e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d181e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d181e-119">-Confirm</span></span>
<span data-ttu-id="d181e-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d181e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d181e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d181e-121">-WhatIf</span></span>
<span data-ttu-id="d181e-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d181e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d181e-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d181e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d181e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d181e-124">CommonParameters</span></span>
<span data-ttu-id="d181e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d181e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d181e-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d181e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d181e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d181e-127">INPUTS</span></span>

### <span data-ttu-id="d181e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d181e-128">System.String</span></span>

## <span data-ttu-id="d181e-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d181e-129">OUTPUTS</span></span>

### <span data-ttu-id="d181e-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d181e-130">System.Void</span></span>

## <span data-ttu-id="d181e-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d181e-131">NOTES</span></span>

## <span data-ttu-id="d181e-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d181e-132">RELATED LINKS</span></span>