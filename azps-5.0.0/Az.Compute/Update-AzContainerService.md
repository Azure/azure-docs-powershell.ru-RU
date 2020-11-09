---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311951"
---
# <span data-ttu-id="d7625-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-101">Update-AzContainerService</span></span>

## <span data-ttu-id="d7625-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7625-102">SYNOPSIS</span></span>
<span data-ttu-id="d7625-103">Обновляет состояние службы контейнера.</span><span class="sxs-lookup"><span data-stu-id="d7625-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="d7625-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7625-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7625-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7625-105">DESCRIPTION</span></span>
<span data-ttu-id="d7625-106">Командлет **Update-AzContainerService** обновляет состояние службы контейнеров в соответствии с локальным экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="d7625-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="d7625-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7625-107">EXAMPLES</span></span>

### <span data-ttu-id="d7625-108">Пример 1: обновление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="d7625-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="d7625-109">Эта команда получает службу контейнеров с именем CSResourceGroup17 с помощью командлета Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="d7625-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="d7625-110">Команда передает этот объект в командлет Remove-AzContainerServiceAgentPoolProfile с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d7625-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7625-111">**Remove-AzContainerServiceAgentPoolProfile** удаляет профиль с именем AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="d7625-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="d7625-112">Команда передает результат в командлет Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="d7625-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="d7625-113">**Add-AzContainerServiceAgentPoolProfile** добавляет профиль с именем AgentPool01 и имеет указанные свойства.</span><span class="sxs-lookup"><span data-stu-id="d7625-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="d7625-114">Команда передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="d7625-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="d7625-115">Текущий командлет обновляет службу контейнеров, чтобы отразить изменения, внесенные в этой команде.</span><span class="sxs-lookup"><span data-stu-id="d7625-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="d7625-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7625-116">PARAMETERS</span></span>

### <span data-ttu-id="d7625-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7625-117">-AsJob</span></span>
<span data-ttu-id="d7625-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d7625-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7625-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-119">-ContainerService</span></span>
<span data-ttu-id="d7625-120">Указывает локальный объект **ContainerService** , который содержит изменения.</span><span class="sxs-lookup"><span data-stu-id="d7625-120">Specifies a local **ContainerService** object that contains changes.</span></span>

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

### <span data-ttu-id="d7625-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7625-121">-DefaultProfile</span></span>
<span data-ttu-id="d7625-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7625-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7625-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7625-123">-Name</span></span>
<span data-ttu-id="d7625-124">Указывает имя службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d7625-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d7625-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7625-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7625-126">Указывает группу ресурсов службы контейнера, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d7625-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d7625-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7625-127">-Confirm</span></span>
<span data-ttu-id="d7625-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7625-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7625-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7625-129">-WhatIf</span></span>
<span data-ttu-id="d7625-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7625-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7625-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7625-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7625-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7625-132">CommonParameters</span></span>
<span data-ttu-id="d7625-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7625-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7625-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7625-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7625-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7625-135">INPUTS</span></span>

### <span data-ttu-id="d7625-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d7625-136">System.String</span></span>

### <span data-ttu-id="d7625-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d7625-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7625-138">OUTPUTS</span></span>

### <span data-ttu-id="d7625-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d7625-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7625-140">NOTES</span></span>

## <span data-ttu-id="d7625-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7625-141">RELATED LINKS</span></span>

[<span data-ttu-id="d7625-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d7625-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d7625-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="d7625-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="d7625-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d7625-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="d7625-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d7625-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


