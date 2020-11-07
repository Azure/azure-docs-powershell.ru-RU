---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 7878932b0e7a2aad6e171c39e546ad86b2ea0a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729335"
---
# <span data-ttu-id="a92c0-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a92c0-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="a92c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a92c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a92c0-103">Удаляет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a92c0-103">Removes a resource group.</span></span>

## <span data-ttu-id="a92c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a92c0-104">SYNTAX</span></span>

### <span data-ttu-id="a92c0-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a92c0-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a92c0-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a92c0-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a92c0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92c0-107">DESCRIPTION</span></span>
<span data-ttu-id="a92c0-108">Командлет **Remove-AzResourceGroup** удаляет группу ресурсов Azure и ее ресурсы из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="a92c0-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="a92c0-109">Чтобы удалить ресурс, но оставить группу ресурсов, используйте командлет Remove-AzResource.</span><span class="sxs-lookup"><span data-stu-id="a92c0-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="a92c0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a92c0-110">EXAMPLES</span></span>

### <span data-ttu-id="a92c0-111">Пример 1: Удаление группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a92c0-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="a92c0-112">Эта команда удаляет группу ресурсов ContosoRG01 из подписки.</span><span class="sxs-lookup"><span data-stu-id="a92c0-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="a92c0-113">Командлет запрашивает подтверждение и не возвращает результаты.</span><span class="sxs-lookup"><span data-stu-id="a92c0-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="a92c0-114">Пример 2: Удаление группы ресурсов без подтверждения</span><span class="sxs-lookup"><span data-stu-id="a92c0-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="a92c0-115">Эта команда использует командлет Get-AzResourceGroup для получения группы ресурсов ContosoRG01, а затем передает его в **Remove-AzResourceGroup** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a92c0-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="a92c0-116">Параметр *verbose* Common возвращает сведения о состоянии операции, а параметр *Force* подавляет вывод запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a92c0-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="a92c0-117">Пример 3: удаление всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="a92c0-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="a92c0-118">Эта команда использует командлет **Get-AzResourceGroup** для получения всех групп ресурсов, а затем передает их в **Remove-AzResourceGroup** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a92c0-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="a92c0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a92c0-119">PARAMETERS</span></span>

### <span data-ttu-id="a92c0-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a92c0-120">-ApiVersion</span></span>
<span data-ttu-id="a92c0-121">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a92c0-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a92c0-122">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a92c0-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a92c0-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a92c0-123">-AsJob</span></span>
<span data-ttu-id="a92c0-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a92c0-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a92c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92c0-125">-DefaultProfile</span></span>
<span data-ttu-id="a92c0-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a92c0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92c0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="a92c0-127">-Force</span></span>
<span data-ttu-id="a92c0-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a92c0-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a92c0-129">-ID</span><span class="sxs-lookup"><span data-stu-id="a92c0-129">-Id</span></span>
<span data-ttu-id="a92c0-130">Указывает идентификатор группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a92c0-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="a92c0-131">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="a92c0-131">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a92c0-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a92c0-132">-Name</span></span>
<span data-ttu-id="a92c0-133">Указывает имена групп ресурсов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a92c0-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="a92c0-134">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="a92c0-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a92c0-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a92c0-135">-Pre</span></span>
<span data-ttu-id="a92c0-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a92c0-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a92c0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a92c0-137">-Confirm</span></span>
<span data-ttu-id="a92c0-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a92c0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92c0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92c0-139">-WhatIf</span></span>
<span data-ttu-id="a92c0-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a92c0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92c0-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a92c0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92c0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92c0-142">CommonParameters</span></span>
<span data-ttu-id="a92c0-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a92c0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92c0-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92c0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92c0-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a92c0-145">INPUTS</span></span>

### <span data-ttu-id="a92c0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a92c0-146">System.String</span></span>

## <span data-ttu-id="a92c0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92c0-147">OUTPUTS</span></span>

### <span data-ttu-id="a92c0-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a92c0-148">System.Boolean</span></span>

## <span data-ttu-id="a92c0-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="a92c0-149">NOTES</span></span>

## <span data-ttu-id="a92c0-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a92c0-150">RELATED LINKS</span></span>

[<span data-ttu-id="a92c0-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a92c0-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="a92c0-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a92c0-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a92c0-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a92c0-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


