---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249291"
---
# <span data-ttu-id="757ad-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="757ad-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="757ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="757ad-102">SYNOPSIS</span></span>
<span data-ttu-id="757ad-103">Создание рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="757ad-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="757ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="757ad-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="757ad-105">DESCRIPTION</span></span>
<span data-ttu-id="757ad-106">Командлет **New-AzSynapseWorkspace** создает рабочую область Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="757ad-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="757ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="757ad-107">EXAMPLES</span></span>

### <span data-ttu-id="757ad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="757ad-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="757ad-109">Эта команда создает рабочую область аналитики Synapse с именем ContosoWorkspace, которая использует хранилище данных ContosoAdlGenStorage, в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="757ad-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="757ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="757ad-110">PARAMETERS</span></span>

### <span data-ttu-id="757ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="757ad-111">-AsJob</span></span>
<span data-ttu-id="757ad-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="757ad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="757ad-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="757ad-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="757ad-114">Имя учетной записи хранения ADLS Gen2 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="757ad-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="757ad-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="757ad-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="757ad-116">Файловая система по умолчанию ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="757ad-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="757ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757ad-117">-DefaultProfile</span></span>
<span data-ttu-id="757ad-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="757ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="757ad-119">-Location</span><span class="sxs-lookup"><span data-stu-id="757ad-119">-Location</span></span>
<span data-ttu-id="757ad-120">Регион Azure, в котором нужно создать ресурс.</span><span class="sxs-lookup"><span data-stu-id="757ad-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="757ad-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="757ad-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="757ad-122">Имя Synapse-управляемой виртуальной сети, выделенной для рабочей области Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="757ad-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="757ad-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="757ad-123">-Name</span></span>
<span data-ttu-id="757ad-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="757ad-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="757ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="757ad-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="757ad-126">Resource group name.</span></span>

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

### <span data-ttu-id="757ad-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="757ad-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="757ad-128">Учетные данные администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="757ad-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="757ad-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="757ad-129">-Tag</span></span>
<span data-ttu-id="757ad-130">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="757ad-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="757ad-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="757ad-131">-Confirm</span></span>
<span data-ttu-id="757ad-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="757ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757ad-133">-WhatIf</span></span>
<span data-ttu-id="757ad-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="757ad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757ad-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="757ad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757ad-136">CommonParameters</span></span>
<span data-ttu-id="757ad-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="757ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757ad-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="757ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757ad-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="757ad-139">INPUTS</span></span>

### <span data-ttu-id="757ad-140">System. String</span><span class="sxs-lookup"><span data-stu-id="757ad-140">System.String</span></span>

### <span data-ttu-id="757ad-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="757ad-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="757ad-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="757ad-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="757ad-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="757ad-143">OUTPUTS</span></span>

### <span data-ttu-id="757ad-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="757ad-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="757ad-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="757ad-145">NOTES</span></span>

## <span data-ttu-id="757ad-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="757ad-146">RELATED LINKS</span></span>