---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 3897282708c310d59dffba52b3f5abfdf78d5f77
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915029"
---
# <span data-ttu-id="cc553-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="cc553-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="cc553-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc553-102">SYNOPSIS</span></span>
<span data-ttu-id="cc553-103">Удаляет управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="cc553-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc553-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc553-104">SYNTAX</span></span>

### <span data-ttu-id="cc553-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc553-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc553-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="cc553-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc553-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc553-107">DESCRIPTION</span></span>
<span data-ttu-id="cc553-108">Командлет **Remove-AzureRmManagedApplication** удаляет управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="cc553-108">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="cc553-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc553-109">EXAMPLES</span></span>

### <span data-ttu-id="cc553-110">Пример 1: Удаление управляемого приложения по ИДЕНТИФИКАТОРу ресурса</span><span class="sxs-lookup"><span data-stu-id="cc553-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="cc553-111">Первая команда получает управляемое приложение с именем myApp с помощью командлета Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="cc553-111">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="cc553-112">Команда сохраняет его в переменной $Application.</span><span class="sxs-lookup"><span data-stu-id="cc553-112">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="cc553-113">Вторая команда удаляет управляемое приложение, определяемое свойством **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="cc553-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="cc553-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc553-114">PARAMETERS</span></span>

### <span data-ttu-id="cc553-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc553-115">-ApiVersion</span></span>
<span data-ttu-id="cc553-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc553-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="cc553-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="cc553-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="cc553-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc553-118">-DefaultProfile</span></span>
<span data-ttu-id="cc553-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc553-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc553-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cc553-120">-Force</span></span>
<span data-ttu-id="cc553-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cc553-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc553-122">-ID</span><span class="sxs-lookup"><span data-stu-id="cc553-122">-Id</span></span>
<span data-ttu-id="cc553-123">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="cc553-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="cc553-124">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="cc553-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="cc553-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc553-125">-Name</span></span>
<span data-ttu-id="cc553-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="cc553-126">The managed application name.</span></span>

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

### <span data-ttu-id="cc553-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc553-127">-Pre</span></span>
<span data-ttu-id="cc553-128">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="cc553-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cc553-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc553-129">-ResourceGroupName</span></span>
<span data-ttu-id="cc553-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc553-130">The resource group name.</span></span>

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

### <span data-ttu-id="cc553-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc553-131">-Confirm</span></span>
<span data-ttu-id="cc553-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc553-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc553-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc553-133">-WhatIf</span></span>
<span data-ttu-id="cc553-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc553-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc553-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc553-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc553-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc553-136">CommonParameters</span></span>
<span data-ttu-id="cc553-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc553-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc553-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc553-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc553-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc553-139">INPUTS</span></span>

### <span data-ttu-id="cc553-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cc553-140">System.String</span></span>

## <span data-ttu-id="cc553-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc553-141">OUTPUTS</span></span>

### <span data-ttu-id="cc553-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc553-142">System.Boolean</span></span>

## <span data-ttu-id="cc553-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc553-143">NOTES</span></span>

## <span data-ttu-id="cc553-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc553-144">RELATED LINKS</span></span>
