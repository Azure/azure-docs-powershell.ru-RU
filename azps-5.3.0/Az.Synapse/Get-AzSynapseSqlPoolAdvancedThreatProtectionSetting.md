---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424415"
---
# <span data-ttu-id="623fe-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="623fe-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="623fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="623fe-102">SYNOPSIS</span></span>
<span data-ttu-id="623fe-103">Получает дополнительные параметры защиты от угроз для SQL пула.</span><span class="sxs-lookup"><span data-stu-id="623fe-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="623fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="623fe-104">SYNTAX</span></span>

### <span data-ttu-id="623fe-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="623fe-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="623fe-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="623fe-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="623fe-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="623fe-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="623fe-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="623fe-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="623fe-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="623fe-109">DESCRIPTION</span></span>
<span data-ttu-id="623fe-110">Для пула Azure Synapse Analytics можно получить расширенные параметры защиты от SQL Synapse Analytics для **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="623fe-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="623fe-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="623fe-111">EXAMPLES</span></span>

### <span data-ttu-id="623fe-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="623fe-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="623fe-113">Эта команда получает расширенные параметры защиты от угроз для SQL contosoSqlPool в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="623fe-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="623fe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="623fe-114">PARAMETERS</span></span>

### <span data-ttu-id="623fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623fe-115">-DefaultProfile</span></span>
<span data-ttu-id="623fe-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="623fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="623fe-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="623fe-117">-InputObject</span></span>
<span data-ttu-id="623fe-118">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="623fe-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623fe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="623fe-119">-Name</span></span>
<span data-ttu-id="623fe-120">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="623fe-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="623fe-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="623fe-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623fe-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="623fe-123">-ResourceId</span></span>
<span data-ttu-id="623fe-124">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="623fe-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623fe-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="623fe-125">-WorkspaceName</span></span>
<span data-ttu-id="623fe-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="623fe-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623fe-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="623fe-127">-WorkspaceObject</span></span>
<span data-ttu-id="623fe-128">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="623fe-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623fe-129">CommonParameters</span></span>
<span data-ttu-id="623fe-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623fe-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="623fe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623fe-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="623fe-132">INPUTS</span></span>

### <span data-ttu-id="623fe-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="623fe-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="623fe-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="623fe-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="623fe-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="623fe-135">OUTPUTS</span></span>

### <span data-ttu-id="623fe-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="623fe-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="623fe-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="623fe-137">NOTES</span></span>

## <span data-ttu-id="623fe-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="623fe-138">RELATED LINKS</span></span>
