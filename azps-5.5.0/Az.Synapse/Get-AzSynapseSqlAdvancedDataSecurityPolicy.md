---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232465"
---
# <span data-ttu-id="98462-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="98462-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="98462-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98462-102">SYNOPSIS</span></span>
<span data-ttu-id="98462-103">Получает политику advanced Data Security рабочей области.</span><span class="sxs-lookup"><span data-stu-id="98462-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="98462-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98462-104">SYNTAX</span></span>

### <span data-ttu-id="98462-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98462-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98462-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98462-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98462-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98462-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98462-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98462-108">DESCRIPTION</span></span>
<span data-ttu-id="98462-109">Для получения политики Advanced Data Security рабочей области будет извлечена cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy.**</span><span class="sxs-lookup"><span data-stu-id="98462-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="98462-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98462-110">EXAMPLES</span></span>

### <span data-ttu-id="98462-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98462-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="98462-112">Эта команда получает advanced Data Security в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="98462-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="98462-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98462-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="98462-114">Эта команда получает advanced Data Security в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="98462-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="98462-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98462-115">PARAMETERS</span></span>

### <span data-ttu-id="98462-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98462-116">-DefaultProfile</span></span>
<span data-ttu-id="98462-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98462-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98462-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98462-118">-InputObject</span></span>
<span data-ttu-id="98462-119">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="98462-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="98462-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98462-120">-ResourceGroupName</span></span>
<span data-ttu-id="98462-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98462-121">Resource group name.</span></span>

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

### <span data-ttu-id="98462-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98462-122">-ResourceId</span></span>
<span data-ttu-id="98462-123">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="98462-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="98462-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98462-124">-WorkspaceName</span></span>
<span data-ttu-id="98462-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="98462-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="98462-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98462-126">CommonParameters</span></span>
<span data-ttu-id="98462-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98462-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98462-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98462-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98462-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98462-129">INPUTS</span></span>

### <span data-ttu-id="98462-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="98462-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="98462-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98462-131">OUTPUTS</span></span>

### <span data-ttu-id="98462-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="98462-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="98462-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98462-133">NOTES</span></span>

## <span data-ttu-id="98462-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98462-134">RELATED LINKS</span></span>
