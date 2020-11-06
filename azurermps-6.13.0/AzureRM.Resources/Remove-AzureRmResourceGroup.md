---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: f59aca506ca9cb9e02c5b76f401d32ec314b864d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568157"
---
# <span data-ttu-id="91dcb-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91dcb-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="91dcb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="91dcb-103">Удаляет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91dcb-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91dcb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91dcb-104">SYNTAX</span></span>

### <span data-ttu-id="91dcb-105">RemoveByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91dcb-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91dcb-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="91dcb-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91dcb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91dcb-107">DESCRIPTION</span></span>
<span data-ttu-id="91dcb-108">Командлет **Remove-AzureRmResourceGroup** удаляет группу ресурсов Azure и ее ресурсы из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="91dcb-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="91dcb-109">Чтобы удалить ресурс, но оставить группу ресурсов, используйте командлет Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="91dcb-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="91dcb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91dcb-110">EXAMPLES</span></span>

### <span data-ttu-id="91dcb-111">Пример 1: Удаление группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="91dcb-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="91dcb-112">Эта команда удаляет группу ресурсов ContosoRG01 из подписки.</span><span class="sxs-lookup"><span data-stu-id="91dcb-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="91dcb-113">Командлет запрашивает подтверждение и не возвращает результаты.</span><span class="sxs-lookup"><span data-stu-id="91dcb-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="91dcb-114">Пример 2: Удаление группы ресурсов без подтверждения</span><span class="sxs-lookup"><span data-stu-id="91dcb-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="91dcb-115">Эта команда использует командлет Get-AzureRmResourceGroup для получения группы ресурсов ContosoRG01, а затем передает его в **Remove-AzureRmResourceGroup** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="91dcb-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="91dcb-116">Параметр *verbose* Common возвращает сведения о состоянии операции, а параметр *Force* подавляет вывод запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="91dcb-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="91dcb-117">Пример 3: удаление всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="91dcb-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="91dcb-118">Эта команда использует командлет **Get-AzureRmResourceGroup** для получения всех групп ресурсов, а затем передает их в **Remove-AzureRmResourceGroup** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="91dcb-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="91dcb-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91dcb-119">PARAMETERS</span></span>

### <span data-ttu-id="91dcb-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="91dcb-120">-ApiVersion</span></span>
<span data-ttu-id="91dcb-121">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91dcb-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="91dcb-122">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91dcb-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="91dcb-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91dcb-123">-AsJob</span></span>
<span data-ttu-id="91dcb-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="91dcb-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91dcb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dcb-125">-DefaultProfile</span></span>
<span data-ttu-id="91dcb-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="91dcb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91dcb-127">-Force</span><span class="sxs-lookup"><span data-stu-id="91dcb-127">-Force</span></span>
<span data-ttu-id="91dcb-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="91dcb-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91dcb-129">-ID</span><span class="sxs-lookup"><span data-stu-id="91dcb-129">-Id</span></span>
<span data-ttu-id="91dcb-130">Указывает идентификатор группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="91dcb-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="91dcb-131">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="91dcb-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91dcb-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91dcb-132">-Name</span></span>
<span data-ttu-id="91dcb-133">Указывает имена групп ресурсов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="91dcb-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="91dcb-134">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="91dcb-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="91dcb-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="91dcb-135">-Pre</span></span>
<span data-ttu-id="91dcb-136">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="91dcb-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="91dcb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91dcb-137">-Confirm</span></span>
<span data-ttu-id="91dcb-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="91dcb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91dcb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91dcb-139">-WhatIf</span></span>
<span data-ttu-id="91dcb-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="91dcb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91dcb-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="91dcb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91dcb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dcb-142">CommonParameters</span></span>
<span data-ttu-id="91dcb-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91dcb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dcb-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91dcb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dcb-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91dcb-145">INPUTS</span></span>

## <span data-ttu-id="91dcb-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91dcb-146">OUTPUTS</span></span>

## <span data-ttu-id="91dcb-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="91dcb-147">NOTES</span></span>

## <span data-ttu-id="91dcb-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91dcb-148">RELATED LINKS</span></span>

[<span data-ttu-id="91dcb-149">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91dcb-149">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="91dcb-150">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91dcb-150">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="91dcb-151">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91dcb-151">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


