---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732744"
---
# <span data-ttu-id="7e2ce-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e2ce-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="7e2ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2ce-103">Создает репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e2ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e2ce-104">SYNTAX</span></span>

### <span data-ttu-id="7e2ce-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e2ce-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2ce-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e2ce-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2ce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e2ce-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e2ce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e2ce-108">DESCRIPTION</span></span>
<span data-ttu-id="7e2ce-109">Командлет New-AzureRmContainerRegistryReplication создает новую репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="7e2ce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e2ce-110">EXAMPLES</span></span>

### <span data-ttu-id="7e2ce-111">Пример 1: создание новой репликации реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="7e2ce-112">Создание новой репликации реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="7e2ce-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e2ce-113">PARAMETERS</span></span>

### <span data-ttu-id="7e2ce-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e2ce-114">-Confirm</span></span>
<span data-ttu-id="7e2ce-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2ce-116">-DefaultProfile</span></span>
<span data-ttu-id="7e2ce-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-118">-Location</span><span class="sxs-lookup"><span data-stu-id="7e2ce-118">-Location</span></span>
<span data-ttu-id="7e2ce-119">Расположение в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-119">Container Registry Location.</span></span>
<span data-ttu-id="7e2ce-120">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e2ce-121">-Name</span></span>
<span data-ttu-id="7e2ce-122">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="7e2ce-123">По умолчанию — имя расположения.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-124">-Registry</span><span class="sxs-lookup"><span data-stu-id="7e2ce-124">-Registry</span></span>
<span data-ttu-id="7e2ce-125">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-126">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7e2ce-126">-RegistryName</span></span>
<span data-ttu-id="7e2ce-127">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e2ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e2ce-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e2ce-130">-ResourceId</span></span>
<span data-ttu-id="7e2ce-131">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="7e2ce-131">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="7e2ce-132">-Tag</span></span>
<span data-ttu-id="7e2ce-133">Теги реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-133">Container Registry Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e2ce-134">-WhatIf</span></span>
<span data-ttu-id="7e2ce-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e2ce-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2ce-137">CommonParameters</span></span>
<span data-ttu-id="7e2ce-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e2ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2ce-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2ce-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2ce-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e2ce-140">INPUTS</span></span>

### <span data-ttu-id="7e2ce-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7e2ce-141">System.String</span></span>

## <span data-ttu-id="7e2ce-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e2ce-142">OUTPUTS</span></span>

### <span data-ttu-id="7e2ce-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e2ce-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="7e2ce-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e2ce-144">NOTES</span></span>

## <span data-ttu-id="7e2ce-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e2ce-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e2ce-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e2ce-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="7e2ce-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e2ce-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
