---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231489"
---
# <span data-ttu-id="14a51-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="14a51-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="14a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a51-102">SYNOPSIS</span></span>
<span data-ttu-id="14a51-103">Отключение advanced Data Security в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="14a51-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="14a51-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14a51-104">SYNTAX</span></span>

### <span data-ttu-id="14a51-105">DisableByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14a51-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a51-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a51-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a51-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a51-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a51-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14a51-108">DESCRIPTION</span></span>
<span data-ttu-id="14a51-109">Для рабочей области отключение advanced Data Security (Безопасность данных) для отключения advanced Data Security **(Отключение-AzSynapseSqlAdvancedDataSecurity).**</span><span class="sxs-lookup"><span data-stu-id="14a51-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="14a51-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14a51-110">EXAMPLES</span></span>

### <span data-ttu-id="14a51-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14a51-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="14a51-112">Эта команда отключает advanced Data Security в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="14a51-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="14a51-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14a51-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="14a51-114">Эта команда отключает advanced Data Security в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="14a51-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="14a51-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14a51-115">PARAMETERS</span></span>

### <span data-ttu-id="14a51-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14a51-116">-AsJob</span></span>
<span data-ttu-id="14a51-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14a51-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14a51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a51-118">-DefaultProfile</span></span>
<span data-ttu-id="14a51-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14a51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a51-120">-InputObject</span></span>
<span data-ttu-id="14a51-121">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="14a51-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="14a51-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a51-122">-ResourceGroupName</span></span>
<span data-ttu-id="14a51-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14a51-123">Resource group name.</span></span>

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

### <span data-ttu-id="14a51-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a51-124">-ResourceId</span></span>
<span data-ttu-id="14a51-125">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="14a51-125">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="14a51-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="14a51-126">-WorkspaceName</span></span>
<span data-ttu-id="14a51-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="14a51-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14a51-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14a51-128">-Confirm</span></span>
<span data-ttu-id="14a51-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14a51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a51-130">-WhatIf</span></span>
<span data-ttu-id="14a51-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14a51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a51-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14a51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a51-133">CommonParameters</span></span>
<span data-ttu-id="14a51-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a51-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14a51-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a51-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14a51-136">INPUTS</span></span>

### <span data-ttu-id="14a51-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14a51-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="14a51-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14a51-138">OUTPUTS</span></span>

### <span data-ttu-id="14a51-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="14a51-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="14a51-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14a51-140">NOTES</span></span>

## <span data-ttu-id="14a51-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14a51-141">RELATED LINKS</span></span>
