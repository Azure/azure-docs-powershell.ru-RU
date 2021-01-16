---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507934"
---
# <span data-ttu-id="d454c-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d454c-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="d454c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d454c-102">SYNOPSIS</span></span>
<span data-ttu-id="d454c-103">Изменяет свойство TDE для SQL пула.</span><span class="sxs-lookup"><span data-stu-id="d454c-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="d454c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d454c-104">SYNTAX</span></span>

### <span data-ttu-id="d454c-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d454c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d454c-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d454c-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d454c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d454c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d454c-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d454c-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d454c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d454c-109">DESCRIPTION</span></span>
<span data-ttu-id="d454c-110">В этом режиме свойство **Set-AzSynapseSqlPoolTransparentDataEncryption** изменяет свойство прозрачного шифрования данных (TDE) пула azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="d454c-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d454c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d454c-111">EXAMPLES</span></span>

### <span data-ttu-id="d454c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d454c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="d454c-113">Эта команда включает TDE для SQL ContosoSqlPool в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d454c-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d454c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d454c-114">PARAMETERS</span></span>

### <span data-ttu-id="d454c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d454c-115">-AsJob</span></span>
<span data-ttu-id="d454c-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d454c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d454c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d454c-117">-DefaultProfile</span></span>
<span data-ttu-id="d454c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d454c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d454c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d454c-119">-InputObject</span></span>
<span data-ttu-id="d454c-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d454c-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d454c-121">-Name</span></span>
<span data-ttu-id="d454c-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d454c-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d454c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d454c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d454c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d454c-125">-ResourceId</span></span>
<span data-ttu-id="d454c-126">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d454c-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-127">-State</span><span class="sxs-lookup"><span data-stu-id="d454c-127">-State</span></span>
<span data-ttu-id="d454c-128">Состояние прозрачного шифрования данных пула Sql Synapse Analytics Azure.</span><span class="sxs-lookup"><span data-stu-id="d454c-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d454c-129">-WorkspaceName</span></span>
<span data-ttu-id="d454c-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d454c-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d454c-131">-WorkspaceObject</span></span>
<span data-ttu-id="d454c-132">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d454c-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d454c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d454c-133">-Confirm</span></span>
<span data-ttu-id="d454c-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d454c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d454c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d454c-135">-WhatIf</span></span>
<span data-ttu-id="d454c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d454c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d454c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d454c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d454c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d454c-138">CommonParameters</span></span>
<span data-ttu-id="d454c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d454c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d454c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d454c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d454c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d454c-141">INPUTS</span></span>

### <span data-ttu-id="d454c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d454c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d454c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d454c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d454c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d454c-144">OUTPUTS</span></span>

### <span data-ttu-id="d454c-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d454c-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="d454c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d454c-146">NOTES</span></span>

## <span data-ttu-id="d454c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d454c-147">RELATED LINKS</span></span>
