---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567061"
---
# <span data-ttu-id="53866-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53866-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="53866-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53866-102">SYNOPSIS</span></span>
<span data-ttu-id="53866-103">Удаляет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53866-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53866-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53866-104">SYNTAX</span></span>

### <span data-ttu-id="53866-105">Перечень групп ресурсов на основе имени.</span><span class="sxs-lookup"><span data-stu-id="53866-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="53866-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="53866-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53866-107">Список группы ресурсов на основе идентификатора.</span><span class="sxs-lookup"><span data-stu-id="53866-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53866-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53866-108">DESCRIPTION</span></span>
<span data-ttu-id="53866-109">Командлет **Remove-AzureRmResourceGroup** удаляет группу ресурсов Azure и ее ресурсы из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="53866-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="53866-110">Чтобы удалить ресурс, но оставить группу ресурсов, используйте командлет Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="53866-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="53866-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53866-111">EXAMPLES</span></span>

### <span data-ttu-id="53866-112">Пример 1: Удаление группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="53866-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="53866-113">Эта команда удаляет группу ресурсов ContosoRG01 из подписки.</span><span class="sxs-lookup"><span data-stu-id="53866-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="53866-114">Командлет запрашивает подтверждение и не возвращает результаты.</span><span class="sxs-lookup"><span data-stu-id="53866-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="53866-115">Пример 2: Удаление группы ресурсов без подтверждения</span><span class="sxs-lookup"><span data-stu-id="53866-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="53866-116">Эта команда использует командлет Get-AzureRmResourceGroup для получения группы ресурсов ContosoRG01, а затем передает его в **Remove-AzureRmResourceGroup** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="53866-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="53866-117">Параметр *verbose* Common возвращает сведения о состоянии операции, а параметр *Force* подавляет вывод запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="53866-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="53866-118">Пример 3: удаление всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="53866-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="53866-119">Эта команда использует командлет **Get-AzureRmResourceGroup** для получения всех групп ресурсов, а затем передает их в **Remove-AzureRmResourceGroup** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="53866-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="53866-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53866-120">PARAMETERS</span></span>

### <span data-ttu-id="53866-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53866-121">-ApiVersion</span></span>
<span data-ttu-id="53866-122">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53866-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="53866-123">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53866-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="53866-124">-Force</span><span class="sxs-lookup"><span data-stu-id="53866-124">-Force</span></span>
<span data-ttu-id="53866-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="53866-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53866-126">-ID</span><span class="sxs-lookup"><span data-stu-id="53866-126">-Id</span></span>
<span data-ttu-id="53866-127">Указывает идентификатор группы ресурсов, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="53866-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="53866-128">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="53866-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53866-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53866-129">-Name</span></span>
<span data-ttu-id="53866-130">Указывает имена групп ресурсов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="53866-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="53866-131">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="53866-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53866-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="53866-132">-Pre</span></span>
<span data-ttu-id="53866-133">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="53866-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53866-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53866-134">-Confirm</span></span>
<span data-ttu-id="53866-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53866-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53866-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53866-136">-WhatIf</span></span>
<span data-ttu-id="53866-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53866-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53866-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53866-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53866-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53866-139">-DefaultProfile</span></span>
<span data-ttu-id="53866-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53866-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53866-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53866-141">CommonParameters</span></span>
<span data-ttu-id="53866-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53866-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53866-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53866-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53866-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53866-144">INPUTS</span></span>

### <span data-ttu-id="53866-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="53866-145">None</span></span>

## <span data-ttu-id="53866-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53866-146">OUTPUTS</span></span>

### <span data-ttu-id="53866-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="53866-147">None</span></span>

## <span data-ttu-id="53866-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="53866-148">NOTES</span></span>

## <span data-ttu-id="53866-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53866-149">RELATED LINKS</span></span>

[<span data-ttu-id="53866-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53866-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="53866-151">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53866-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="53866-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53866-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


