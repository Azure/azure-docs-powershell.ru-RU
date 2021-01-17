---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424239"
---
# <span data-ttu-id="0fc1b-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0fc1b-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="0fc1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc1b-103">Создает рабочее пространство Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0fc1b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0fc1b-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc1b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc1b-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc1b-106">Командлет **New-AzSynapseWorkspace** создает рабочее пространство Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0fc1b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0fc1b-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc1b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0fc1b-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="0fc1b-109">Эта команда создает рабочее пространство Synapse Analytics ContosoWorkspace, использующее хранилище данных ContosoAdlGenStorage в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="0fc1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fc1b-110">PARAMETERS</span></span>

### <span data-ttu-id="0fc1b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fc1b-111">-AsJob</span></span>
<span data-ttu-id="0fc1b-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0fc1b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fc1b-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0fc1b-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="0fc1b-114">Стандартное имя учетной записи хранения ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="0fc1b-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="0fc1b-116">Файловая система ADLS gen2 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc1b-117">-DefaultProfile</span></span>
<span data-ttu-id="0fc1b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc1b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="0fc1b-119">-Location</span></span>
<span data-ttu-id="0fc1b-120">Регион Azure, в котором должен быть создан ресурс.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0fc1b-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="0fc1b-122">Имя виртуальной сети под управлением Synapse, выделенной для рабочей области Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0fc1b-123">-Name</span></span>
<span data-ttu-id="0fc1b-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="0fc1b-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="0fc1b-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="0fc1b-128">SQL учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fc1b-129">-Tag</span></span>
<span data-ttu-id="0fc1b-130">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc1b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fc1b-131">-Confirm</span></span>
<span data-ttu-id="0fc1b-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc1b-133">-WhatIf</span></span>
<span data-ttu-id="0fc1b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc1b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc1b-136">CommonParameters</span></span>
<span data-ttu-id="0fc1b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc1b-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fc1b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc1b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fc1b-139">INPUTS</span></span>

### <span data-ttu-id="0fc1b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0fc1b-140">System.String</span></span>

### <span data-ttu-id="0fc1b-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0fc1b-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0fc1b-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="0fc1b-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="0fc1b-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0fc1b-143">OUTPUTS</span></span>

### <span data-ttu-id="0fc1b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0fc1b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0fc1b-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0fc1b-145">NOTES</span></span>

## <span data-ttu-id="0fc1b-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fc1b-146">RELATED LINKS</span></span>
