---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557172"
---
# <span data-ttu-id="c33b7-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c33b7-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="c33b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c33b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c33b7-103">Изменение определения Set политики</span><span class="sxs-lookup"><span data-stu-id="c33b7-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c33b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c33b7-104">SYNTAX</span></span>

### <span data-ttu-id="c33b7-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c33b7-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c33b7-106">SetById</span><span class="sxs-lookup"><span data-stu-id="c33b7-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c33b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c33b7-107">DESCRIPTION</span></span>
<span data-ttu-id="c33b7-108">Командлет **Set-AzureRmPolicySetDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="c33b7-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="c33b7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c33b7-109">EXAMPLES</span></span>

### <span data-ttu-id="c33b7-110">Пример 1: Обновление описания определения набора политик</span><span class="sxs-lookup"><span data-stu-id="c33b7-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="c33b7-111">Первая команда получает определение политики с помощью командлета Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c33b7-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="c33b7-112">Команда сохраняет этот объект в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c33b7-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="c33b7-113">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="c33b7-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="c33b7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c33b7-114">PARAMETERS</span></span>

### <span data-ttu-id="c33b7-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c33b7-115">-ApiVersion</span></span>
<span data-ttu-id="c33b7-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c33b7-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c33b7-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="c33b7-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33b7-118">-DefaultProfile</span></span>
<span data-ttu-id="c33b7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c33b7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="c33b7-120">-Description</span></span>
<span data-ttu-id="c33b7-121">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="c33b7-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c33b7-122">-DisplayName</span></span>
<span data-ttu-id="c33b7-123">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="c33b7-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c33b7-124">-Id</span></span>
<span data-ttu-id="c33b7-125">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="c33b7-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="c33b7-126">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c33b7-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c33b7-127">-Name</span></span>
<span data-ttu-id="c33b7-128">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="c33b7-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c33b7-129">-PolicyDefinition</span></span>
<span data-ttu-id="c33b7-130">Определение настройки политики.</span><span class="sxs-lookup"><span data-stu-id="c33b7-130">The policy set definition.</span></span> <span data-ttu-id="c33b7-131">Это может быть путь к имени файла, содержащему определения политики, или определению политики как String.</span><span class="sxs-lookup"><span data-stu-id="c33b7-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="c33b7-132">-Pre</span></span>
<span data-ttu-id="c33b7-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="c33b7-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c33b7-134">-Confirm</span></span>
<span data-ttu-id="c33b7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c33b7-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33b7-136">-WhatIf</span></span>
<span data-ttu-id="c33b7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c33b7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c33b7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c33b7-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33b7-139">CommonParameters</span></span>
<span data-ttu-id="c33b7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c33b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33b7-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c33b7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33b7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c33b7-142">INPUTS</span></span>

### <span data-ttu-id="c33b7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c33b7-143">System.String</span></span>

## <span data-ttu-id="c33b7-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c33b7-144">OUTPUTS</span></span>

### <span data-ttu-id="c33b7-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c33b7-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c33b7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c33b7-146">NOTES</span></span>

## <span data-ttu-id="c33b7-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c33b7-147">RELATED LINKS</span></span>
