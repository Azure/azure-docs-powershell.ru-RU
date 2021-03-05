---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 58b2aa2f62de5cc47a9319c9cf36b0d2c8d55975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961139"
---
# <span data-ttu-id="cb9ce-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="cb9ce-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="cb9ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ce-103">Отключение advanced Data Security в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="cb9ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb9ce-104">SYNTAX</span></span>

### <span data-ttu-id="cb9ce-105">DisableByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb9ce-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb9ce-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb9ce-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb9ce-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb9ce-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb9ce-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb9ce-108">DESCRIPTION</span></span>
<span data-ttu-id="cb9ce-109">Из-за cmdlet Advanced Data Security в рабочей области отключена служба Advanced Data **Security (Отключение-AzSynapseSqlAdvancedDataSecurity).**</span><span class="sxs-lookup"><span data-stu-id="cb9ce-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="cb9ce-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb9ce-110">EXAMPLES</span></span>

### <span data-ttu-id="cb9ce-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb9ce-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cb9ce-112">Эта команда отключает advanced Data Security в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cb9ce-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb9ce-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="cb9ce-114">Эта команда отключает advanced Data Security в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cb9ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-115">PARAMETERS</span></span>

### <span data-ttu-id="cb9ce-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb9ce-116">-AsJob</span></span>
<span data-ttu-id="cb9ce-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cb9ce-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb9ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9ce-118">-DefaultProfile</span></span>
<span data-ttu-id="cb9ce-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb9ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb9ce-120">-InputObject</span></span>
<span data-ttu-id="cb9ce-121">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb9ce-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb9ce-124">-ResourceId</span></span>
<span data-ttu-id="cb9ce-125">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ce-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb9ce-126">-WorkspaceName</span></span>
<span data-ttu-id="cb9ce-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ce-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb9ce-128">-Confirm</span></span>
<span data-ttu-id="cb9ce-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9ce-130">-WhatIf</span></span>
<span data-ttu-id="cb9ce-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9ce-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ce-133">CommonParameters</span></span>
<span data-ttu-id="cb9ce-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ce-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb9ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ce-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-136">INPUTS</span></span>

### <span data-ttu-id="cb9ce-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cb9ce-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cb9ce-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-138">OUTPUTS</span></span>

### <span data-ttu-id="cb9ce-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="cb9ce-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="cb9ce-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb9ce-140">NOTES</span></span>

## <span data-ttu-id="cb9ce-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb9ce-141">RELATED LINKS</span></span>
