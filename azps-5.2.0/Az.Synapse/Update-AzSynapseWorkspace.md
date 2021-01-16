---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412652"
---
# <span data-ttu-id="772b6-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="772b6-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="772b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="772b6-102">SYNOPSIS</span></span>
<span data-ttu-id="772b6-103">Обновляет рабочее пространство Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="772b6-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="772b6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="772b6-104">SYNTAX</span></span>

### <span data-ttu-id="772b6-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="772b6-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772b6-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="772b6-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772b6-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="772b6-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772b6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="772b6-108">DESCRIPTION</span></span>
<span data-ttu-id="772b6-109">Командлет **Update-AzSynapseWorkspace** обновляет рабочее пространство Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="772b6-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="772b6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="772b6-110">EXAMPLES</span></span>

### <span data-ttu-id="772b6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="772b6-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="772b6-112">Эта команда обновляет теги для указанной рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="772b6-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="772b6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="772b6-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="772b6-114">Эта команда обновляет теги указанной рабочей области Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="772b6-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="772b6-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="772b6-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="772b6-116">Эта команда обновляет теги указанного рабочего пространства Azure Synapse Analytics через канал с ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="772b6-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="772b6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="772b6-117">PARAMETERS</span></span>

### <span data-ttu-id="772b6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="772b6-118">-AsJob</span></span>
<span data-ttu-id="772b6-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="772b6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="772b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772b6-120">-DefaultProfile</span></span>
<span data-ttu-id="772b6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="772b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="772b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="772b6-122">-InputObject</span></span>
<span data-ttu-id="772b6-123">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="772b6-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="772b6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="772b6-124">-Name</span></span>
<span data-ttu-id="772b6-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="772b6-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="772b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="772b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="772b6-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="772b6-127">Resource group name.</span></span>

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

### <span data-ttu-id="772b6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="772b6-128">-ResourceId</span></span>
<span data-ttu-id="772b6-129">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="772b6-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="772b6-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="772b6-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="772b6-131">Новый пароль SQL администратора для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="772b6-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="772b6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="772b6-132">-Tag</span></span>
<span data-ttu-id="772b6-133">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="772b6-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="772b6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="772b6-134">-Confirm</span></span>
<span data-ttu-id="772b6-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="772b6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772b6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772b6-136">-WhatIf</span></span>
<span data-ttu-id="772b6-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="772b6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772b6-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="772b6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772b6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772b6-139">CommonParameters</span></span>
<span data-ttu-id="772b6-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772b6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772b6-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="772b6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772b6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="772b6-142">INPUTS</span></span>

### <span data-ttu-id="772b6-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="772b6-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="772b6-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="772b6-144">OUTPUTS</span></span>

### <span data-ttu-id="772b6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="772b6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="772b6-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="772b6-146">NOTES</span></span>

## <span data-ttu-id="772b6-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="772b6-147">RELATED LINKS</span></span>
