---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241733"
---
# <span data-ttu-id="78633-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="78633-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="78633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78633-102">SYNOPSIS</span></span>
<span data-ttu-id="78633-103">Получает дополнительные параметры защиты от угроз для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="78633-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="78633-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78633-104">SYNTAX</span></span>

### <span data-ttu-id="78633-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78633-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78633-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78633-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78633-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78633-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78633-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78633-108">DESCRIPTION</span></span>
<span data-ttu-id="78633-109">Чтобы получить дополнительные параметры защиты от угроз в рабочей области Azure Synapse Analytics, для **get-AzSynapseSqlAdvancedThreatProtectionSetting** можно получить дополнительные параметры защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="78633-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="78633-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78633-110">EXAMPLES</span></span>

### <span data-ttu-id="78633-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78633-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="78633-112">Эта команда получает расширенные параметры защиты от угроз для рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="78633-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="78633-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78633-113">PARAMETERS</span></span>

### <span data-ttu-id="78633-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78633-114">-DefaultProfile</span></span>
<span data-ttu-id="78633-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78633-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78633-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78633-116">-InputObject</span></span>
<span data-ttu-id="78633-117">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="78633-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="78633-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78633-118">-ResourceGroupName</span></span>
<span data-ttu-id="78633-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78633-119">Resource group name.</span></span>

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

### <span data-ttu-id="78633-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78633-120">-ResourceId</span></span>
<span data-ttu-id="78633-121">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="78633-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="78633-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78633-122">-WorkspaceName</span></span>
<span data-ttu-id="78633-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="78633-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="78633-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78633-124">CommonParameters</span></span>
<span data-ttu-id="78633-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78633-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78633-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78633-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78633-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78633-127">INPUTS</span></span>

### <span data-ttu-id="78633-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78633-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="78633-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78633-129">OUTPUTS</span></span>

### <span data-ttu-id="78633-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="78633-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="78633-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78633-131">NOTES</span></span>

## <span data-ttu-id="78633-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78633-132">RELATED LINKS</span></span>
