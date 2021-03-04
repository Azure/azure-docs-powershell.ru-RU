---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 16e43df2da9509d7fb222f3299a4c611d146026c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962659"
---
# <span data-ttu-id="16c56-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="16c56-101">Move-AzResource</span></span>

## <span data-ttu-id="16c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c56-102">SYNOPSIS</span></span>
<span data-ttu-id="16c56-103">Перемещение ресурса в другую группу ресурсов или подписку.</span><span class="sxs-lookup"><span data-stu-id="16c56-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="16c56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16c56-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c56-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c56-105">DESCRIPTION</span></span>
<span data-ttu-id="16c56-106">Для перемещения существующих ресурсов в другую **группу перемещается ресурс AzResource.**</span><span class="sxs-lookup"><span data-stu-id="16c56-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="16c56-107">Группа ресурсов может быть в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="16c56-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="16c56-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16c56-108">EXAMPLES</span></span>

### <span data-ttu-id="16c56-109">Пример 1. Перемещение ресурса в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="16c56-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="16c56-110">Первая команда получает ресурс с именем ContosoStorageAccount с помощью командлета Get-AzResource, а затем сохраняет его в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="16c56-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="16c56-111">Вторая команда перемещает этот ресурс в группу ресурсов с именем ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="16c56-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="16c56-112">Команда определяет ресурс, который нужно переместить, с помощью свойства **ResourceId** $Resource.</span><span class="sxs-lookup"><span data-stu-id="16c56-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="16c56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c56-113">PARAMETERS</span></span>

### <span data-ttu-id="16c56-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="16c56-114">-ApiVersion</span></span>
<span data-ttu-id="16c56-115">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16c56-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="16c56-116">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="16c56-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="16c56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c56-117">-DefaultProfile</span></span>
<span data-ttu-id="16c56-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16c56-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16c56-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c56-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="16c56-120">Имя группы ресурсов, в которую этот cmdlet перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="16c56-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="16c56-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16c56-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="16c56-122">Определяет код подписки, в которую этот cmdlet перемещает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="16c56-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="16c56-123">-Force</span><span class="sxs-lookup"><span data-stu-id="16c56-123">-Force</span></span>
<span data-ttu-id="16c56-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="16c56-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16c56-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="16c56-125">-Pre</span></span>
<span data-ttu-id="16c56-126">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="16c56-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="16c56-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16c56-127">-ResourceId</span></span>
<span data-ttu-id="16c56-128">Определяет массив кодов ресурсов, перемещаемых этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16c56-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="16c56-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16c56-129">-Confirm</span></span>
<span data-ttu-id="16c56-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="16c56-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c56-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c56-131">-WhatIf</span></span>
<span data-ttu-id="16c56-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16c56-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c56-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="16c56-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c56-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c56-134">CommonParameters</span></span>
<span data-ttu-id="16c56-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c56-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c56-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16c56-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c56-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16c56-137">INPUTS</span></span>

### <span data-ttu-id="16c56-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="16c56-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="16c56-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="16c56-139">System.String[]</span></span>

## <span data-ttu-id="16c56-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16c56-140">OUTPUTS</span></span>

### <span data-ttu-id="16c56-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16c56-141">System.Boolean</span></span>

## <span data-ttu-id="16c56-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16c56-142">NOTES</span></span>

## <span data-ttu-id="16c56-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c56-143">RELATED LINKS</span></span>

[<span data-ttu-id="16c56-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="16c56-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="16c56-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="16c56-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="16c56-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="16c56-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="16c56-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="16c56-147">Set-AzResource</span></span>](./Set-AzResource.md)


