---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235196"
---
# <span data-ttu-id="6d58a-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6d58a-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="6d58a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d58a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d58a-103">Возвращает определение роли аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="6d58a-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="6d58a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d58a-104">SYNTAX</span></span>

### <span data-ttu-id="6d58a-105">GetByWorkspaceNameAndIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d58a-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d58a-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d58a-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d58a-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d58a-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d58a-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d58a-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d58a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d58a-109">DESCRIPTION</span></span>
<span data-ttu-id="6d58a-110">Командлет **Get-AzSynapseRoleDefinition** получает определение роли аналитики Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="6d58a-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="6d58a-111">Если не указать имя роли или идентификатор роли, этот командлет получает все определения ролей.</span><span class="sxs-lookup"><span data-stu-id="6d58a-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="6d58a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d58a-112">EXAMPLES</span></span>

### <span data-ttu-id="6d58a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d58a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6d58a-114">Эта команда получает все определения ролей в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6d58a-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="6d58a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6d58a-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="6d58a-116">Эта команда получает определение роли в разделе Рабочая область ContosoWorkspace с именем ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="6d58a-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="6d58a-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6d58a-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="6d58a-118">Эта команда получает все определения ролей в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="6d58a-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="6d58a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d58a-119">PARAMETERS</span></span>

### <span data-ttu-id="6d58a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d58a-120">-DefaultProfile</span></span>
<span data-ttu-id="6d58a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d58a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d58a-122">-ID</span><span class="sxs-lookup"><span data-stu-id="6d58a-122">-Id</span></span>
<span data-ttu-id="6d58a-123">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="6d58a-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="6d58a-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d58a-124">-Name</span></span>
<span data-ttu-id="6d58a-125">Имя роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="6d58a-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="6d58a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6d58a-126">-WorkspaceName</span></span>
<span data-ttu-id="6d58a-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6d58a-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6d58a-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6d58a-128">-WorkspaceObject</span></span>
<span data-ttu-id="6d58a-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6d58a-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6d58a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d58a-130">CommonParameters</span></span>
<span data-ttu-id="6d58a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d58a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d58a-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d58a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d58a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d58a-133">INPUTS</span></span>

### <span data-ttu-id="6d58a-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d58a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6d58a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d58a-135">OUTPUTS</span></span>

### <span data-ttu-id="6d58a-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="6d58a-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="6d58a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d58a-137">NOTES</span></span>

## <span data-ttu-id="6d58a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d58a-138">RELATED LINKS</span></span>
