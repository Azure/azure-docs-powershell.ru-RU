---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 41f59b46595d45932010b1fcbedae07cdeca5f78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971779"
---
# <span data-ttu-id="5d9e5-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="5d9e5-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="5d9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9e5-103">Удаление управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="5d9e5-103">Removes a managed application</span></span>

## <span data-ttu-id="5d9e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d9e5-104">SYNTAX</span></span>

### <span data-ttu-id="5d9e5-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d9e5-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d9e5-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="5d9e5-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d9e5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d9e5-107">DESCRIPTION</span></span>
<span data-ttu-id="5d9e5-108">Из-за этого управляемые приложения удаляются с применением **cmdlet Remove-AzManagedApplication.**</span><span class="sxs-lookup"><span data-stu-id="5d9e5-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="5d9e5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d9e5-109">EXAMPLES</span></span>

### <span data-ttu-id="5d9e5-110">Пример 1. Удаление управляемого приложения по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="5d9e5-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="5d9e5-111">Первая команда получает управляемое приложение myApp с помощью Get-AzManagedApplication командлета.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="5d9e5-112">Команда сохраняет ее в переменной $Application.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="5d9e5-113">Вторая команда удаляет управляемое приложение, которое определено **свойством ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="5d9e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d9e5-114">PARAMETERS</span></span>

### <span data-ttu-id="5d9e5-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5d9e5-115">-ApiVersion</span></span>
<span data-ttu-id="5d9e5-116">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5d9e5-117">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5d9e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9e5-118">-DefaultProfile</span></span>
<span data-ttu-id="5d9e5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d9e5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5d9e5-120">-Force</span></span>
<span data-ttu-id="5d9e5-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5d9e5-122">-Id</span><span class="sxs-lookup"><span data-stu-id="5d9e5-122">-Id</span></span>
<span data-ttu-id="5d9e5-123">Полностью управляемый ИД приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="5d9e5-124">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="5d9e5-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="5d9e5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5d9e5-125">-Name</span></span>
<span data-ttu-id="5d9e5-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-126">The managed application name.</span></span>

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

### <span data-ttu-id="5d9e5-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="5d9e5-127">-Pre</span></span>
<span data-ttu-id="5d9e5-128">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5d9e5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d9e5-129">-ResourceGroupName</span></span>
<span data-ttu-id="5d9e5-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-130">The resource group name.</span></span>

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

### <span data-ttu-id="5d9e5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d9e5-131">-Confirm</span></span>
<span data-ttu-id="5d9e5-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d9e5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d9e5-133">-WhatIf</span></span>
<span data-ttu-id="5d9e5-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d9e5-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d9e5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9e5-136">CommonParameters</span></span>
<span data-ttu-id="5d9e5-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d9e5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9e5-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d9e5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9e5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d9e5-139">INPUTS</span></span>

### <span data-ttu-id="5d9e5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5d9e5-140">System.String</span></span>

## <span data-ttu-id="5d9e5-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d9e5-141">OUTPUTS</span></span>

### <span data-ttu-id="5d9e5-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d9e5-142">System.Boolean</span></span>

## <span data-ttu-id="5d9e5-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d9e5-143">NOTES</span></span>

## <span data-ttu-id="5d9e5-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d9e5-144">RELATED LINKS</span></span>
