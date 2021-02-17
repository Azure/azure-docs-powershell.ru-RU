---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241717"
---
# <span data-ttu-id="74a18-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="74a18-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="74a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74a18-102">SYNOPSIS</span></span>
<span data-ttu-id="74a18-103">Параметры аудита рабочей области аналитики Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="74a18-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="74a18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74a18-104">SYNTAX</span></span>

### <span data-ttu-id="74a18-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74a18-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74a18-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a18-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74a18-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a18-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74a18-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74a18-108">DESCRIPTION</span></span>
<span data-ttu-id="74a18-109">Для параметра аудита рабочей области Azure Synapse Analytics задаются параметры аудита для **cmdlet Get-AzSynapseSqlAuditSetting.**</span><span class="sxs-lookup"><span data-stu-id="74a18-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="74a18-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74a18-110">EXAMPLES</span></span>

### <span data-ttu-id="74a18-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74a18-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="74a18-112">Параметры аудита рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="74a18-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="74a18-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="74a18-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="74a18-114">Параметры аудита рабочей области с именем ContosoWorkspace проходят через канал.</span><span class="sxs-lookup"><span data-stu-id="74a18-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="74a18-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74a18-115">PARAMETERS</span></span>

### <span data-ttu-id="74a18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a18-116">-DefaultProfile</span></span>
<span data-ttu-id="74a18-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74a18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a18-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74a18-118">-InputObject</span></span>
<span data-ttu-id="74a18-119">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="74a18-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="74a18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a18-120">-ResourceGroupName</span></span>
<span data-ttu-id="74a18-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74a18-121">Resource group name.</span></span>

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

### <span data-ttu-id="74a18-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74a18-122">-ResourceId</span></span>
<span data-ttu-id="74a18-123">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="74a18-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="74a18-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74a18-124">-WorkspaceName</span></span>
<span data-ttu-id="74a18-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="74a18-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="74a18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a18-126">CommonParameters</span></span>
<span data-ttu-id="74a18-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a18-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74a18-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a18-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74a18-129">INPUTS</span></span>

### <span data-ttu-id="74a18-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74a18-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="74a18-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74a18-131">OUTPUTS</span></span>

### <span data-ttu-id="74a18-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="74a18-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="74a18-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74a18-133">NOTES</span></span>

## <span data-ttu-id="74a18-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74a18-134">RELATED LINKS</span></span>
