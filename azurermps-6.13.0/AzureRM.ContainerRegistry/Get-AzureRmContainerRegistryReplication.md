---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731977"
---
# <span data-ttu-id="cbf6a-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbf6a-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="cbf6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf6a-103">Возвращает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbf6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbf6a-104">SYNTAX</span></span>

### <span data-ttu-id="cbf6a-105">ListReplicationByNameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbf6a-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf6a-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbf6a-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf6a-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbf6a-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf6a-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbf6a-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf6a-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbf6a-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbf6a-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbf6a-110">DESCRIPTION</span></span>
<span data-ttu-id="cbf6a-111">Командлет Get-AzureRmContainerRegistryReplication получает указанную репликацию реестра контейнера или все репликация в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="cbf6a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbf6a-112">EXAMPLES</span></span>

### <span data-ttu-id="cbf6a-113">Пример 1: получение указанной репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="cbf6a-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cbf6a-114">Возвращает заданную репликацию реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="cbf6a-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="cbf6a-115">Пример 2: получение всех репликаций реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="cbf6a-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cbf6a-116">Получение всех репликаций реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="cbf6a-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="cbf6a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbf6a-117">PARAMETERS</span></span>

### <span data-ttu-id="cbf6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf6a-118">-DefaultProfile</span></span>
<span data-ttu-id="cbf6a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf6a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbf6a-120">-Name</span></span>
<span data-ttu-id="cbf6a-121">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="cbf6a-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="cbf6a-122">-Registry</span></span>
<span data-ttu-id="cbf6a-123">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="cbf6a-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cbf6a-124">-RegistryName</span></span>
<span data-ttu-id="cbf6a-125">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="cbf6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="cbf6a-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="cbf6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf6a-128">-ResourceId</span></span>
<span data-ttu-id="cbf6a-129">Идентификатор ресурса репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="cbf6a-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="cbf6a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf6a-130">CommonParameters</span></span>
<span data-ttu-id="cbf6a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbf6a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf6a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf6a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf6a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbf6a-133">INPUTS</span></span>

### <span data-ttu-id="cbf6a-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cbf6a-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="cbf6a-135">Параметры: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cbf6a-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="cbf6a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf6a-136">System.String</span></span>

## <span data-ttu-id="cbf6a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbf6a-137">OUTPUTS</span></span>

### <span data-ttu-id="cbf6a-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbf6a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="cbf6a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbf6a-139">NOTES</span></span>

## <span data-ttu-id="cbf6a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbf6a-140">RELATED LINKS</span></span>

[<span data-ttu-id="cbf6a-141">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbf6a-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="cbf6a-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbf6a-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
