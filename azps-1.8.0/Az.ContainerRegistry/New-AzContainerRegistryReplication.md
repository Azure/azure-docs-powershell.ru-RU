---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: 091f1efd8dc9373c99e4b853de63393860ff73cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731181"
---
# <span data-ttu-id="b03b3-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b03b3-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="b03b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b03b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b03b3-103">Создает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="b03b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b03b3-104">SYNTAX</span></span>

### <span data-ttu-id="b03b3-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b03b3-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b03b3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03b3-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b03b3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03b3-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b03b3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b03b3-108">DESCRIPTION</span></span>
<span data-ttu-id="b03b3-109">Командлет New-AzContainerRegistryReplication создает новую репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="b03b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b03b3-110">EXAMPLES</span></span>

### <span data-ttu-id="b03b3-111">Пример 1: создание новой репликации реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="b03b3-112">Создание новой репликации реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="b03b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b03b3-113">PARAMETERS</span></span>

### <span data-ttu-id="b03b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03b3-114">-DefaultProfile</span></span>
<span data-ttu-id="b03b3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b03b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b03b3-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b03b3-116">-Location</span></span>
<span data-ttu-id="b03b3-117">Расположение в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-117">Container Registry Location.</span></span>
<span data-ttu-id="b03b3-118">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b03b3-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b03b3-119">-Name</span></span>
<span data-ttu-id="b03b3-120">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="b03b3-121">По умолчанию — имя расположения.</span><span class="sxs-lookup"><span data-stu-id="b03b3-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="b03b3-122">-Registry</span></span>
<span data-ttu-id="b03b3-123">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b03b3-124">-RegistryName</span></span>
<span data-ttu-id="b03b3-125">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="b03b3-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="b03b3-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b03b3-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b03b3-128">-ResourceId</span></span>
<span data-ttu-id="b03b3-129">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="b03b3-129">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="b03b3-130">-Tag</span></span>
<span data-ttu-id="b03b3-131">Теги реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="b03b3-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b03b3-132">-Confirm</span></span>
<span data-ttu-id="b03b3-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b03b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03b3-134">-WhatIf</span></span>
<span data-ttu-id="b03b3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b03b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03b3-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b03b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03b3-137">CommonParameters</span></span>
<span data-ttu-id="b03b3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b03b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03b3-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03b3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03b3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b03b3-140">INPUTS</span></span>

### <span data-ttu-id="b03b3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b03b3-141">System.String</span></span>

## <span data-ttu-id="b03b3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b03b3-142">OUTPUTS</span></span>

### <span data-ttu-id="b03b3-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b03b3-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="b03b3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b03b3-144">NOTES</span></span>

## <span data-ttu-id="b03b3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b03b3-145">RELATED LINKS</span></span>

[<span data-ttu-id="b03b3-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b03b3-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="b03b3-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b03b3-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)