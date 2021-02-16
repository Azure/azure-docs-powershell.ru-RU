---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220396"
---
# <span data-ttu-id="fc4f8-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="fc4f8-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="fc4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4f8-103">Обновление управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="fc4f8-103">Updates managed application</span></span>

## <span data-ttu-id="fc4f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc4f8-104">SYNTAX</span></span>

### <span data-ttu-id="fc4f8-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc4f8-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4f8-106">SetById</span><span class="sxs-lookup"><span data-stu-id="fc4f8-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4f8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc4f8-107">DESCRIPTION</span></span>
<span data-ttu-id="fc4f8-108">**Cmdlet Set-AzManagedApplication** обновляет управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="fc4f8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc4f8-109">EXAMPLES</span></span>

### <span data-ttu-id="fc4f8-110">Пример 1. Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="fc4f8-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="fc4f8-111">Эта команда обновляет описание управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-111">This command updates the managed application description</span></span>

## <span data-ttu-id="fc4f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc4f8-112">PARAMETERS</span></span>

### <span data-ttu-id="fc4f8-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc4f8-113">-ApiVersion</span></span>
<span data-ttu-id="fc4f8-114">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc4f8-115">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fc4f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4f8-116">-DefaultProfile</span></span>
<span data-ttu-id="fc4f8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc4f8-118">-Id</span><span class="sxs-lookup"><span data-stu-id="fc4f8-118">-Id</span></span>
<span data-ttu-id="fc4f8-119">Полностью управляемый ИД приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="fc4f8-120">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4f8-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="fc4f8-121">-Kind</span></span>
<span data-ttu-id="fc4f8-122">Тип управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-122">The managed application kind.</span></span>
<span data-ttu-id="fc4f8-123">Один из marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="fc4f8-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="fc4f8-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fc4f8-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="fc4f8-125">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4f8-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="fc4f8-127">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-127">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="fc4f8-128">-Name</span></span>
<span data-ttu-id="fc4f8-129">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="fc4f8-130">-Parameter</span></span>
<span data-ttu-id="fc4f8-131">Строка параметров в формате JSON для управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="fc4f8-132">Это может быть путь к имени файла или URI, содержащий параметры, или параметры в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="fc4f8-133">-Plan</span></span>
<span data-ttu-id="fc4f8-134">Hash table which represents managed application plan properties.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc4f8-135">-Pre</span></span>
<span data-ttu-id="fc4f8-136">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fc4f8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4f8-137">-ResourceGroupName</span></span>
<span data-ttu-id="fc4f8-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc4f8-139">-Tag</span></span>
<span data-ttu-id="fc4f8-140">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4f8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc4f8-141">-Confirm</span></span>
<span data-ttu-id="fc4f8-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4f8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4f8-143">-WhatIf</span></span>
<span data-ttu-id="fc4f8-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4f8-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4f8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4f8-146">CommonParameters</span></span>
<span data-ttu-id="fc4f8-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4f8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4f8-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc4f8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4f8-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc4f8-149">INPUTS</span></span>

### <span data-ttu-id="fc4f8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="fc4f8-150">System.String</span></span>

### <span data-ttu-id="fc4f8-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc4f8-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc4f8-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc4f8-152">OUTPUTS</span></span>

### <span data-ttu-id="fc4f8-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="fc4f8-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fc4f8-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc4f8-154">NOTES</span></span>

## <span data-ttu-id="fc4f8-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc4f8-155">RELATED LINKS</span></span>
