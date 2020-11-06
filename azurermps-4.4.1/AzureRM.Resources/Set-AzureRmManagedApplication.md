---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562188"
---
# <span data-ttu-id="80d2f-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="80d2f-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="80d2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="80d2f-103">Обновляет управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="80d2f-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80d2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80d2f-104">SYNTAX</span></span>

### <span data-ttu-id="80d2f-105">Заданный параметр имени управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="80d2f-105">The managed application name parameter set.</span></span> <span data-ttu-id="80d2f-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="80d2f-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d2f-107">Заданный параметр идентификатора управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="80d2f-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d2f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80d2f-108">DESCRIPTION</span></span>
<span data-ttu-id="80d2f-109">Командлет **Set-AzureRmManagedApplication** обновляет управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="80d2f-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="80d2f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80d2f-110">EXAMPLES</span></span>

### <span data-ttu-id="80d2f-111">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="80d2f-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="80d2f-112">Эта команда обновляет описание управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="80d2f-112">This command updates the managed application description</span></span>

## <span data-ttu-id="80d2f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80d2f-113">PARAMETERS</span></span>

### <span data-ttu-id="80d2f-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="80d2f-114">-ApiVersion</span></span>
<span data-ttu-id="80d2f-115">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80d2f-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="80d2f-116">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="80d2f-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="80d2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d2f-117">-DefaultProfile</span></span>
<span data-ttu-id="80d2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80d2f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80d2f-119">-Видах</span><span class="sxs-lookup"><span data-stu-id="80d2f-119">-Kind</span></span>
<span data-ttu-id="80d2f-120">Управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="80d2f-120">The managed application kind.</span></span>
<span data-ttu-id="80d2f-121">Один из решений Marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="80d2f-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="80d2f-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="80d2f-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="80d2f-123">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80d2f-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="80d2f-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d2f-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="80d2f-125">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80d2f-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="80d2f-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80d2f-126">-Name</span></span>
<span data-ttu-id="80d2f-127">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="80d2f-127">The managed application name.</span></span>

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

### <span data-ttu-id="80d2f-128">-Параметр</span><span class="sxs-lookup"><span data-stu-id="80d2f-128">-Parameter</span></span>
<span data-ttu-id="80d2f-129">Форматированная строка JSON параметров управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="80d2f-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="80d2f-130">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему параметры, или параметрам в виде строки.</span><span class="sxs-lookup"><span data-stu-id="80d2f-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="80d2f-131">-Планирование</span><span class="sxs-lookup"><span data-stu-id="80d2f-131">-Plan</span></span>
<span data-ttu-id="80d2f-132">Хэш-таблица, представляющая свойства плана управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="80d2f-132">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d2f-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="80d2f-133">-Pre</span></span>
<span data-ttu-id="80d2f-134">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="80d2f-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="80d2f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d2f-135">-ResourceGroupName</span></span>
<span data-ttu-id="80d2f-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80d2f-136">The resource group name.</span></span>

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

### <span data-ttu-id="80d2f-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="80d2f-137">-Tag</span></span>
<span data-ttu-id="80d2f-138">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80d2f-138">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d2f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80d2f-139">-Confirm</span></span>
<span data-ttu-id="80d2f-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80d2f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d2f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d2f-141">-WhatIf</span></span>
<span data-ttu-id="80d2f-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80d2f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d2f-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80d2f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d2f-144">-ID</span><span class="sxs-lookup"><span data-stu-id="80d2f-144">-Id</span></span>
<span data-ttu-id="80d2f-145">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="80d2f-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="80d2f-146">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="80d2f-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="80d2f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d2f-147">CommonParameters</span></span>
<span data-ttu-id="80d2f-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80d2f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d2f-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80d2f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d2f-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80d2f-150">INPUTS</span></span>

### <span data-ttu-id="80d2f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="80d2f-151">System.String</span></span>
<span data-ttu-id="80d2f-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="80d2f-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80d2f-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80d2f-153">OUTPUTS</span></span>

### <span data-ttu-id="80d2f-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="80d2f-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="80d2f-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="80d2f-155">NOTES</span></span>

## <span data-ttu-id="80d2f-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80d2f-156">RELATED LINKS</span></span>

