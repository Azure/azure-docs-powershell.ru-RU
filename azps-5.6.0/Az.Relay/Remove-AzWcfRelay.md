---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f99a3a999baad580e04c6872f047c02d4a99091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000435"
---
# <span data-ttu-id="11ff8-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="11ff8-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="11ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="11ff8-103">Удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="11ff8-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="11ff8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11ff8-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ff8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="11ff8-106">Командлет **Remove-AzWcfRelay** удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="11ff8-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="11ff8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="11ff8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11ff8-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="11ff8-109">Удаляет WcfRelay `TestWCFRelay1` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="11ff8-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="11ff8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="11ff8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ff8-111">-DefaultProfile</span></span>
<span data-ttu-id="11ff8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11ff8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ff8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="11ff8-113">-Name</span></span>
<span data-ttu-id="11ff8-114">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="11ff8-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="11ff8-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11ff8-115">-Namespace</span></span>
<span data-ttu-id="11ff8-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="11ff8-116">Namespace Name.</span></span>

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

### <span data-ttu-id="11ff8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ff8-117">-ResourceGroupName</span></span>
<span data-ttu-id="11ff8-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11ff8-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="11ff8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11ff8-119">-Confirm</span></span>
<span data-ttu-id="11ff8-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ff8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ff8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ff8-121">-WhatIf</span></span>
<span data-ttu-id="11ff8-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ff8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ff8-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="11ff8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ff8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ff8-124">CommonParameters</span></span>
<span data-ttu-id="11ff8-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ff8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ff8-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ff8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ff8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11ff8-127">INPUTS</span></span>

### <span data-ttu-id="11ff8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="11ff8-128">System.String</span></span>

## <span data-ttu-id="11ff8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11ff8-129">OUTPUTS</span></span>

### <span data-ttu-id="11ff8-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="11ff8-130">System.Void</span></span>

## <span data-ttu-id="11ff8-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11ff8-131">NOTES</span></span>

## <span data-ttu-id="11ff8-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11ff8-132">RELATED LINKS</span></span>
