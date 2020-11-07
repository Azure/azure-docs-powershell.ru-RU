---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 75e750aa13df16deb5c281a5914a6c21a1740e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734244"
---
# <span data-ttu-id="25bd6-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="25bd6-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="25bd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="25bd6-103">Удаляет управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="25bd6-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25bd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25bd6-104">SYNTAX</span></span>

### <span data-ttu-id="25bd6-105">Заданный параметр имени управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="25bd6-105">The managed application name parameter set.</span></span> <span data-ttu-id="25bd6-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="25bd6-106">(Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25bd6-107">Заданный параметр идентификатора управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="25bd6-107">The managed application Id parameter set.</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25bd6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25bd6-108">DESCRIPTION</span></span>
<span data-ttu-id="25bd6-109">Командлет **Remove-AzureRmManagedApplication** удаляет управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="25bd6-109">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="25bd6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25bd6-110">EXAMPLES</span></span>

### <span data-ttu-id="25bd6-111">Пример 1: Удаление управляемого приложения по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="25bd6-111">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="25bd6-112">Первая команда получает управляемое приложение с именем myApp с помощью командлета Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="25bd6-112">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="25bd6-113">Команда сохраняет его в переменной $Application.</span><span class="sxs-lookup"><span data-stu-id="25bd6-113">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="25bd6-114">Вторая команда удаляет управляемое приложение, определяемое свойством **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="25bd6-114">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="25bd6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25bd6-115">PARAMETERS</span></span>

### <span data-ttu-id="25bd6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="25bd6-116">-ApiVersion</span></span>
<span data-ttu-id="25bd6-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25bd6-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="25bd6-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="25bd6-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="25bd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bd6-119">-DefaultProfile</span></span>
<span data-ttu-id="25bd6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25bd6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25bd6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="25bd6-121">-Force</span></span>
<span data-ttu-id="25bd6-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="25bd6-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="25bd6-123">-ID</span><span class="sxs-lookup"><span data-stu-id="25bd6-123">-Id</span></span>
<span data-ttu-id="25bd6-124">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="25bd6-124">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="25bd6-125">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="25bd6-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bd6-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25bd6-126">-Name</span></span>
<span data-ttu-id="25bd6-127">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="25bd6-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bd6-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="25bd6-128">-Pre</span></span>
<span data-ttu-id="25bd6-129">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="25bd6-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="25bd6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bd6-130">-ResourceGroupName</span></span>
<span data-ttu-id="25bd6-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25bd6-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25bd6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25bd6-132">-Confirm</span></span>
<span data-ttu-id="25bd6-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25bd6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25bd6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25bd6-134">-WhatIf</span></span>
<span data-ttu-id="25bd6-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25bd6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25bd6-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25bd6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25bd6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bd6-137">CommonParameters</span></span>
<span data-ttu-id="25bd6-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25bd6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bd6-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bd6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bd6-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25bd6-140">INPUTS</span></span>

### <span data-ttu-id="25bd6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="25bd6-141">System.String</span></span>

## <span data-ttu-id="25bd6-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25bd6-142">OUTPUTS</span></span>

### <span data-ttu-id="25bd6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25bd6-143">System.Boolean</span></span>

## <span data-ttu-id="25bd6-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="25bd6-144">NOTES</span></span>

## <span data-ttu-id="25bd6-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25bd6-145">RELATED LINKS</span></span>

