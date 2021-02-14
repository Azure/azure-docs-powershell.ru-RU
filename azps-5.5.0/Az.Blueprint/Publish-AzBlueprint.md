---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234972"
---
# <span data-ttu-id="cd2f6-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="cd2f6-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="cd2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2f6-103">Опубликуем новую версию документа.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="cd2f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd2f6-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd2f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="cd2f6-106">Опубликуем новую версию определения схемы.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="cd2f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="cd2f6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd2f6-108">Example 1</span></span>
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

<span data-ttu-id="cd2f6-109">Опубликуем новую версию определения схемы.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="cd2f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd2f6-110">PARAMETERS</span></span>

### <span data-ttu-id="cd2f6-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="cd2f6-111">-Blueprint</span></span>
<span data-ttu-id="cd2f6-112">Объект Blueprint.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-112">Blueprint object.</span></span>

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

### <span data-ttu-id="cd2f6-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="cd2f6-113">-ChangeNote</span></span>
<span data-ttu-id="cd2f6-114">Примечания, описывают содержимое этой версии документа.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="cd2f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2f6-115">-DefaultProfile</span></span>
<span data-ttu-id="cd2f6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd2f6-117">-Версия</span><span class="sxs-lookup"><span data-stu-id="cd2f6-117">-Version</span></span>
<span data-ttu-id="cd2f6-118">Версия определения схемы.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="cd2f6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd2f6-119">-Confirm</span></span>
<span data-ttu-id="cd2f6-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2f6-121">-WhatIf</span></span>
<span data-ttu-id="cd2f6-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd2f6-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2f6-124">CommonParameters</span></span>
<span data-ttu-id="cd2f6-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd2f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2f6-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd2f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2f6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd2f6-127">INPUTS</span></span>

### <span data-ttu-id="cd2f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cd2f6-128">System.String</span></span>

### <span data-ttu-id="cd2f6-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="cd2f6-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="cd2f6-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd2f6-130">OUTPUTS</span></span>

### <span data-ttu-id="cd2f6-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBluePrint</span><span class="sxs-lookup"><span data-stu-id="cd2f6-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="cd2f6-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd2f6-132">NOTES</span></span>

## <span data-ttu-id="cd2f6-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd2f6-133">RELATED LINKS</span></span>
