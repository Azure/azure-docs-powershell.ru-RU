---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733326"
---
# <span data-ttu-id="9aad9-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9aad9-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="9aad9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aad9-102">SYNOPSIS</span></span>
<span data-ttu-id="9aad9-103">Удаление определения политики.</span><span class="sxs-lookup"><span data-stu-id="9aad9-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aad9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aad9-104">SYNTAX</span></span>

### <span data-ttu-id="9aad9-105">Параметр имени определения политики задает.</span><span class="sxs-lookup"><span data-stu-id="9aad9-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="9aad9-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="9aad9-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aad9-107">Параметр идентификатора определения политики задает значение.</span><span class="sxs-lookup"><span data-stu-id="9aad9-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aad9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aad9-108">DESCRIPTION</span></span>
<span data-ttu-id="9aad9-109">Командлет **Remove-AzureRmPolicySetDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="9aad9-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="9aad9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aad9-110">EXAMPLES</span></span>

### <span data-ttu-id="9aad9-111">Пример 1: Удаление определения политики для идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="9aad9-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="9aad9-112">Первая команда получает определение политики с помощью командлета Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="9aad9-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="9aad9-113">Команда сохраняет его в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="9aad9-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="9aad9-114">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="9aad9-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="9aad9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aad9-115">PARAMETERS</span></span>

### <span data-ttu-id="9aad9-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9aad9-116">-ApiVersion</span></span>
<span data-ttu-id="9aad9-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9aad9-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9aad9-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="9aad9-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9aad9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9aad9-119">-Force</span></span>
<span data-ttu-id="9aad9-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9aad9-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9aad9-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9aad9-121">-Id</span></span>
<span data-ttu-id="9aad9-122">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="9aad9-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="9aad9-123">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9aad9-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="9aad9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9aad9-124">-Name</span></span>
<span data-ttu-id="9aad9-125">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="9aad9-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="9aad9-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="9aad9-126">-Pre</span></span>
<span data-ttu-id="9aad9-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="9aad9-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9aad9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9aad9-128">-Confirm</span></span>
<span data-ttu-id="9aad9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9aad9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aad9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aad9-130">-WhatIf</span></span>
<span data-ttu-id="9aad9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9aad9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aad9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9aad9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aad9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aad9-133">-DefaultProfile</span></span>
<span data-ttu-id="9aad9-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9aad9-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aad9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aad9-135">CommonParameters</span></span>
<span data-ttu-id="9aad9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aad9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aad9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aad9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aad9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aad9-138">INPUTS</span></span>

### <span data-ttu-id="9aad9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9aad9-139">System.String</span></span>

## <span data-ttu-id="9aad9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aad9-140">OUTPUTS</span></span>

### <span data-ttu-id="9aad9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9aad9-141">System.Boolean</span></span>

## <span data-ttu-id="9aad9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aad9-142">NOTES</span></span>

## <span data-ttu-id="9aad9-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aad9-143">RELATED LINKS</span></span>

