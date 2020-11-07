---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912076"
---
# <span data-ttu-id="2962d-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2962d-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="2962d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2962d-102">SYNOPSIS</span></span>
<span data-ttu-id="2962d-103">Возвращает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="2962d-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="2962d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2962d-104">SYNTAX</span></span>

### <span data-ttu-id="2962d-105">ListReplicationByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2962d-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2962d-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2962d-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2962d-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2962d-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2962d-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2962d-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2962d-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2962d-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2962d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2962d-110">DESCRIPTION</span></span>
<span data-ttu-id="2962d-111">Командлет Get-AzContainerRegistryReplication получает указанную репликацию реестра контейнера или все репликация в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="2962d-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="2962d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2962d-112">EXAMPLES</span></span>

### <span data-ttu-id="2962d-113">Пример 1: получение указанной репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2962d-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="2962d-114">Возвращает заданную репликацию реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2962d-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="2962d-115">Пример 2: получение всех репликаций реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2962d-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="2962d-116">Получение всех репликаций реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2962d-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="2962d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2962d-117">PARAMETERS</span></span>

### <span data-ttu-id="2962d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2962d-118">-DefaultProfile</span></span>
<span data-ttu-id="2962d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2962d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2962d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2962d-120">-Name</span></span>
<span data-ttu-id="2962d-121">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="2962d-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="2962d-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="2962d-122">-Registry</span></span>
<span data-ttu-id="2962d-123">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="2962d-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="2962d-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2962d-124">-RegistryName</span></span>
<span data-ttu-id="2962d-125">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="2962d-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="2962d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2962d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2962d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2962d-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2962d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2962d-128">-ResourceId</span></span>
<span data-ttu-id="2962d-129">Идентификатор ресурса репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="2962d-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="2962d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2962d-130">CommonParameters</span></span>
<span data-ttu-id="2962d-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2962d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2962d-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2962d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2962d-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2962d-133">INPUTS</span></span>

### <span data-ttu-id="2962d-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2962d-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="2962d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2962d-135">System.String</span></span>

## <span data-ttu-id="2962d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2962d-136">OUTPUTS</span></span>

### <span data-ttu-id="2962d-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2962d-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="2962d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2962d-138">NOTES</span></span>

## <span data-ttu-id="2962d-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2962d-139">RELATED LINKS</span></span>

[<span data-ttu-id="2962d-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2962d-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="2962d-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2962d-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)