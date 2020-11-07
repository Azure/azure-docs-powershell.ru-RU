---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 19af1cf3ae051500a6515340b96792efa8dbbc17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720355"
---
# <span data-ttu-id="ddef3-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ddef3-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="ddef3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddef3-102">SYNOPSIS</span></span>
<span data-ttu-id="ddef3-103">Повторное создание ключа учетной записи пространственных привязок</span><span class="sxs-lookup"><span data-stu-id="ddef3-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="ddef3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddef3-104">SYNTAX</span></span>

### <span data-ttu-id="ddef3-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddef3-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddef3-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddef3-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddef3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddef3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddef3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddef3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddef3-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddef3-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddef3-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddef3-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddef3-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddef3-111">DESCRIPTION</span></span>
<span data-ttu-id="ddef3-112">Повторное создание первичного ключа или вторичного ключа учетной записи пространственных привязок.</span><span class="sxs-lookup"><span data-stu-id="ddef3-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="ddef3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddef3-113">EXAMPLES</span></span>

### <span data-ttu-id="ddef3-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddef3-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="ddef3-115">Повторное создание вторичного ключа учетной записи пространственного якоря "пример" в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="ddef3-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="ddef3-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ddef3-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ddef3-117">Повторное создание вторичного ключа учетной записи пространственного якоря "пример" из текущей подписки и группы ресурсов "Rg1" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="ddef3-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="ddef3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddef3-118">PARAMETERS</span></span>

### <span data-ttu-id="ddef3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddef3-119">-DefaultProfile</span></span>
<span data-ttu-id="ddef3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddef3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddef3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ddef3-121">-Force</span></span>
<span data-ttu-id="ddef3-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ddef3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddef3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddef3-123">-InputObject</span></span>
<span data-ttu-id="ddef3-124">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="ddef3-124">The custom domain object.</span></span>

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

### <span data-ttu-id="ddef3-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddef3-125">-Name</span></span>
<span data-ttu-id="ddef3-126">Имя учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="ddef3-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="ddef3-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="ddef3-127">-Primary</span></span>
<span data-ttu-id="ddef3-128">Повторное создание первичного ключа учетной записи пространственных привязок.</span><span class="sxs-lookup"><span data-stu-id="ddef3-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ddef3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddef3-129">-ResourceGroupName</span></span>
<span data-ttu-id="ddef3-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddef3-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ddef3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddef3-131">-ResourceId</span></span>
<span data-ttu-id="ddef3-132">Идентификатор ресурса учетной записи пространственного якоря.</span><span class="sxs-lookup"><span data-stu-id="ddef3-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ddef3-133">-Получатель</span><span class="sxs-lookup"><span data-stu-id="ddef3-133">-Secondary</span></span>
<span data-ttu-id="ddef3-134">Повторное создание первичного ключа учетной записи пространственных привязок.</span><span class="sxs-lookup"><span data-stu-id="ddef3-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ddef3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddef3-135">-Confirm</span></span>
<span data-ttu-id="ddef3-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddef3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddef3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddef3-137">-WhatIf</span></span>
<span data-ttu-id="ddef3-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddef3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddef3-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddef3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddef3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddef3-140">CommonParameters</span></span>
<span data-ttu-id="ddef3-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddef3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ddef3-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddef3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddef3-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddef3-143">INPUTS</span></span>

### <span data-ttu-id="ddef3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ddef3-144">System.String</span></span>

### <span data-ttu-id="ddef3-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="ddef3-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="ddef3-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddef3-146">OUTPUTS</span></span>

### <span data-ttu-id="ddef3-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ddef3-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="ddef3-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddef3-148">NOTES</span></span>

## <span data-ttu-id="ddef3-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddef3-149">RELATED LINKS</span></span>
