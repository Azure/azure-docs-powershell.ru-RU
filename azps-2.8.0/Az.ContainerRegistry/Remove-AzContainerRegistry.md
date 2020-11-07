---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: c389f62f6f9b76f0ebdab30ddf600d333263a87c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721591"
---
# <span data-ttu-id="1eb02-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1eb02-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="1eb02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1eb02-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb02-103">Удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="1eb02-103">Removes a container registry.</span></span>

## <span data-ttu-id="1eb02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1eb02-104">SYNTAX</span></span>

### <span data-ttu-id="1eb02-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1eb02-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb02-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb02-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb02-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb02-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb02-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb02-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb02-109">Командлет Remove-AzContainerRegistry удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="1eb02-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="1eb02-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1eb02-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb02-111">Пример 1: Удаление указанного реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="1eb02-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="1eb02-112">Эта команда удаляет заданный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="1eb02-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="1eb02-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb02-113">PARAMETERS</span></span>

### <span data-ttu-id="1eb02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb02-114">-DefaultProfile</span></span>
<span data-ttu-id="1eb02-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1eb02-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eb02-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1eb02-116">-Name</span></span>
<span data-ttu-id="1eb02-117">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="1eb02-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb02-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1eb02-118">-PassThru</span></span>
<span data-ttu-id="1eb02-119">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="1eb02-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="1eb02-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="1eb02-120">-Registry</span></span>
<span data-ttu-id="1eb02-121">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="1eb02-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="1eb02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb02-122">-ResourceGroupName</span></span>
<span data-ttu-id="1eb02-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1eb02-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="1eb02-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb02-124">-ResourceId</span></span>
<span data-ttu-id="1eb02-125">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="1eb02-125">The container registry resource id</span></span>

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

### <span data-ttu-id="1eb02-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb02-126">-Confirm</span></span>
<span data-ttu-id="1eb02-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1eb02-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb02-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb02-128">-WhatIf</span></span>
<span data-ttu-id="1eb02-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1eb02-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb02-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1eb02-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb02-131">CommonParameters</span></span>
<span data-ttu-id="1eb02-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1eb02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb02-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb02-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb02-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1eb02-134">INPUTS</span></span>

### <span data-ttu-id="1eb02-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb02-135">System.String</span></span>

## <span data-ttu-id="1eb02-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb02-136">OUTPUTS</span></span>

### <span data-ttu-id="1eb02-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1eb02-137">System.Boolean</span></span>

## <span data-ttu-id="1eb02-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1eb02-138">NOTES</span></span>

## <span data-ttu-id="1eb02-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb02-139">RELATED LINKS</span></span>

[<span data-ttu-id="1eb02-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1eb02-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="1eb02-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1eb02-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="1eb02-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1eb02-142">Update-AzContainerRegistry</span></span>]()

