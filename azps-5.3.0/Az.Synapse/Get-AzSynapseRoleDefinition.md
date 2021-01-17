---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424495"
---
# <span data-ttu-id="56e7c-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="56e7c-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="56e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="56e7c-103">Получает определение роли synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="56e7c-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="56e7c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56e7c-104">SYNTAX</span></span>

### <span data-ttu-id="56e7c-105">GetByWorkspaceNameAndIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56e7c-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56e7c-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e7c-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56e7c-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e7c-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56e7c-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e7c-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e7c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56e7c-109">DESCRIPTION</span></span>
<span data-ttu-id="56e7c-110">Для получения определения роли Synapse Analytics в Azure возвращается **cmdlet Get-AzSynapseRoleDefinition.**</span><span class="sxs-lookup"><span data-stu-id="56e7c-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="56e7c-111">Если не указать имя роли или ее код, этот cmdlet получит все определения ролей.</span><span class="sxs-lookup"><span data-stu-id="56e7c-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="56e7c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56e7c-112">EXAMPLES</span></span>

### <span data-ttu-id="56e7c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56e7c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="56e7c-114">Эта команда получает все определения ролей в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56e7c-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="56e7c-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="56e7c-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="56e7c-116">Эта команда получает определение роли в рабочей области ContosoWorkspace с именем ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="56e7c-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="56e7c-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="56e7c-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="56e7c-118">Эта команда получает все определения ролей в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="56e7c-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="56e7c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56e7c-119">PARAMETERS</span></span>

### <span data-ttu-id="56e7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e7c-120">-DefaultProfile</span></span>
<span data-ttu-id="56e7c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56e7c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e7c-122">-Id</span><span class="sxs-lookup"><span data-stu-id="56e7c-122">-Id</span></span>
<span data-ttu-id="56e7c-123">ИД роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="56e7c-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e7c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="56e7c-124">-Name</span></span>
<span data-ttu-id="56e7c-125">Имя роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="56e7c-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e7c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56e7c-126">-WorkspaceName</span></span>
<span data-ttu-id="56e7c-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="56e7c-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e7c-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="56e7c-128">-WorkspaceObject</span></span>
<span data-ttu-id="56e7c-129">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="56e7c-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56e7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e7c-130">CommonParameters</span></span>
<span data-ttu-id="56e7c-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e7c-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56e7c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e7c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56e7c-133">INPUTS</span></span>

### <span data-ttu-id="56e7c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="56e7c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="56e7c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56e7c-135">OUTPUTS</span></span>

### <span data-ttu-id="56e7c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="56e7c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="56e7c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56e7c-137">NOTES</span></span>

## <span data-ttu-id="56e7c-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56e7c-138">RELATED LINKS</span></span>
