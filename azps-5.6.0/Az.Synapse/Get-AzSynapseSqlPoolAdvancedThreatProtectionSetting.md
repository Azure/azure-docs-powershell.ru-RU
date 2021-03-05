---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c706de537f4d95603399540342bd3ad52d2b30fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015672"
---
# <span data-ttu-id="c14e8-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="c14e8-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="c14e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c14e8-103">Получает дополнительные параметры защиты от угроз для SQL пула.</span><span class="sxs-lookup"><span data-stu-id="c14e8-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="c14e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c14e8-104">SYNTAX</span></span>

### <span data-ttu-id="c14e8-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c14e8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14e8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14e8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14e8-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14e8-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c14e8-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14e8-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c14e8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c14e8-109">DESCRIPTION</span></span>
<span data-ttu-id="c14e8-110">Для пула Azure Synapse Analytics можно получить расширенные параметры защиты от SQL Synapse Analytics для **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="c14e8-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c14e8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c14e8-111">EXAMPLES</span></span>

### <span data-ttu-id="c14e8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c14e8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c14e8-113">Эта команда получает расширенные параметры защиты от угроз для SQL contosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c14e8-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c14e8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c14e8-114">PARAMETERS</span></span>

### <span data-ttu-id="c14e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14e8-115">-DefaultProfile</span></span>
<span data-ttu-id="c14e8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c14e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14e8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14e8-117">-InputObject</span></span>
<span data-ttu-id="c14e8-118">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="c14e8-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c14e8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c14e8-119">-Name</span></span>
<span data-ttu-id="c14e8-120">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c14e8-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="c14e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="c14e8-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c14e8-122">Resource group name.</span></span>

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

### <span data-ttu-id="c14e8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c14e8-123">-ResourceId</span></span>
<span data-ttu-id="c14e8-124">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c14e8-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="c14e8-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c14e8-125">-WorkspaceName</span></span>
<span data-ttu-id="c14e8-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c14e8-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c14e8-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c14e8-127">-WorkspaceObject</span></span>
<span data-ttu-id="c14e8-128">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="c14e8-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c14e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14e8-129">CommonParameters</span></span>
<span data-ttu-id="c14e8-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14e8-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c14e8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14e8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c14e8-132">INPUTS</span></span>

### <span data-ttu-id="c14e8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c14e8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c14e8-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c14e8-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c14e8-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c14e8-135">OUTPUTS</span></span>

### <span data-ttu-id="c14e8-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="c14e8-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="c14e8-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c14e8-137">NOTES</span></span>

## <span data-ttu-id="c14e8-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c14e8-138">RELATED LINKS</span></span>
