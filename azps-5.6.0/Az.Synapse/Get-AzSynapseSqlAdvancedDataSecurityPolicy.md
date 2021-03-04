---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 47800968fec9a12255bae01499618f9928416648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015715"
---
# <span data-ttu-id="f7254-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="f7254-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="f7254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7254-102">SYNOPSIS</span></span>
<span data-ttu-id="f7254-103">Получает политику advanced Data Security для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7254-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="f7254-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7254-104">SYNTAX</span></span>

### <span data-ttu-id="f7254-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7254-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7254-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7254-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7254-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7254-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7254-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7254-108">DESCRIPTION</span></span>
<span data-ttu-id="f7254-109">Cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** извлекает политику Advanced Data Security рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7254-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="f7254-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7254-110">EXAMPLES</span></span>

### <span data-ttu-id="f7254-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7254-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f7254-112">Эта команда получает advanced Data Security в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f7254-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f7254-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f7254-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="f7254-114">Эта команда получает advanced Data Security в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="f7254-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f7254-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7254-115">PARAMETERS</span></span>

### <span data-ttu-id="f7254-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7254-116">-DefaultProfile</span></span>
<span data-ttu-id="f7254-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7254-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7254-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7254-118">-InputObject</span></span>
<span data-ttu-id="f7254-119">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f7254-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7254-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7254-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7254-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7254-121">Resource group name.</span></span>

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

### <span data-ttu-id="f7254-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7254-122">-ResourceId</span></span>
<span data-ttu-id="f7254-123">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7254-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7254-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7254-124">-WorkspaceName</span></span>
<span data-ttu-id="f7254-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7254-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7254-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7254-126">CommonParameters</span></span>
<span data-ttu-id="f7254-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7254-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7254-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7254-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7254-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7254-129">INPUTS</span></span>

### <span data-ttu-id="f7254-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7254-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f7254-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7254-131">OUTPUTS</span></span>

### <span data-ttu-id="f7254-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="f7254-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="f7254-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7254-133">NOTES</span></span>

## <span data-ttu-id="f7254-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7254-134">RELATED LINKS</span></span>
