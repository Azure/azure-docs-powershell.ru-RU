---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246597"
---
# <span data-ttu-id="54029-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54029-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="54029-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54029-102">SYNOPSIS</span></span>
<span data-ttu-id="54029-103">Обновляет рабочую область Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="54029-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="54029-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54029-104">SYNTAX</span></span>

### <span data-ttu-id="54029-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54029-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54029-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54029-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54029-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54029-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54029-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54029-108">DESCRIPTION</span></span>
<span data-ttu-id="54029-109">Командлет **Update-AzSynapseWorkspace** обновляет рабочую область Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="54029-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="54029-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54029-110">EXAMPLES</span></span>

### <span data-ttu-id="54029-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54029-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="54029-112">Эта команда обновляет теги для рабочей области specififed Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="54029-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="54029-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="54029-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="54029-114">Эта команда обновляет теги для рабочей области specififed Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="54029-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="54029-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="54029-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="54029-116">Эта команда обновляет теги для рабочей области specififed Azure Synapse Analytics с помощью конвейера с ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="54029-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="54029-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54029-117">PARAMETERS</span></span>

### <span data-ttu-id="54029-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54029-118">-AsJob</span></span>
<span data-ttu-id="54029-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="54029-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54029-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54029-120">-DefaultProfile</span></span>
<span data-ttu-id="54029-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54029-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54029-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54029-122">-InputObject</span></span>
<span data-ttu-id="54029-123">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="54029-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="54029-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54029-124">-Name</span></span>
<span data-ttu-id="54029-125">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="54029-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="54029-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54029-126">-ResourceGroupName</span></span>
<span data-ttu-id="54029-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54029-127">Resource group name.</span></span>

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

### <span data-ttu-id="54029-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54029-128">-ResourceId</span></span>
<span data-ttu-id="54029-129">Идентификатор ресурса Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="54029-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="54029-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="54029-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="54029-131">Новый пароль администратора SQL для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="54029-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="54029-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="54029-132">-Tag</span></span>
<span data-ttu-id="54029-133">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="54029-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="54029-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54029-134">-Confirm</span></span>
<span data-ttu-id="54029-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54029-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54029-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54029-136">-WhatIf</span></span>
<span data-ttu-id="54029-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54029-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54029-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54029-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54029-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54029-139">CommonParameters</span></span>
<span data-ttu-id="54029-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54029-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54029-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54029-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54029-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54029-142">INPUTS</span></span>

### <span data-ttu-id="54029-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54029-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="54029-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54029-144">OUTPUTS</span></span>

### <span data-ttu-id="54029-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54029-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="54029-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="54029-146">NOTES</span></span>

## <span data-ttu-id="54029-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54029-147">RELATED LINKS</span></span>
