---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224700"
---
# <span data-ttu-id="bff76-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="bff76-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="bff76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff76-102">SYNOPSIS</span></span>
<span data-ttu-id="bff76-103">Возвращает состояние TDE для SQL пула.</span><span class="sxs-lookup"><span data-stu-id="bff76-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="bff76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bff76-104">SYNTAX</span></span>

### <span data-ttu-id="bff76-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bff76-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bff76-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff76-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bff76-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff76-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bff76-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff76-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bff76-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff76-109">DESCRIPTION</span></span>
<span data-ttu-id="bff76-110">Для пула аналитики Synapse Analytics в Azure SQL состояние шифрования данных (TDE) для **get-AzSynapseSqlPoolTransparentDataEncryption.**</span><span class="sxs-lookup"><span data-stu-id="bff76-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bff76-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bff76-111">EXAMPLES</span></span>

### <span data-ttu-id="bff76-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bff76-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="bff76-113">Эта команда получает состояние TDE для SQL ContosoSqlPool в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bff76-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="bff76-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bff76-114">PARAMETERS</span></span>

### <span data-ttu-id="bff76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff76-115">-DefaultProfile</span></span>
<span data-ttu-id="bff76-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bff76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff76-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bff76-117">-InputObject</span></span>
<span data-ttu-id="bff76-118">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="bff76-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bff76-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bff76-119">-Name</span></span>
<span data-ttu-id="bff76-120">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="bff76-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="bff76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff76-121">-ResourceGroupName</span></span>
<span data-ttu-id="bff76-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bff76-122">Resource group name.</span></span>

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

### <span data-ttu-id="bff76-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bff76-123">-ResourceId</span></span>
<span data-ttu-id="bff76-124">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="bff76-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="bff76-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bff76-125">-WorkspaceName</span></span>
<span data-ttu-id="bff76-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="bff76-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bff76-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bff76-127">-WorkspaceObject</span></span>
<span data-ttu-id="bff76-128">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="bff76-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bff76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff76-129">CommonParameters</span></span>
<span data-ttu-id="bff76-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff76-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bff76-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff76-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bff76-132">INPUTS</span></span>

### <span data-ttu-id="bff76-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bff76-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bff76-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bff76-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bff76-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bff76-135">OUTPUTS</span></span>

### <span data-ttu-id="bff76-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="bff76-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="bff76-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bff76-137">NOTES</span></span>

## <span data-ttu-id="bff76-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bff76-138">RELATED LINKS</span></span>
