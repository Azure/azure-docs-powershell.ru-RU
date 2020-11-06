---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568310"
---
# <span data-ttu-id="06b51-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="06b51-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="06b51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06b51-102">SYNOPSIS</span></span>
<span data-ttu-id="06b51-103">Удаляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="06b51-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06b51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06b51-104">SYNTAX</span></span>

### <span data-ttu-id="06b51-105">Заданный параметр имени определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="06b51-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="06b51-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="06b51-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06b51-107">Заданный параметр идентификатора определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="06b51-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b51-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06b51-108">DESCRIPTION</span></span>
<span data-ttu-id="06b51-109">Командлет **Remove-AzureRmManagedApplicationDefinition** удаляет определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="06b51-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="06b51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06b51-110">EXAMPLES</span></span>

### <span data-ttu-id="06b51-111">Пример 1: Удаление определения управляемого приложения с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="06b51-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="06b51-112">Первая команда получает определение управляемого приложения с именем myAppDef с помощью командлета Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="06b51-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="06b51-113">Команда сохраняет его в переменной $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="06b51-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="06b51-114">Вторая команда удаляет определение управляемого приложения, определяемое свойством **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="06b51-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="06b51-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06b51-115">PARAMETERS</span></span>

### <span data-ttu-id="06b51-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06b51-116">-ApiVersion</span></span>
<span data-ttu-id="06b51-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06b51-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06b51-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="06b51-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06b51-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b51-119">-DefaultProfile</span></span>
<span data-ttu-id="06b51-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06b51-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06b51-121">-Force</span><span class="sxs-lookup"><span data-stu-id="06b51-121">-Force</span></span>
<span data-ttu-id="06b51-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="06b51-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="06b51-123">-ID</span><span class="sxs-lookup"><span data-stu-id="06b51-123">-Id</span></span>
<span data-ttu-id="06b51-124">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="06b51-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="06b51-125">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="06b51-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b51-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06b51-126">-Name</span></span>
<span data-ttu-id="06b51-127">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="06b51-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b51-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="06b51-128">-Pre</span></span>
<span data-ttu-id="06b51-129">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="06b51-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06b51-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b51-130">-ResourceGroupName</span></span>
<span data-ttu-id="06b51-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06b51-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b51-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06b51-132">-Confirm</span></span>
<span data-ttu-id="06b51-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06b51-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b51-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b51-134">-WhatIf</span></span>
<span data-ttu-id="06b51-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06b51-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b51-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06b51-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b51-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b51-137">CommonParameters</span></span>
<span data-ttu-id="06b51-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06b51-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b51-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b51-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b51-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06b51-140">INPUTS</span></span>

### <span data-ttu-id="06b51-141">System. String</span><span class="sxs-lookup"><span data-stu-id="06b51-141">System.String</span></span>

## <span data-ttu-id="06b51-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06b51-142">OUTPUTS</span></span>

### <span data-ttu-id="06b51-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06b51-143">System.Boolean</span></span>

## <span data-ttu-id="06b51-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="06b51-144">NOTES</span></span>

## <span data-ttu-id="06b51-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06b51-145">RELATED LINKS</span></span>

