---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400804"
---
# <span data-ttu-id="9e944-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e944-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="9e944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e944-102">SYNOPSIS</span></span>
<span data-ttu-id="9e944-103">Повторное сгенерировать ключ учетной записи пространственной привязки</span><span class="sxs-lookup"><span data-stu-id="9e944-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="9e944-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e944-104">SYNTAX</span></span>

### <span data-ttu-id="9e944-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e944-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e944-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e944-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e944-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e944-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e944-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e944-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e944-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e944-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e944-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e944-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e944-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e944-111">DESCRIPTION</span></span>
<span data-ttu-id="9e944-112">Повторно сгенерировать первичный ключ или дополнительный ключ учетной записи пространственных привязки.</span><span class="sxs-lookup"><span data-stu-id="9e944-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="9e944-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e944-113">EXAMPLES</span></span>

### <span data-ttu-id="9e944-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e944-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="9e944-115">Повторно сгенерировать дополнительный ключ учетной записи пространственной привязки "example" в группе ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="9e944-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="9e944-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e944-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="9e944-117">Повторно сгенерировать дополнительный ключ учетной записи пространственой привязки "example" из текущей подписки и группы ресурсов "rg1" с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="9e944-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="9e944-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e944-118">PARAMETERS</span></span>

### <span data-ttu-id="9e944-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e944-119">-DefaultProfile</span></span>
<span data-ttu-id="9e944-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e944-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e944-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9e944-121">-Force</span></span>
<span data-ttu-id="9e944-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9e944-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e944-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e944-123">-InputObject</span></span>
<span data-ttu-id="9e944-124">Объект пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="9e944-124">The custom domain object.</span></span>

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

### <span data-ttu-id="9e944-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9e944-125">-Name</span></span>
<span data-ttu-id="9e944-126">Имя учетной записи с пространственными привязками.</span><span class="sxs-lookup"><span data-stu-id="9e944-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="9e944-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="9e944-127">-Primary</span></span>
<span data-ttu-id="9e944-128">Повторно сгенерировать первичный ключ учетной записи пространственных привязки.</span><span class="sxs-lookup"><span data-stu-id="9e944-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9e944-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e944-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e944-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e944-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e944-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e944-131">-ResourceId</span></span>
<span data-ttu-id="9e944-132">ИД ресурса учетной записи пространственной привязки.</span><span class="sxs-lookup"><span data-stu-id="9e944-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9e944-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="9e944-133">-Secondary</span></span>
<span data-ttu-id="9e944-134">Повторно сгенерировать первичный ключ учетной записи пространственных привязки.</span><span class="sxs-lookup"><span data-stu-id="9e944-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9e944-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e944-135">-Confirm</span></span>
<span data-ttu-id="9e944-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e944-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e944-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e944-137">-WhatIf</span></span>
<span data-ttu-id="9e944-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e944-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e944-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9e944-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e944-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e944-140">CommonParameters</span></span>
<span data-ttu-id="9e944-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e944-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e944-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e944-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e944-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e944-143">INPUTS</span></span>

### <span data-ttu-id="9e944-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9e944-144">System.String</span></span>

### <span data-ttu-id="9e944-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="9e944-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="9e944-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e944-146">OUTPUTS</span></span>

### <span data-ttu-id="9e944-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9e944-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="9e944-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e944-148">NOTES</span></span>

## <span data-ttu-id="9e944-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e944-149">RELATED LINKS</span></span>
