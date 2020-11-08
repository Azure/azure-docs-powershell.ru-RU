---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236413"
---
# <span data-ttu-id="47dcd-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="47dcd-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="47dcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="47dcd-103">Удаляет управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="47dcd-103">Removes a managed application</span></span>

## <span data-ttu-id="47dcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47dcd-104">SYNTAX</span></span>

### <span data-ttu-id="47dcd-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47dcd-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47dcd-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="47dcd-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47dcd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47dcd-107">DESCRIPTION</span></span>
<span data-ttu-id="47dcd-108">Командлет **Remove-AzManagedApplication** удаляет управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="47dcd-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="47dcd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47dcd-109">EXAMPLES</span></span>

### <span data-ttu-id="47dcd-110">Пример 1: Удаление управляемого приложения по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="47dcd-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="47dcd-111">Первая команда получает управляемое приложение с именем myApp с помощью командлета Get-AzManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="47dcd-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="47dcd-112">Команда сохраняет его в переменной $Application.</span><span class="sxs-lookup"><span data-stu-id="47dcd-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="47dcd-113">Вторая команда удаляет управляемое приложение, определяемое свойством **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="47dcd-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="47dcd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47dcd-114">PARAMETERS</span></span>

### <span data-ttu-id="47dcd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="47dcd-115">-ApiVersion</span></span>
<span data-ttu-id="47dcd-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47dcd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="47dcd-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="47dcd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="47dcd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dcd-118">-DefaultProfile</span></span>
<span data-ttu-id="47dcd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47dcd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47dcd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="47dcd-120">-Force</span></span>
<span data-ttu-id="47dcd-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="47dcd-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47dcd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="47dcd-122">-Id</span></span>
<span data-ttu-id="47dcd-123">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="47dcd-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="47dcd-124">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="47dcd-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="47dcd-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47dcd-125">-Name</span></span>
<span data-ttu-id="47dcd-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="47dcd-126">The managed application name.</span></span>

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

### <span data-ttu-id="47dcd-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="47dcd-127">-Pre</span></span>
<span data-ttu-id="47dcd-128">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="47dcd-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="47dcd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47dcd-129">-ResourceGroupName</span></span>
<span data-ttu-id="47dcd-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47dcd-130">The resource group name.</span></span>

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

### <span data-ttu-id="47dcd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47dcd-131">-Confirm</span></span>
<span data-ttu-id="47dcd-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47dcd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47dcd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dcd-133">-WhatIf</span></span>
<span data-ttu-id="47dcd-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47dcd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47dcd-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47dcd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47dcd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dcd-136">CommonParameters</span></span>
<span data-ttu-id="47dcd-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47dcd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dcd-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47dcd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dcd-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47dcd-139">INPUTS</span></span>

### <span data-ttu-id="47dcd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="47dcd-140">System.String</span></span>

## <span data-ttu-id="47dcd-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47dcd-141">OUTPUTS</span></span>

### <span data-ttu-id="47dcd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47dcd-142">System.Boolean</span></span>

## <span data-ttu-id="47dcd-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="47dcd-143">NOTES</span></span>

## <span data-ttu-id="47dcd-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47dcd-144">RELATED LINKS</span></span>
