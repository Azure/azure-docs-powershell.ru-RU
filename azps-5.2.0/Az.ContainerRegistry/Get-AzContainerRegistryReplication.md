---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405263"
---
# <span data-ttu-id="e5c6c-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="e5c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c6c-103">Возвращает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="e5c6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5c6c-104">SYNTAX</span></span>

### <span data-ttu-id="e5c6c-105">ListReplicationByNameResourceGroupParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c6c-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c6c-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c6c-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c6c-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c6c-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5c6c-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c6c-110">DESCRIPTION</span></span>
<span data-ttu-id="e5c6c-111">Этот Get-AzContainerRegistryReplication возвращает заданную репликацию реестра контейнера или все репликации реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="e5c6c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c6c-112">EXAMPLES</span></span>

### <span data-ttu-id="e5c6c-113">Пример 1. Возвращает заданную репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e5c6c-114">Возвращает заданную репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="e5c6c-115">Пример 2. Получает все репликации реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e5c6c-116">Возвращает все репликации реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="e5c6c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-117">PARAMETERS</span></span>

### <span data-ttu-id="e5c6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c6c-118">-DefaultProfile</span></span>
<span data-ttu-id="e5c6c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c6c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e5c6c-120">-Name</span></span>
<span data-ttu-id="e5c6c-121">Имя репликации контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="e5c6c-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="e5c6c-122">-Registry</span></span>
<span data-ttu-id="e5c6c-123">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="e5c6c-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e5c6c-124">-RegistryName</span></span>
<span data-ttu-id="e5c6c-125">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="e5c6c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c6c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5c6c-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e5c6c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c6c-128">-ResourceId</span></span>
<span data-ttu-id="e5c6c-129">ИД ресурса репликации контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="e5c6c-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="e5c6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c6c-130">CommonParameters</span></span>
<span data-ttu-id="e5c6c-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c6c-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5c6c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c6c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-133">INPUTS</span></span>

### <span data-ttu-id="e5c6c-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e5c6c-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="e5c6c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e5c6c-135">System.String</span></span>

## <span data-ttu-id="e5c6c-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c6c-136">OUTPUTS</span></span>

### <span data-ttu-id="e5c6c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="e5c6c-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5c6c-138">NOTES</span></span>

## <span data-ttu-id="e5c6c-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c6c-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5c6c-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="e5c6c-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5c6c-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)