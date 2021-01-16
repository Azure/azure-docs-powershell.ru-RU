---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508946"
---
# <span data-ttu-id="eabce-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eabce-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="eabce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eabce-102">SYNOPSIS</span></span>
<span data-ttu-id="eabce-103">Возвращает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="eabce-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="eabce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eabce-104">SYNTAX</span></span>

### <span data-ttu-id="eabce-105">ListReplicationByNameResourceGroupParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="eabce-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabce-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabce-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabce-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabce-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabce-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabce-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eabce-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabce-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eabce-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eabce-110">DESCRIPTION</span></span>
<span data-ttu-id="eabce-111">Этот Get-AzContainerRegistryReplication возвращает заданную репликацию реестра контейнера или все репликации реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="eabce-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="eabce-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eabce-112">EXAMPLES</span></span>

### <span data-ttu-id="eabce-113">Пример 1. Возвращает заданную репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="eabce-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="eabce-114">Возвращает заданную репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="eabce-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="eabce-115">Пример 2. Получает все репликации реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="eabce-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="eabce-116">Возвращает все репликации реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="eabce-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="eabce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eabce-117">PARAMETERS</span></span>

### <span data-ttu-id="eabce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabce-118">-DefaultProfile</span></span>
<span data-ttu-id="eabce-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eabce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eabce-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eabce-120">-Name</span></span>
<span data-ttu-id="eabce-121">Имя репликации контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="eabce-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabce-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="eabce-122">-Registry</span></span>
<span data-ttu-id="eabce-123">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="eabce-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eabce-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="eabce-124">-RegistryName</span></span>
<span data-ttu-id="eabce-125">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="eabce-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabce-126">-ResourceGroupName</span></span>
<span data-ttu-id="eabce-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eabce-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eabce-128">-ResourceId</span></span>
<span data-ttu-id="eabce-129">ИД ресурса репликации контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="eabce-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="eabce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabce-130">CommonParameters</span></span>
<span data-ttu-id="eabce-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabce-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eabce-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabce-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eabce-133">INPUTS</span></span>

### <span data-ttu-id="eabce-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eabce-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="eabce-135">System.String</span><span class="sxs-lookup"><span data-stu-id="eabce-135">System.String</span></span>

## <span data-ttu-id="eabce-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eabce-136">OUTPUTS</span></span>

### <span data-ttu-id="eabce-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eabce-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="eabce-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eabce-138">NOTES</span></span>

## <span data-ttu-id="eabce-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eabce-139">RELATED LINKS</span></span>

[<span data-ttu-id="eabce-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eabce-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="eabce-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eabce-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)