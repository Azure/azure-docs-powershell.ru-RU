---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424404"
---
# <span data-ttu-id="8d2bf-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="8d2bf-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="8d2bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2bf-103">Настраивает параметры аудита пула azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8d2bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d2bf-104">SYNTAX</span></span>

### <span data-ttu-id="8d2bf-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d2bf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d2bf-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d2bf-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d2bf-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d2bf-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d2bf-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d2bf-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d2bf-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d2bf-109">DESCRIPTION</span></span>
<span data-ttu-id="8d2bf-110">Для **этого** с его SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8d2bf-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d2bf-111">EXAMPLES</span></span>

### <span data-ttu-id="8d2bf-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d2bf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="8d2bf-113">Эта команда получает параметры аудита для пула contosoSqlPool SQL под названием ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="8d2bf-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d2bf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="8d2bf-115">Эта команда получает параметры аудита пула SQL ContosoSqlPool в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8d2bf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d2bf-116">PARAMETERS</span></span>

### <span data-ttu-id="8d2bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2bf-117">-DefaultProfile</span></span>
<span data-ttu-id="8d2bf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d2bf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2bf-119">-InputObject</span></span>
<span data-ttu-id="8d2bf-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8d2bf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d2bf-121">-Name</span></span>
<span data-ttu-id="8d2bf-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="8d2bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d2bf-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-124">Resource group name.</span></span>

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

### <span data-ttu-id="8d2bf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d2bf-125">-ResourceId</span></span>
<span data-ttu-id="8d2bf-126">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="8d2bf-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8d2bf-127">-WorkspaceName</span></span>
<span data-ttu-id="8d2bf-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8d2bf-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8d2bf-129">-WorkspaceObject</span></span>
<span data-ttu-id="8d2bf-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8d2bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2bf-131">CommonParameters</span></span>
<span data-ttu-id="8d2bf-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d2bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2bf-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d2bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2bf-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d2bf-134">INPUTS</span></span>

### <span data-ttu-id="8d2bf-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d2bf-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8d2bf-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8d2bf-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8d2bf-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d2bf-137">OUTPUTS</span></span>

### <span data-ttu-id="8d2bf-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="8d2bf-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="8d2bf-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d2bf-139">NOTES</span></span>

## <span data-ttu-id="8d2bf-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d2bf-140">RELATED LINKS</span></span>
