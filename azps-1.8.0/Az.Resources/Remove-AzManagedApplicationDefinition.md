---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 42acc50c5e370f20e168e6c7cd757f57b1dacc4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729348"
---
# <span data-ttu-id="680fa-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="680fa-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="680fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="680fa-102">SYNOPSIS</span></span>
<span data-ttu-id="680fa-103">Удаляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="680fa-103">Removes a managed application definition</span></span>

## <span data-ttu-id="680fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="680fa-104">SYNTAX</span></span>

### <span data-ttu-id="680fa-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="680fa-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="680fa-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="680fa-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="680fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="680fa-107">DESCRIPTION</span></span>
<span data-ttu-id="680fa-108">Командлет **Remove-AzManagedApplicationDefinition** удаляет определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="680fa-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="680fa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="680fa-109">EXAMPLES</span></span>

### <span data-ttu-id="680fa-110">Пример 1: Удаление определения управляемого приложения с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="680fa-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="680fa-111">Первая команда получает определение управляемого приложения с именем myAppDef с помощью командлета Get-AzManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="680fa-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="680fa-112">Команда сохраняет его в переменной $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="680fa-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="680fa-113">Вторая команда удаляет определение управляемого приложения, определяемое свойством **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="680fa-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="680fa-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="680fa-114">PARAMETERS</span></span>

### <span data-ttu-id="680fa-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="680fa-115">-ApiVersion</span></span>
<span data-ttu-id="680fa-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="680fa-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="680fa-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="680fa-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="680fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="680fa-118">-DefaultProfile</span></span>
<span data-ttu-id="680fa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="680fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="680fa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="680fa-120">-Force</span></span>
<span data-ttu-id="680fa-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="680fa-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="680fa-122">-ID</span><span class="sxs-lookup"><span data-stu-id="680fa-122">-Id</span></span>
<span data-ttu-id="680fa-123">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="680fa-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="680fa-124">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="680fa-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="680fa-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="680fa-125">-Name</span></span>
<span data-ttu-id="680fa-126">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="680fa-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="680fa-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="680fa-127">-Pre</span></span>
<span data-ttu-id="680fa-128">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="680fa-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="680fa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="680fa-129">-ResourceGroupName</span></span>
<span data-ttu-id="680fa-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="680fa-130">The resource group name.</span></span>

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

### <span data-ttu-id="680fa-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="680fa-131">-Confirm</span></span>
<span data-ttu-id="680fa-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="680fa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="680fa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="680fa-133">-WhatIf</span></span>
<span data-ttu-id="680fa-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="680fa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="680fa-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="680fa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="680fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680fa-136">CommonParameters</span></span>
<span data-ttu-id="680fa-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="680fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680fa-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="680fa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680fa-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="680fa-139">INPUTS</span></span>

### <span data-ttu-id="680fa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="680fa-140">System.String</span></span>

## <span data-ttu-id="680fa-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="680fa-141">OUTPUTS</span></span>

### <span data-ttu-id="680fa-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="680fa-142">System.Boolean</span></span>

## <span data-ttu-id="680fa-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="680fa-143">NOTES</span></span>

## <span data-ttu-id="680fa-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="680fa-144">RELATED LINKS</span></span>
