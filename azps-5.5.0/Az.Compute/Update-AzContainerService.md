---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244021"
---
# <span data-ttu-id="d1cf0-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-101">Update-AzContainerService</span></span>

## <span data-ttu-id="d1cf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cf0-103">Обновляет состояние службы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="d1cf0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1cf0-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1cf0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="d1cf0-106">Командлет **Update-AzContainerService** обновляет состояние службы контейнеров в соответствие с локальным экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="d1cf0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1cf0-107">EXAMPLES</span></span>

### <span data-ttu-id="d1cf0-108">Пример 1. Обновление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="d1cf0-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="d1cf0-109">Эта команда получает службу контейнера CSResourceGroup17 с помощью Get-AzContainerService командлета.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="d1cf0-110">Эта команда передает этот объект в командлет Remove-AzContainerServiceAgentPoolProfile с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d1cf0-111">**Remove-AzContainerServiceAgentPoolProfile** удаляет профиль AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="d1cf0-112">Команда передает результат командлету Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="d1cf0-113">**Add-AzContainerServiceAgentPoolProfile** добавляет профиль с именем AgentPool01 и указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="d1cf0-114">Команда передает результат текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="d1cf0-115">Текущий командлет обновляет службу контейнеров с учетом изменений, внесенных в этой команде.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="d1cf0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1cf0-116">PARAMETERS</span></span>

### <span data-ttu-id="d1cf0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1cf0-117">-AsJob</span></span>
<span data-ttu-id="d1cf0-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d1cf0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1cf0-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-119">-ContainerService</span></span>
<span data-ttu-id="d1cf0-120">Определяет локальный объект **ContainerService,** содержащий изменения.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cf0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cf0-121">-DefaultProfile</span></span>
<span data-ttu-id="d1cf0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1cf0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d1cf0-123">-Name</span></span>
<span data-ttu-id="d1cf0-124">Указывает имя службы контейнеров, которую обновляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cf0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1cf0-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1cf0-126">Определяет группу ресурсов службы контейнеров, которую обновляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cf0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1cf0-127">-Confirm</span></span>
<span data-ttu-id="d1cf0-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1cf0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1cf0-129">-WhatIf</span></span>
<span data-ttu-id="d1cf0-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1cf0-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1cf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cf0-132">CommonParameters</span></span>
<span data-ttu-id="d1cf0-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1cf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cf0-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1cf0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cf0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1cf0-135">INPUTS</span></span>

### <span data-ttu-id="d1cf0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d1cf0-136">System.String</span></span>

### <span data-ttu-id="d1cf0-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d1cf0-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1cf0-138">OUTPUTS</span></span>

### <span data-ttu-id="d1cf0-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d1cf0-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1cf0-140">NOTES</span></span>

## <span data-ttu-id="d1cf0-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1cf0-141">RELATED LINKS</span></span>

[<span data-ttu-id="d1cf0-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d1cf0-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d1cf0-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="d1cf0-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="d1cf0-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d1cf0-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="d1cf0-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d1cf0-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


