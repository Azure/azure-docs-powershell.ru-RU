---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733875"
---
# <span data-ttu-id="4152e-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4152e-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="4152e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4152e-102">SYNOPSIS</span></span>
<span data-ttu-id="4152e-103">Удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="4152e-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4152e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4152e-104">SYNTAX</span></span>

### <span data-ttu-id="4152e-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4152e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4152e-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4152e-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4152e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4152e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4152e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4152e-108">DESCRIPTION</span></span>
<span data-ttu-id="4152e-109">Командлет Remove-AzureRmContainerRegistryReplication удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="4152e-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="4152e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4152e-110">EXAMPLES</span></span>

### <span data-ttu-id="4152e-111">Пример 1: удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="4152e-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="4152e-112">Удаляет репликацию реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="4152e-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="4152e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4152e-113">PARAMETERS</span></span>

### <span data-ttu-id="4152e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4152e-114">-DefaultProfile</span></span>
<span data-ttu-id="4152e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4152e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4152e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4152e-116">-Name</span></span>
<span data-ttu-id="4152e-117">Имя репликации в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="4152e-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="4152e-118">По умолчанию — имя расположения.</span><span class="sxs-lookup"><span data-stu-id="4152e-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4152e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4152e-119">-PassThru</span></span>
<span data-ttu-id="4152e-120">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="4152e-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="4152e-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4152e-121">-RegistryName</span></span>
<span data-ttu-id="4152e-122">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="4152e-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4152e-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="4152e-123">-Replicatoin</span></span>
<span data-ttu-id="4152e-124">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="4152e-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4152e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4152e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4152e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4152e-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4152e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4152e-127">-ResourceId</span></span>
<span data-ttu-id="4152e-128">Идентификатор ресурса репликации реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="4152e-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="4152e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4152e-129">-Confirm</span></span>
<span data-ttu-id="4152e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4152e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4152e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4152e-131">-WhatIf</span></span>
<span data-ttu-id="4152e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4152e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4152e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4152e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4152e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4152e-134">CommonParameters</span></span>
<span data-ttu-id="4152e-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4152e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4152e-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4152e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4152e-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4152e-137">INPUTS</span></span>

### <span data-ttu-id="4152e-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4152e-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="4152e-139">Параметры: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4152e-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="4152e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4152e-140">System.String</span></span>

## <span data-ttu-id="4152e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4152e-141">OUTPUTS</span></span>

### <span data-ttu-id="4152e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4152e-142">System.Boolean</span></span>

## <span data-ttu-id="4152e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4152e-143">NOTES</span></span>

## <span data-ttu-id="4152e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4152e-144">RELATED LINKS</span></span>

[<span data-ttu-id="4152e-145">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4152e-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="4152e-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4152e-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

