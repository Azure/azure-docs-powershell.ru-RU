---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565168"
---
# <span data-ttu-id="43f1a-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="43f1a-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="43f1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="43f1a-103">Изменение определения Set политики</span><span class="sxs-lookup"><span data-stu-id="43f1a-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43f1a-104">SYNTAX</span></span>

### <span data-ttu-id="43f1a-105">Параметр имени определения политики задает.</span><span class="sxs-lookup"><span data-stu-id="43f1a-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="43f1a-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="43f1a-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43f1a-107">Параметр идентификатора определения политики задает значение.</span><span class="sxs-lookup"><span data-stu-id="43f1a-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f1a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43f1a-108">DESCRIPTION</span></span>
<span data-ttu-id="43f1a-109">Командлет **Set-AzureRmPolicySetDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="43f1a-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="43f1a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43f1a-110">EXAMPLES</span></span>

### <span data-ttu-id="43f1a-111">Пример 1: Обновление описания определения набора политик</span><span class="sxs-lookup"><span data-stu-id="43f1a-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="43f1a-112">Первая команда получает определение политики с помощью командлета Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="43f1a-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="43f1a-113">Команда сохраняет этот объект в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="43f1a-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="43f1a-114">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="43f1a-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="43f1a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43f1a-115">PARAMETERS</span></span>

### <span data-ttu-id="43f1a-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="43f1a-116">-ApiVersion</span></span>
<span data-ttu-id="43f1a-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43f1a-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="43f1a-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="43f1a-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="43f1a-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="43f1a-119">-Description</span></span>
<span data-ttu-id="43f1a-120">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="43f1a-120">The description for policy set definition.</span></span>

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

### <span data-ttu-id="43f1a-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="43f1a-121">-DisplayName</span></span>
<span data-ttu-id="43f1a-122">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="43f1a-122">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="43f1a-123">-ID</span><span class="sxs-lookup"><span data-stu-id="43f1a-123">-Id</span></span>
<span data-ttu-id="43f1a-124">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="43f1a-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="43f1a-125">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="43f1a-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f1a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43f1a-126">-Name</span></span>
<span data-ttu-id="43f1a-127">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="43f1a-127">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f1a-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="43f1a-128">-PolicyDefinition</span></span>
<span data-ttu-id="43f1a-129">Определение настройки политики.</span><span class="sxs-lookup"><span data-stu-id="43f1a-129">The policy set definition.</span></span> <span data-ttu-id="43f1a-130">Это может быть путь к имени файла, содержащему определения политики, или определению политики как String.</span><span class="sxs-lookup"><span data-stu-id="43f1a-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="43f1a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="43f1a-131">-Pre</span></span>
<span data-ttu-id="43f1a-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="43f1a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="43f1a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43f1a-133">-Confirm</span></span>
<span data-ttu-id="43f1a-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43f1a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f1a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f1a-135">-DefaultProfile</span></span>
<span data-ttu-id="43f1a-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43f1a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43f1a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f1a-137">-WhatIf</span></span>
<span data-ttu-id="43f1a-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43f1a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43f1a-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43f1a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f1a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f1a-140">CommonParameters</span></span>
<span data-ttu-id="43f1a-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43f1a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f1a-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f1a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f1a-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43f1a-143">INPUTS</span></span>

### <span data-ttu-id="43f1a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="43f1a-144">System.String</span></span>

## <span data-ttu-id="43f1a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43f1a-145">OUTPUTS</span></span>

### <span data-ttu-id="43f1a-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="43f1a-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="43f1a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="43f1a-147">NOTES</span></span>

## <span data-ttu-id="43f1a-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43f1a-148">RELATED LINKS</span></span>

