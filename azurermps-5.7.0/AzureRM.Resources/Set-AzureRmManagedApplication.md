---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 870769c6bb2557b2a654b4625d3f2c7ea1b4293e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561516"
---
# <span data-ttu-id="1fd62-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="1fd62-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="1fd62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fd62-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd62-103">Обновляет управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="1fd62-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fd62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fd62-104">SYNTAX</span></span>

### <span data-ttu-id="1fd62-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fd62-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fd62-106">SetById</span><span class="sxs-lookup"><span data-stu-id="1fd62-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd62-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd62-107">DESCRIPTION</span></span>
<span data-ttu-id="1fd62-108">Командлет **Set-AzureRmManagedApplication** обновляет управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="1fd62-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="1fd62-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fd62-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd62-110">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="1fd62-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="1fd62-111">Эта команда обновляет описание управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="1fd62-111">This command updates the managed application description</span></span>

## <span data-ttu-id="1fd62-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fd62-112">PARAMETERS</span></span>

### <span data-ttu-id="1fd62-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1fd62-113">-ApiVersion</span></span>
<span data-ttu-id="1fd62-114">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd62-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1fd62-115">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="1fd62-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1fd62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd62-116">-DefaultProfile</span></span>
<span data-ttu-id="1fd62-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd62-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fd62-118">-ID</span><span class="sxs-lookup"><span data-stu-id="1fd62-118">-Id</span></span>
<span data-ttu-id="1fd62-119">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="1fd62-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="1fd62-120">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd62-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="1fd62-121">-Видах</span><span class="sxs-lookup"><span data-stu-id="1fd62-121">-Kind</span></span>
<span data-ttu-id="1fd62-122">Управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="1fd62-122">The managed application kind.</span></span>
<span data-ttu-id="1fd62-123">Один из решений Marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="1fd62-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="1fd62-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1fd62-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="1fd62-125">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd62-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="1fd62-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd62-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="1fd62-127">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd62-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="1fd62-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fd62-128">-Name</span></span>
<span data-ttu-id="1fd62-129">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="1fd62-129">The managed application name.</span></span>

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

### <span data-ttu-id="1fd62-130">-Параметр</span><span class="sxs-lookup"><span data-stu-id="1fd62-130">-Parameter</span></span>
<span data-ttu-id="1fd62-131">Форматированная строка JSON параметров управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="1fd62-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="1fd62-132">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему параметры, или параметрам в виде строки.</span><span class="sxs-lookup"><span data-stu-id="1fd62-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="1fd62-133">-Планирование</span><span class="sxs-lookup"><span data-stu-id="1fd62-133">-Plan</span></span>
<span data-ttu-id="1fd62-134">Хэш-таблица, представляющая свойства плана управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="1fd62-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd62-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="1fd62-135">-Pre</span></span>
<span data-ttu-id="1fd62-136">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="1fd62-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1fd62-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd62-137">-ResourceGroupName</span></span>
<span data-ttu-id="1fd62-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd62-138">The resource group name.</span></span>

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

### <span data-ttu-id="1fd62-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="1fd62-139">-Tag</span></span>
<span data-ttu-id="1fd62-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fd62-140">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd62-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fd62-141">-Confirm</span></span>
<span data-ttu-id="1fd62-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fd62-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd62-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd62-143">-WhatIf</span></span>
<span data-ttu-id="1fd62-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fd62-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd62-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fd62-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd62-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd62-146">CommonParameters</span></span>
<span data-ttu-id="1fd62-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fd62-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd62-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd62-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd62-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fd62-149">INPUTS</span></span>

### <span data-ttu-id="1fd62-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1fd62-150">System.String</span></span>
<span data-ttu-id="1fd62-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1fd62-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1fd62-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd62-152">OUTPUTS</span></span>

### <span data-ttu-id="1fd62-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1fd62-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1fd62-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fd62-154">NOTES</span></span>

## <span data-ttu-id="1fd62-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fd62-155">RELATED LINKS</span></span>
