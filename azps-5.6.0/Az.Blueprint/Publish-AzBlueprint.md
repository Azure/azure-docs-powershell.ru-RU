---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: bc1ec66846037a7081af85809f2187b5d35aecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010835"
---
# <span data-ttu-id="a62ce-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a62ce-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="a62ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a62ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a62ce-103">Опубликуем новую версию документа.</span><span class="sxs-lookup"><span data-stu-id="a62ce-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="a62ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a62ce-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a62ce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a62ce-105">DESCRIPTION</span></span>
<span data-ttu-id="a62ce-106">Опубликуем новую версию определения схемы.</span><span class="sxs-lookup"><span data-stu-id="a62ce-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="a62ce-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a62ce-107">EXAMPLES</span></span>

### <span data-ttu-id="a62ce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a62ce-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="a62ce-109">Опубликуем новую версию определения схемы.</span><span class="sxs-lookup"><span data-stu-id="a62ce-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="a62ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a62ce-110">PARAMETERS</span></span>

### <span data-ttu-id="a62ce-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a62ce-111">-Blueprint</span></span>
<span data-ttu-id="a62ce-112">Объект Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a62ce-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ce-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="a62ce-113">-ChangeNote</span></span>
<span data-ttu-id="a62ce-114">Примечания, описывают содержимое этого документа.</span><span class="sxs-lookup"><span data-stu-id="a62ce-114">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62ce-115">-DefaultProfile</span></span>
<span data-ttu-id="a62ce-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a62ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a62ce-117">-Version</span><span class="sxs-lookup"><span data-stu-id="a62ce-117">-Version</span></span>
<span data-ttu-id="a62ce-118">Версия определения схемы.</span><span class="sxs-lookup"><span data-stu-id="a62ce-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="a62ce-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a62ce-119">-Confirm</span></span>
<span data-ttu-id="a62ce-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a62ce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a62ce-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a62ce-121">-WhatIf</span></span>
<span data-ttu-id="a62ce-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a62ce-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a62ce-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a62ce-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a62ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62ce-124">CommonParameters</span></span>
<span data-ttu-id="a62ce-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62ce-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a62ce-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62ce-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a62ce-127">INPUTS</span></span>

### <span data-ttu-id="a62ce-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a62ce-128">System.String</span></span>

### <span data-ttu-id="a62ce-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="a62ce-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="a62ce-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a62ce-130">OUTPUTS</span></span>

### <span data-ttu-id="a62ce-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBluePrint</span><span class="sxs-lookup"><span data-stu-id="a62ce-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="a62ce-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a62ce-132">NOTES</span></span>

## <span data-ttu-id="a62ce-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a62ce-133">RELATED LINKS</span></span>
