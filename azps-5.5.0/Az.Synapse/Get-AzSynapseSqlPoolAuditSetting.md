---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229684"
---
# <span data-ttu-id="38d42-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="38d42-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="38d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d42-102">SYNOPSIS</span></span>
<span data-ttu-id="38d42-103">Настраивает параметры аудита пула azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="38d42-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="38d42-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38d42-104">SYNTAX</span></span>

### <span data-ttu-id="38d42-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38d42-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d42-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38d42-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d42-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38d42-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38d42-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38d42-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38d42-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38d42-109">DESCRIPTION</span></span>
<span data-ttu-id="38d42-110">Для **этого** с его SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="38d42-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="38d42-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38d42-111">EXAMPLES</span></span>

### <span data-ttu-id="38d42-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38d42-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="38d42-113">Эта команда получает параметры аудита для пула contosoSqlPool SQL под названием ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="38d42-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="38d42-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="38d42-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="38d42-115">Эта команда получает параметры аудита пула SQL ContosoSqlPool в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="38d42-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="38d42-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d42-116">PARAMETERS</span></span>

### <span data-ttu-id="38d42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d42-117">-DefaultProfile</span></span>
<span data-ttu-id="38d42-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38d42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d42-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38d42-119">-InputObject</span></span>
<span data-ttu-id="38d42-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="38d42-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="38d42-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38d42-121">-Name</span></span>
<span data-ttu-id="38d42-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="38d42-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="38d42-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d42-123">-ResourceGroupName</span></span>
<span data-ttu-id="38d42-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38d42-124">Resource group name.</span></span>

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

### <span data-ttu-id="38d42-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38d42-125">-ResourceId</span></span>
<span data-ttu-id="38d42-126">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="38d42-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="38d42-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38d42-127">-WorkspaceName</span></span>
<span data-ttu-id="38d42-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="38d42-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="38d42-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="38d42-129">-WorkspaceObject</span></span>
<span data-ttu-id="38d42-130">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="38d42-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="38d42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d42-131">CommonParameters</span></span>
<span data-ttu-id="38d42-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d42-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38d42-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d42-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38d42-134">INPUTS</span></span>

### <span data-ttu-id="38d42-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="38d42-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="38d42-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="38d42-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="38d42-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38d42-137">OUTPUTS</span></span>

### <span data-ttu-id="38d42-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="38d42-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="38d42-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38d42-139">NOTES</span></span>

## <span data-ttu-id="38d42-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38d42-140">RELATED LINKS</span></span>
