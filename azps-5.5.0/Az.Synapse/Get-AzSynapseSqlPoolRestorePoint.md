---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241709"
---
# <span data-ttu-id="59943-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="59943-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="59943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59943-102">SYNOPSIS</span></span>
<span data-ttu-id="59943-103">Извлекает отдельные точки восстановления, из которых SQL можно восстановить пул средств аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="59943-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="59943-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59943-104">SYNTAX</span></span>

### <span data-ttu-id="59943-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59943-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59943-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59943-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59943-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59943-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59943-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59943-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59943-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59943-109">DESCRIPTION</span></span>
<span data-ttu-id="59943-110">Для получения различных точек восстановления, из SQL Azure Synapse Analytics, извлекается SQL **Get-AzSynapseSqlPoolRestorePoint.**</span><span class="sxs-lookup"><span data-stu-id="59943-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="59943-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59943-111">EXAMPLES</span></span>

### <span data-ttu-id="59943-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59943-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="59943-113">Эта команда возвращает все доступные точки восстановления для пула Azure Synapse Analytics SQL ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="59943-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="59943-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59943-114">PARAMETERS</span></span>

### <span data-ttu-id="59943-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59943-115">-DefaultProfile</span></span>
<span data-ttu-id="59943-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59943-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59943-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59943-117">-InputObject</span></span>
<span data-ttu-id="59943-118">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="59943-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="59943-119">-Name</span><span class="sxs-lookup"><span data-stu-id="59943-119">-Name</span></span>
<span data-ttu-id="59943-120">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="59943-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="59943-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59943-121">-ResourceGroupName</span></span>
<span data-ttu-id="59943-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59943-122">Resource group name.</span></span>

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

### <span data-ttu-id="59943-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59943-123">-ResourceId</span></span>
<span data-ttu-id="59943-124">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="59943-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="59943-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59943-125">-WorkspaceName</span></span>
<span data-ttu-id="59943-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="59943-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="59943-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="59943-127">-WorkspaceObject</span></span>
<span data-ttu-id="59943-128">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="59943-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="59943-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59943-129">CommonParameters</span></span>
<span data-ttu-id="59943-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59943-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59943-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59943-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59943-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59943-132">INPUTS</span></span>

### <span data-ttu-id="59943-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="59943-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="59943-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="59943-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="59943-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59943-135">OUTPUTS</span></span>

### <span data-ttu-id="59943-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="59943-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="59943-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59943-137">NOTES</span></span>

## <span data-ttu-id="59943-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59943-138">RELATED LINKS</span></span>
