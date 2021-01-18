---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505981"
---
# <span data-ttu-id="9a143-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="9a143-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="9a143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a143-102">SYNOPSIS</span></span>
<span data-ttu-id="9a143-103">Удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="9a143-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="9a143-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a143-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a143-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a143-105">DESCRIPTION</span></span>
<span data-ttu-id="9a143-106">Командлет **Remove-AzWcfRelay** удаляет WcfRelay из указанного пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="9a143-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="9a143-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a143-107">EXAMPLES</span></span>

### <span data-ttu-id="9a143-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a143-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="9a143-109">Удаляет WcfRelay `TestWCFRelay1` из пространства `TestNameSpace-Relay1` имен.</span><span class="sxs-lookup"><span data-stu-id="9a143-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="9a143-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a143-110">PARAMETERS</span></span>

### <span data-ttu-id="9a143-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a143-111">-DefaultProfile</span></span>
<span data-ttu-id="9a143-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a143-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a143-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9a143-113">-Name</span></span>
<span data-ttu-id="9a143-114">Имя WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="9a143-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9a143-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a143-115">-Namespace</span></span>
<span data-ttu-id="9a143-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9a143-116">Namespace Name.</span></span>

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

### <span data-ttu-id="9a143-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a143-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a143-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a143-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="9a143-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a143-119">-Confirm</span></span>
<span data-ttu-id="9a143-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a143-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a143-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a143-121">-WhatIf</span></span>
<span data-ttu-id="9a143-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a143-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a143-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a143-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a143-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a143-124">CommonParameters</span></span>
<span data-ttu-id="9a143-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a143-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a143-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a143-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a143-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a143-127">INPUTS</span></span>

### <span data-ttu-id="9a143-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9a143-128">System.String</span></span>

## <span data-ttu-id="9a143-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a143-129">OUTPUTS</span></span>

### <span data-ttu-id="9a143-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="9a143-130">System.Void</span></span>

## <span data-ttu-id="9a143-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a143-131">NOTES</span></span>

## <span data-ttu-id="9a143-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a143-132">RELATED LINKS</span></span>
