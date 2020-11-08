---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247963"
---
# <span data-ttu-id="61581-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61581-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="61581-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61581-102">SYNOPSIS</span></span>
<span data-ttu-id="61581-103">Возвращает определение роли аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="61581-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="61581-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61581-104">SYNTAX</span></span>

### <span data-ttu-id="61581-105">GetByWorkspaceNameAndIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61581-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61581-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61581-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61581-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61581-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61581-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61581-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61581-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61581-109">DESCRIPTION</span></span>
<span data-ttu-id="61581-110">Командлет **Get-AzSynapseRoleDefinition** получает определение роли аналитики Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="61581-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="61581-111">Если не указать имя роли или идентификатор роли, этот командлет получает все определения ролей.</span><span class="sxs-lookup"><span data-stu-id="61581-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="61581-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61581-112">EXAMPLES</span></span>

### <span data-ttu-id="61581-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61581-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="61581-114">Эта команда получает все определения ролей в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="61581-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="61581-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="61581-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="61581-116">Эта команда получает определение роли в разделе Рабочая область ContosoWorkspace с именем ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="61581-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="61581-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="61581-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="61581-118">Эта команда получает все определения ролей в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="61581-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="61581-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61581-119">PARAMETERS</span></span>

### <span data-ttu-id="61581-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61581-120">-DefaultProfile</span></span>
<span data-ttu-id="61581-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61581-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61581-122">-ID</span><span class="sxs-lookup"><span data-stu-id="61581-122">-Id</span></span>
<span data-ttu-id="61581-123">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="61581-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="61581-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61581-124">-Name</span></span>
<span data-ttu-id="61581-125">Имя роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="61581-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="61581-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61581-126">-WorkspaceName</span></span>
<span data-ttu-id="61581-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="61581-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="61581-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61581-128">-WorkspaceObject</span></span>
<span data-ttu-id="61581-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="61581-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="61581-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61581-130">CommonParameters</span></span>
<span data-ttu-id="61581-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61581-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61581-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61581-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61581-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61581-133">INPUTS</span></span>

### <span data-ttu-id="61581-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="61581-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="61581-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61581-135">OUTPUTS</span></span>

### <span data-ttu-id="61581-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="61581-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="61581-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="61581-137">NOTES</span></span>

## <span data-ttu-id="61581-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61581-138">RELATED LINKS</span></span>
