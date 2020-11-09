---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 4f21ce7a14873d201fa18f45c96d508dcd38cb8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244677"
---
# <span data-ttu-id="58ebd-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="58ebd-101">Move-AzResource</span></span>

## <span data-ttu-id="58ebd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="58ebd-103">Перемещает ресурс в другую группу ресурсов или подписку.</span><span class="sxs-lookup"><span data-stu-id="58ebd-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="58ebd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58ebd-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ebd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="58ebd-106">Командлет **Move-AzResource** перемещает существующие ресурсы в другую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58ebd-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="58ebd-107">Эта группа ресурсов может входить в другую подписку.</span><span class="sxs-lookup"><span data-stu-id="58ebd-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="58ebd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58ebd-108">EXAMPLES</span></span>

### <span data-ttu-id="58ebd-109">Пример 1: перемещение ресурса в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="58ebd-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="58ebd-110">Первая команда получает ресурс с именем ContosoStorageAccount с помощью командлета Get-AzResource и сохраняет этот ресурс в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="58ebd-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="58ebd-111">Вторая команда перемещает этот ресурс в группу ресурсов с именем ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="58ebd-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="58ebd-112">Команда определяет ресурс для перемещения с помощью свойства **ResourceId** для $Resource.</span><span class="sxs-lookup"><span data-stu-id="58ebd-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="58ebd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="58ebd-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="58ebd-114">-ApiVersion</span></span>
<span data-ttu-id="58ebd-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58ebd-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="58ebd-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="58ebd-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="58ebd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ebd-117">-DefaultProfile</span></span>
<span data-ttu-id="58ebd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="58ebd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58ebd-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ebd-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="58ebd-120">Указывает имя группы ресурсов, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="58ebd-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ebd-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58ebd-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="58ebd-122">Указывает идентификатор подписки, в которую этот командлет перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="58ebd-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ebd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="58ebd-123">-Force</span></span>
<span data-ttu-id="58ebd-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="58ebd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58ebd-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="58ebd-125">-Pre</span></span>
<span data-ttu-id="58ebd-126">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="58ebd-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="58ebd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ebd-127">-ResourceId</span></span>
<span data-ttu-id="58ebd-128">Задает массив идентификаторов ресурсов, перемещаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="58ebd-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58ebd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ebd-129">-Confirm</span></span>
<span data-ttu-id="58ebd-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58ebd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ebd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ebd-131">-WhatIf</span></span>
<span data-ttu-id="58ebd-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58ebd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ebd-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58ebd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ebd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ebd-134">CommonParameters</span></span>
<span data-ttu-id="58ebd-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58ebd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ebd-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58ebd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ebd-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58ebd-137">INPUTS</span></span>

### <span data-ttu-id="58ebd-138">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58ebd-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="58ebd-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="58ebd-139">System.String[]</span></span>

## <span data-ttu-id="58ebd-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ebd-140">OUTPUTS</span></span>

### <span data-ttu-id="58ebd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58ebd-141">System.Boolean</span></span>

## <span data-ttu-id="58ebd-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="58ebd-142">NOTES</span></span>

## <span data-ttu-id="58ebd-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58ebd-143">RELATED LINKS</span></span>

[<span data-ttu-id="58ebd-144">Find-AzResource</span><span class="sxs-lookup"><span data-stu-id="58ebd-144">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="58ebd-145">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="58ebd-145">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="58ebd-146">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="58ebd-146">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="58ebd-147">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="58ebd-147">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="58ebd-148">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="58ebd-148">Set-AzResource</span></span>](./Set-AzResource.md)

