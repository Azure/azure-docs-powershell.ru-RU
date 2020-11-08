---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065264"
---
# <span data-ttu-id="125cd-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="125cd-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="125cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="125cd-102">SYNOPSIS</span></span>
<span data-ttu-id="125cd-103">Удаляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="125cd-103">Removes a managed application definition</span></span>

## <span data-ttu-id="125cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="125cd-104">SYNTAX</span></span>

### <span data-ttu-id="125cd-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="125cd-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="125cd-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="125cd-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="125cd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="125cd-107">DESCRIPTION</span></span>
<span data-ttu-id="125cd-108">Командлет **Remove-AzManagedApplicationDefinition** удаляет определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="125cd-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="125cd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="125cd-109">EXAMPLES</span></span>

### <span data-ttu-id="125cd-110">Пример 1: Удаление определения управляемого приложения с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="125cd-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="125cd-111">Первая команда получает определение управляемого приложения с именем myAppDef с помощью командлета Get-AzManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="125cd-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="125cd-112">Команда сохраняет его в переменной $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="125cd-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="125cd-113">Вторая команда удаляет определение управляемого приложения, определяемое свойством **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="125cd-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="125cd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="125cd-114">PARAMETERS</span></span>

### <span data-ttu-id="125cd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="125cd-115">-ApiVersion</span></span>
<span data-ttu-id="125cd-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="125cd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="125cd-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="125cd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="125cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125cd-118">-DefaultProfile</span></span>
<span data-ttu-id="125cd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="125cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="125cd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="125cd-120">-Force</span></span>
<span data-ttu-id="125cd-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="125cd-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="125cd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="125cd-122">-Id</span></span>
<span data-ttu-id="125cd-123">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="125cd-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="125cd-124">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="125cd-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="125cd-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="125cd-125">-Name</span></span>
<span data-ttu-id="125cd-126">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="125cd-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="125cd-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="125cd-127">-Pre</span></span>
<span data-ttu-id="125cd-128">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="125cd-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="125cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="125cd-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="125cd-130">The resource group name.</span></span>

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

### <span data-ttu-id="125cd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="125cd-131">-Confirm</span></span>
<span data-ttu-id="125cd-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="125cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125cd-133">-WhatIf</span></span>
<span data-ttu-id="125cd-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="125cd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125cd-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="125cd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125cd-136">CommonParameters</span></span>
<span data-ttu-id="125cd-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="125cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125cd-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="125cd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125cd-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="125cd-139">INPUTS</span></span>

### <span data-ttu-id="125cd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="125cd-140">System.String</span></span>

## <span data-ttu-id="125cd-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="125cd-141">OUTPUTS</span></span>

### <span data-ttu-id="125cd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="125cd-142">System.Boolean</span></span>

## <span data-ttu-id="125cd-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="125cd-143">NOTES</span></span>

## <span data-ttu-id="125cd-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="125cd-144">RELATED LINKS</span></span>
