---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 0a4844a3ed1bdc48f741215ae91ee075425cd68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721603"
---
# <span data-ttu-id="81bb3-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="81bb3-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="81bb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="81bb3-103">Возвращает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="81bb3-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="81bb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81bb3-104">SYNTAX</span></span>

### <span data-ttu-id="81bb3-105">ListReplicationByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81bb3-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81bb3-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="81bb3-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81bb3-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81bb3-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81bb3-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81bb3-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81bb3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81bb3-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81bb3-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bb3-110">DESCRIPTION</span></span>
<span data-ttu-id="81bb3-111">Командлет Get-AzContainerRegistryReplication получает указанную репликацию реестра контейнера или все репликация в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="81bb3-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="81bb3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81bb3-112">EXAMPLES</span></span>

### <span data-ttu-id="81bb3-113">Пример 1: получение указанной репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="81bb3-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="81bb3-114">Возвращает заданную репликацию реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="81bb3-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="81bb3-115">Пример 2: получение всех репликаций реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="81bb3-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="81bb3-116">Получение всех репликаций реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="81bb3-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="81bb3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81bb3-117">PARAMETERS</span></span>

### <span data-ttu-id="81bb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bb3-118">-DefaultProfile</span></span>
<span data-ttu-id="81bb3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81bb3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81bb3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81bb3-120">-Name</span></span>
<span data-ttu-id="81bb3-121">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="81bb3-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="81bb3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="81bb3-122">-Registry</span></span>
<span data-ttu-id="81bb3-123">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="81bb3-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="81bb3-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="81bb3-124">-RegistryName</span></span>
<span data-ttu-id="81bb3-125">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="81bb3-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="81bb3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bb3-126">-ResourceGroupName</span></span>
<span data-ttu-id="81bb3-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81bb3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="81bb3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81bb3-128">-ResourceId</span></span>
<span data-ttu-id="81bb3-129">Идентификатор ресурса репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="81bb3-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="81bb3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bb3-130">CommonParameters</span></span>
<span data-ttu-id="81bb3-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81bb3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bb3-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81bb3-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bb3-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81bb3-133">INPUTS</span></span>

### <span data-ttu-id="81bb3-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="81bb3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="81bb3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="81bb3-135">System.String</span></span>

## <span data-ttu-id="81bb3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bb3-136">OUTPUTS</span></span>

### <span data-ttu-id="81bb3-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="81bb3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="81bb3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="81bb3-138">NOTES</span></span>

## <span data-ttu-id="81bb3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81bb3-139">RELATED LINKS</span></span>

[<span data-ttu-id="81bb3-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="81bb3-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="81bb3-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="81bb3-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)