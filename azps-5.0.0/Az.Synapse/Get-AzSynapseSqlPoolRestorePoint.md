---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245749"
---
# <span data-ttu-id="fba3a-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="fba3a-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="fba3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fba3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fba3a-103">Извлекает различные точки восстановления, из которых может быть восстановлен пул SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="fba3a-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="fba3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fba3a-104">SYNTAX</span></span>

### <span data-ttu-id="fba3a-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fba3a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba3a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba3a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba3a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba3a-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fba3a-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba3a-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fba3a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fba3a-109">DESCRIPTION</span></span>
<span data-ttu-id="fba3a-110">Командлет **Get-AzSynapseSqlPoolRestorePoint** извлекает отдельные точки восстановления, из которых может быть восстановлен пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fba3a-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="fba3a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fba3a-111">EXAMPLES</span></span>

### <span data-ttu-id="fba3a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fba3a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fba3a-113">Эта команда возвращает все доступные точки восстановления для пула SQL Azure Synapse Analytics с именем ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="fba3a-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="fba3a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fba3a-114">PARAMETERS</span></span>

### <span data-ttu-id="fba3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba3a-115">-DefaultProfile</span></span>
<span data-ttu-id="fba3a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fba3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba3a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fba3a-117">-InputObject</span></span>
<span data-ttu-id="fba3a-118">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fba3a-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fba3a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fba3a-119">-Name</span></span>
<span data-ttu-id="fba3a-120">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fba3a-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fba3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="fba3a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fba3a-122">Resource group name.</span></span>

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

### <span data-ttu-id="fba3a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba3a-123">-ResourceId</span></span>
<span data-ttu-id="fba3a-124">Идентификатор ресурса пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fba3a-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="fba3a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fba3a-125">-WorkspaceName</span></span>
<span data-ttu-id="fba3a-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fba3a-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fba3a-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fba3a-127">-WorkspaceObject</span></span>
<span data-ttu-id="fba3a-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fba3a-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fba3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba3a-129">CommonParameters</span></span>
<span data-ttu-id="fba3a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fba3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba3a-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fba3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba3a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fba3a-132">INPUTS</span></span>

### <span data-ttu-id="fba3a-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fba3a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fba3a-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fba3a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fba3a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fba3a-135">OUTPUTS</span></span>

### <span data-ttu-id="fba3a-136">Microsoft. Azure. Management. Synapse. Models. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="fba3a-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="fba3a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="fba3a-137">NOTES</span></span>

## <span data-ttu-id="fba3a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fba3a-138">RELATED LINKS</span></span>
