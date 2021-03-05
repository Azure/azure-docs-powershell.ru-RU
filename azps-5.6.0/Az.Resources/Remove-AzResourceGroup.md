---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: d85a6170505563daf1033df60474fd94011d928f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974376"
---
# <span data-ttu-id="9c5b2-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c5b2-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="9c5b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5b2-103">Удаляет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-103">Removes a resource group.</span></span>

## <span data-ttu-id="9c5b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c5b2-104">SYNTAX</span></span>

### <span data-ttu-id="9c5b2-105">RemoveByResourceGroupName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c5b2-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c5b2-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9c5b2-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c5b2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c5b2-107">DESCRIPTION</span></span>
<span data-ttu-id="9c5b2-108">При **этом из текущей** подписки удаляется группа ресурсов Azure и ее ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="9c5b2-109">Чтобы удалить ресурс, но выйти из группы ресурсов, воспользуйтесь Remove-AzResource этим Remove-AzResource.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="9c5b2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c5b2-110">EXAMPLES</span></span>

### <span data-ttu-id="9c5b2-111">Пример 1. Удаление группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c5b2-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="9c5b2-112">Эта команда удаляет группу ресурсов ContosoRG01 из подписки.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="9c5b2-113">Он запросит подтверждение и не возвратит результат.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="9c5b2-114">Пример 2. Удаление группы ресурсов без подтверждения</span><span class="sxs-lookup"><span data-stu-id="9c5b2-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="9c5b2-115">Эта команда использует Get-AzResourceGroup для получения группы ресурсов ContosoRG01, а затем передает ее в **Remove-AzResourceGroup с** помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="9c5b2-116">Параметр *Force* подавляет запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="9c5b2-117">Пример 3. Удаление всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c5b2-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="9c5b2-118">Эта команда использует командлет **Get-AzResourceGroup** для получения всех групп ресурсов, а затем передает их в **Remove-AzResourceGroup с** помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="9c5b2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c5b2-119">PARAMETERS</span></span>

### <span data-ttu-id="9c5b2-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c5b2-120">-ApiVersion</span></span>
<span data-ttu-id="9c5b2-121">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9c5b2-122">Можно указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c5b2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c5b2-123">-AsJob</span></span>
<span data-ttu-id="9c5b2-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9c5b2-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c5b2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5b2-125">-DefaultProfile</span></span>
<span data-ttu-id="9c5b2-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9c5b2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c5b2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9c5b2-127">-Force</span></span>
<span data-ttu-id="9c5b2-128">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c5b2-129">-Id</span><span class="sxs-lookup"><span data-stu-id="9c5b2-129">-Id</span></span>
<span data-ttu-id="9c5b2-130">Определяет ИД удаляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="9c5b2-131">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5b2-132">-Name</span><span class="sxs-lookup"><span data-stu-id="9c5b2-132">-Name</span></span>
<span data-ttu-id="9c5b2-133">Определяет имена групп ресурсов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="9c5b2-134">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5b2-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c5b2-135">-Pre</span></span>
<span data-ttu-id="9c5b2-136">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9c5b2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c5b2-137">-Confirm</span></span>
<span data-ttu-id="9c5b2-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5b2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5b2-139">-WhatIf</span></span>
<span data-ttu-id="9c5b2-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c5b2-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5b2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5b2-142">CommonParameters</span></span>
<span data-ttu-id="9c5b2-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5b2-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c5b2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5b2-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c5b2-145">INPUTS</span></span>

### <span data-ttu-id="9c5b2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9c5b2-146">System.String</span></span>

## <span data-ttu-id="9c5b2-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c5b2-147">OUTPUTS</span></span>

### <span data-ttu-id="9c5b2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c5b2-148">System.Boolean</span></span>

## <span data-ttu-id="9c5b2-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c5b2-149">NOTES</span></span>

## <span data-ttu-id="9c5b2-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c5b2-150">RELATED LINKS</span></span>

[<span data-ttu-id="9c5b2-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c5b2-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="9c5b2-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c5b2-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="9c5b2-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c5b2-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


