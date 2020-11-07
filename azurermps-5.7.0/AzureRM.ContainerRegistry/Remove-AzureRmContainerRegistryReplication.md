---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732740"
---
# <span data-ttu-id="694a4-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="694a4-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="694a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="694a4-102">SYNOPSIS</span></span>
<span data-ttu-id="694a4-103">Удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="694a4-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="694a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="694a4-104">SYNTAX</span></span>

### <span data-ttu-id="694a4-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="694a4-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="694a4-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="694a4-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="694a4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="694a4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="694a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="694a4-108">DESCRIPTION</span></span>
<span data-ttu-id="694a4-109">Командлет Remove-AzureRmContainerRegistryReplication удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="694a4-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="694a4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="694a4-110">EXAMPLES</span></span>

### <span data-ttu-id="694a4-111">Пример 1: удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="694a4-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="694a4-112">Удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="694a4-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="694a4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="694a4-113">PARAMETERS</span></span>

### <span data-ttu-id="694a4-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="694a4-114">-Confirm</span></span>
<span data-ttu-id="694a4-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="694a4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="694a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694a4-116">-DefaultProfile</span></span>
<span data-ttu-id="694a4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="694a4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694a4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="694a4-118">-Name</span></span>
<span data-ttu-id="694a4-119">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="694a4-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="694a4-120">По умолчанию — имя расположения.</span><span class="sxs-lookup"><span data-stu-id="694a4-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694a4-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="694a4-121">-RegistryName</span></span>
<span data-ttu-id="694a4-122">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="694a4-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694a4-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="694a4-123">-Replicatoin</span></span>
<span data-ttu-id="694a4-124">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="694a4-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="694a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="694a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="694a4-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="694a4-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694a4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="694a4-127">-ResourceId</span></span>
<span data-ttu-id="694a4-128">Идентификатор ресурса репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="694a4-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="694a4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694a4-129">-WhatIf</span></span>
<span data-ttu-id="694a4-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="694a4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="694a4-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="694a4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="694a4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="694a4-132">-PassThru</span></span>
<span data-ttu-id="694a4-133">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="694a4-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694a4-134">CommonParameters</span></span>
<span data-ttu-id="694a4-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="694a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694a4-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694a4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694a4-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="694a4-137">INPUTS</span></span>

### <span data-ttu-id="694a4-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="694a4-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="694a4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="694a4-139">System.String</span></span>

## <span data-ttu-id="694a4-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="694a4-140">OUTPUTS</span></span>

### <span data-ttu-id="694a4-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="694a4-141">System.Object</span></span>

## <span data-ttu-id="694a4-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="694a4-142">NOTES</span></span>

## <span data-ttu-id="694a4-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="694a4-143">RELATED LINKS</span></span>

[<span data-ttu-id="694a4-144">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="694a4-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="694a4-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="694a4-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

