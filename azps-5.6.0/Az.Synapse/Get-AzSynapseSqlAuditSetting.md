---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: cf32bea3942c89b408592778657e5ecffae2acd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015699"
---
# <span data-ttu-id="69e66-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="69e66-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="69e66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69e66-102">SYNOPSIS</span></span>
<span data-ttu-id="69e66-103">Параметры аудита рабочей области аналитики Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="69e66-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="69e66-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69e66-104">SYNTAX</span></span>

### <span data-ttu-id="69e66-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69e66-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69e66-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69e66-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69e66-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69e66-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69e66-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69e66-108">DESCRIPTION</span></span>
<span data-ttu-id="69e66-109">Для параметра аудита рабочей области Azure Synapse Analytics задаются параметры аудита для **get-AzSynapseSqlAuditSetting.**</span><span class="sxs-lookup"><span data-stu-id="69e66-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="69e66-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69e66-110">EXAMPLES</span></span>

### <span data-ttu-id="69e66-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69e66-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="69e66-112">Параметры аудита рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="69e66-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="69e66-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="69e66-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="69e66-114">Параметры аудита рабочей области ContosoWorkspace проходят через канал.</span><span class="sxs-lookup"><span data-stu-id="69e66-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="69e66-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69e66-115">PARAMETERS</span></span>

### <span data-ttu-id="69e66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e66-116">-DefaultProfile</span></span>
<span data-ttu-id="69e66-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69e66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e66-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69e66-118">-InputObject</span></span>
<span data-ttu-id="69e66-119">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="69e66-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69e66-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e66-120">-ResourceGroupName</span></span>
<span data-ttu-id="69e66-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69e66-121">Resource group name.</span></span>

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

### <span data-ttu-id="69e66-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69e66-122">-ResourceId</span></span>
<span data-ttu-id="69e66-123">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="69e66-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="69e66-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69e66-124">-WorkspaceName</span></span>
<span data-ttu-id="69e66-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="69e66-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="69e66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e66-126">CommonParameters</span></span>
<span data-ttu-id="69e66-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e66-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69e66-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e66-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69e66-129">INPUTS</span></span>

### <span data-ttu-id="69e66-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="69e66-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="69e66-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69e66-131">OUTPUTS</span></span>

### <span data-ttu-id="69e66-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="69e66-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="69e66-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69e66-133">NOTES</span></span>

## <span data-ttu-id="69e66-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69e66-134">RELATED LINKS</span></span>
