---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505170"
---
# <span data-ttu-id="5dfe0-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="5dfe0-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="5dfe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dfe0-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfe0-103">Удаление определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="5dfe0-103">Removes a managed application definition</span></span>

## <span data-ttu-id="5dfe0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5dfe0-104">SYNTAX</span></span>

### <span data-ttu-id="5dfe0-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5dfe0-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dfe0-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="5dfe0-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dfe0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dfe0-107">DESCRIPTION</span></span>
<span data-ttu-id="5dfe0-108">Для удаления определения управляемого приложения удаляется **cmdlet Remove-AzManagedApplicationDefinition.**</span><span class="sxs-lookup"><span data-stu-id="5dfe0-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="5dfe0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5dfe0-109">EXAMPLES</span></span>

### <span data-ttu-id="5dfe0-110">Пример 1. Удаление определения управляемого приложения по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="5dfe0-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="5dfe0-111">Первая команда получает управляемое определение приложения myAppDef с помощью Get-AzManagedApplicationDefinition командлета.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="5dfe0-112">Команда сохраняет ее в переменной $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="5dfe0-113">Вторая команда удаляет определение управляемого приложения, заданное **свойством ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="5dfe0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dfe0-114">PARAMETERS</span></span>

### <span data-ttu-id="5dfe0-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5dfe0-115">-ApiVersion</span></span>
<span data-ttu-id="5dfe0-116">Указывает на версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5dfe0-117">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5dfe0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfe0-118">-DefaultProfile</span></span>
<span data-ttu-id="5dfe0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dfe0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5dfe0-120">-Force</span></span>
<span data-ttu-id="5dfe0-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5dfe0-122">-Id</span><span class="sxs-lookup"><span data-stu-id="5dfe0-122">-Id</span></span>
<span data-ttu-id="5dfe0-123">Полного ИД определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="5dfe0-124">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="5dfe0-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5dfe0-125">-Name</span></span>
<span data-ttu-id="5dfe0-126">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe0-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="5dfe0-127">-Pre</span></span>
<span data-ttu-id="5dfe0-128">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5dfe0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfe0-129">-ResourceGroupName</span></span>
<span data-ttu-id="5dfe0-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dfe0-131">-Confirm</span></span>
<span data-ttu-id="5dfe0-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dfe0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dfe0-133">-WhatIf</span></span>
<span data-ttu-id="5dfe0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfe0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dfe0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfe0-136">CommonParameters</span></span>
<span data-ttu-id="5dfe0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfe0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfe0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dfe0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfe0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dfe0-139">INPUTS</span></span>

### <span data-ttu-id="5dfe0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5dfe0-140">System.String</span></span>

## <span data-ttu-id="5dfe0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5dfe0-141">OUTPUTS</span></span>

### <span data-ttu-id="5dfe0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5dfe0-142">System.Boolean</span></span>

## <span data-ttu-id="5dfe0-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5dfe0-143">NOTES</span></span>

## <span data-ttu-id="5dfe0-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dfe0-144">RELATED LINKS</span></span>
