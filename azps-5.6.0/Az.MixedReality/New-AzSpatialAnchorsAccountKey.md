---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 7c94b9fd1395af8b64425837d1fb08c578b3c2a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010456"
---
# <span data-ttu-id="fba34-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="fba34-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="fba34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba34-102">SYNOPSIS</span></span>
<span data-ttu-id="fba34-103">Повторное сгенерировать ключ учетной записи пространственной привязки</span><span class="sxs-lookup"><span data-stu-id="fba34-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="fba34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fba34-104">SYNTAX</span></span>

### <span data-ttu-id="fba34-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba34-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba34-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba34-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba34-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba34-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba34-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba34-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba34-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba34-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba34-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba34-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fba34-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fba34-111">DESCRIPTION</span></span>
<span data-ttu-id="fba34-112">Повторно сгенерировать первичный ключ или дополнительный ключ учетной записи пространственных привязки.</span><span class="sxs-lookup"><span data-stu-id="fba34-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="fba34-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fba34-113">EXAMPLES</span></span>

### <span data-ttu-id="fba34-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fba34-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="fba34-115">Повторно сгенерировать дополнительный ключ учетной записи пространственой привязки "example" в группе ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="fba34-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="fba34-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fba34-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="fba34-117">Повторно сгенерировать дополнительный ключ учетной записи пространственой привязки "example" из текущей подписки и группы ресурсов "rg1" с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="fba34-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="fba34-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fba34-118">PARAMETERS</span></span>

### <span data-ttu-id="fba34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba34-119">-DefaultProfile</span></span>
<span data-ttu-id="fba34-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fba34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fba34-121">-Force</span></span>
<span data-ttu-id="fba34-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="fba34-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fba34-123">-InputObject</span></span>
<span data-ttu-id="fba34-124">Объект пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="fba34-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fba34-125">-Name</span></span>
<span data-ttu-id="fba34-126">Имя учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="fba34-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="fba34-127">-Primary</span></span>
<span data-ttu-id="fba34-128">Повторно сгенерировать первичный ключ учетной записи пространственных привязки.</span><span class="sxs-lookup"><span data-stu-id="fba34-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba34-129">-ResourceGroupName</span></span>
<span data-ttu-id="fba34-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fba34-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba34-131">-ResourceId</span></span>
<span data-ttu-id="fba34-132">ИД ресурса учетной записи пространственной привязки.</span><span class="sxs-lookup"><span data-stu-id="fba34-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="fba34-133">-Secondary</span></span>
<span data-ttu-id="fba34-134">Повторно сгенерировать первичный ключ учетной записи пространственных привязки.</span><span class="sxs-lookup"><span data-stu-id="fba34-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba34-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fba34-135">-Confirm</span></span>
<span data-ttu-id="fba34-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fba34-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba34-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fba34-137">-WhatIf</span></span>
<span data-ttu-id="fba34-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fba34-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fba34-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fba34-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba34-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba34-140">CommonParameters</span></span>
<span data-ttu-id="fba34-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba34-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fba34-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba34-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba34-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fba34-143">INPUTS</span></span>

### <span data-ttu-id="fba34-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fba34-144">System.String</span></span>

### <span data-ttu-id="fba34-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="fba34-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="fba34-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fba34-146">OUTPUTS</span></span>

### <span data-ttu-id="fba34-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fba34-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="fba34-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fba34-148">NOTES</span></span>

## <span data-ttu-id="fba34-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fba34-149">RELATED LINKS</span></span>
