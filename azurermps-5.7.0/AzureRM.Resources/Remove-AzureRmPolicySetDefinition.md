---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566128"
---
# <span data-ttu-id="0fb5d-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="0fb5d-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="0fb5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb5d-103">Удаление определения политики.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fb5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fb5d-104">SYNTAX</span></span>

### <span data-ttu-id="0fb5d-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fb5d-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb5d-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="0fb5d-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb5d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fb5d-107">DESCRIPTION</span></span>
<span data-ttu-id="0fb5d-108">Командлет **Remove-AzureRmPolicySetDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="0fb5d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fb5d-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb5d-110">Пример 1: Удаление определения политики для идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="0fb5d-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="0fb5d-111">Первая команда получает определение политики с помощью командлета Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="0fb5d-112">Команда сохраняет его в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="0fb5d-113">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="0fb5d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fb5d-114">PARAMETERS</span></span>

### <span data-ttu-id="0fb5d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0fb5d-115">-ApiVersion</span></span>
<span data-ttu-id="0fb5d-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0fb5d-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0fb5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb5d-118">-DefaultProfile</span></span>
<span data-ttu-id="0fb5d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0fb5d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fb5d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0fb5d-120">-Force</span></span>
<span data-ttu-id="0fb5d-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0fb5d-122">-ID</span><span class="sxs-lookup"><span data-stu-id="0fb5d-122">-Id</span></span>
<span data-ttu-id="0fb5d-123">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="0fb5d-124">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0fb5d-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb5d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fb5d-125">-Name</span></span>
<span data-ttu-id="0fb5d-126">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb5d-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="0fb5d-127">-Pre</span></span>
<span data-ttu-id="0fb5d-128">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0fb5d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fb5d-129">-Confirm</span></span>
<span data-ttu-id="0fb5d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb5d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb5d-131">-WhatIf</span></span>
<span data-ttu-id="0fb5d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fb5d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb5d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb5d-134">CommonParameters</span></span>
<span data-ttu-id="0fb5d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fb5d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb5d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb5d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb5d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fb5d-137">INPUTS</span></span>

### <span data-ttu-id="0fb5d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0fb5d-138">System.String</span></span>

## <span data-ttu-id="0fb5d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fb5d-139">OUTPUTS</span></span>

### <span data-ttu-id="0fb5d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fb5d-140">System.Boolean</span></span>

## <span data-ttu-id="0fb5d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fb5d-141">NOTES</span></span>

## <span data-ttu-id="0fb5d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fb5d-142">RELATED LINKS</span></span>
