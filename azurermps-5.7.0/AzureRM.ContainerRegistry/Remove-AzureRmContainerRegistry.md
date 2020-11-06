---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: df0c938db8f44ebffedc9760e4a3d33ee175ae01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565536"
---
# <span data-ttu-id="e6761-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e6761-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="e6761-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6761-102">SYNOPSIS</span></span>
<span data-ttu-id="e6761-103">Удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6761-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6761-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6761-104">SYNTAX</span></span>

### <span data-ttu-id="e6761-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6761-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6761-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6761-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6761-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6761-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6761-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6761-108">DESCRIPTION</span></span>
<span data-ttu-id="e6761-109">Командлет Remove-AzureRmContainerRegistry удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6761-109">The Remove-AzureRmContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="e6761-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6761-110">EXAMPLES</span></span>

### <span data-ttu-id="e6761-111">Пример 1: Удаление указанного реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="e6761-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="e6761-112">Эта команда удаляет заданный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="e6761-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="e6761-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6761-113">PARAMETERS</span></span>

### <span data-ttu-id="e6761-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6761-114">-Name</span></span>
<span data-ttu-id="e6761-115">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="e6761-115">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="e6761-116">-Registry</span></span>
<span data-ttu-id="e6761-117">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6761-117">Container Registry Object.</span></span>

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

### <span data-ttu-id="e6761-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6761-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6761-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6761-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="e6761-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6761-120">-Confirm</span></span>
<span data-ttu-id="e6761-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6761-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6761-122">-WhatIf</span></span>
<span data-ttu-id="e6761-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6761-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6761-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6761-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6761-125">-DefaultProfile</span></span>
<span data-ttu-id="e6761-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e6761-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6761-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6761-127">-ResourceId</span></span>
<span data-ttu-id="e6761-128">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="e6761-128">The container registry resource id</span></span>

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

### <span data-ttu-id="e6761-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6761-129">-PassThru</span></span>
<span data-ttu-id="e6761-130">Указывает на то, что этот командлет возвращает значение true, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="e6761-130">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="e6761-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6761-131">CommonParameters</span></span>
<span data-ttu-id="e6761-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6761-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6761-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6761-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6761-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6761-134">INPUTS</span></span>

### <span data-ttu-id="e6761-135">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e6761-135">PSContainerRegistry</span></span>
<span data-ttu-id="e6761-136">Параметр "Registry" принимает значение типа "PSContainerRegistry" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6761-136">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="e6761-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6761-137">OUTPUTS</span></span>

### <span data-ttu-id="e6761-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="e6761-138">None</span></span>

## <span data-ttu-id="e6761-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6761-139">NOTES</span></span>

## <span data-ttu-id="e6761-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6761-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6761-141">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e6761-141">New-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="e6761-142">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e6761-142">Get-AzureRmContainerRegistry</span></span>]()

[<span data-ttu-id="e6761-143">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e6761-143">Update-AzureRmContainerRegistry</span></span>]()

