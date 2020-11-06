---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistry.md
ms.openlocfilehash: 5a5ea87044c18e82f4c17294356a35adb254eee4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559940"
---
# <span data-ttu-id="dbb97-101">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dbb97-101">Remove-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="dbb97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbb97-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb97-103">Удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbb97-103">Removes a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbb97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbb97-104">SYNTAX</span></span>

### <span data-ttu-id="dbb97-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dbb97-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbb97-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbb97-106">RegistryObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistry -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbb97-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbb97-107">DESCRIPTION</span></span>
<span data-ttu-id="dbb97-108">Командлет **Remove-AzureRmContainerRegistry** удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbb97-108">The **Remove-AzureRmContainerRegistry** cmdlet removes a container registry.</span></span>

## <span data-ttu-id="dbb97-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbb97-109">EXAMPLES</span></span>

### <span data-ttu-id="dbb97-110">Пример 1: Удаление указанного реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="dbb97-110">Example 1: Remove a specified container registry</span></span>
```
PS C:\>Remove-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="dbb97-111">Эта команда удаляет заданный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="dbb97-111">This command removes the specified container registry.</span></span>

## <span data-ttu-id="dbb97-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbb97-112">PARAMETERS</span></span>

### <span data-ttu-id="dbb97-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dbb97-113">-Name</span></span>
<span data-ttu-id="dbb97-114">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="dbb97-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="dbb97-115">-Registry</span><span class="sxs-lookup"><span data-stu-id="dbb97-115">-Registry</span></span>
<span data-ttu-id="dbb97-116">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbb97-116">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb97-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbb97-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbb97-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="dbb97-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbb97-119">-Confirm</span></span>
<span data-ttu-id="dbb97-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dbb97-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbb97-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbb97-121">-WhatIf</span></span>
<span data-ttu-id="dbb97-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dbb97-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbb97-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbb97-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbb97-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb97-124">-DefaultProfile</span></span>
<span data-ttu-id="dbb97-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb97-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbb97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb97-126">CommonParameters</span></span>
<span data-ttu-id="dbb97-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbb97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb97-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb97-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb97-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbb97-129">INPUTS</span></span>

### <span data-ttu-id="dbb97-130">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dbb97-130">PSContainerRegistry</span></span>
<span data-ttu-id="dbb97-131">Параметр "Registry" принимает значение типа "PSContainerRegistry" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dbb97-131">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="dbb97-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbb97-132">OUTPUTS</span></span>

### <span data-ttu-id="dbb97-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="dbb97-133">None</span></span>

## <span data-ttu-id="dbb97-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbb97-134">NOTES</span></span>

## <span data-ttu-id="dbb97-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbb97-135">RELATED LINKS</span></span>

[<span data-ttu-id="dbb97-136">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dbb97-136">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="dbb97-137">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dbb97-137">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="dbb97-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dbb97-138">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

