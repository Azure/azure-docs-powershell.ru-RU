---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318863"
---
# <span data-ttu-id="ad551-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="ad551-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="ad551-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad551-102">SYNOPSIS</span></span>
<span data-ttu-id="ad551-103">Создание приложения, управляемого Azure.</span><span class="sxs-lookup"><span data-stu-id="ad551-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="ad551-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad551-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad551-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad551-105">DESCRIPTION</span></span>
<span data-ttu-id="ad551-106">Командлет **New-AzManagedApplication** создает управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="ad551-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="ad551-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad551-107">EXAMPLES</span></span>

### <span data-ttu-id="ad551-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad551-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="ad551-109">Эта команда создает управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="ad551-109">This command creates a managed application</span></span>

## <span data-ttu-id="ad551-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad551-110">PARAMETERS</span></span>

### <span data-ttu-id="ad551-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ad551-111">-ApiVersion</span></span>
<span data-ttu-id="ad551-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad551-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ad551-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="ad551-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ad551-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad551-114">-DefaultProfile</span></span>
<span data-ttu-id="ad551-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad551-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad551-116">-Видах</span><span class="sxs-lookup"><span data-stu-id="ad551-116">-Kind</span></span>
<span data-ttu-id="ad551-117">Управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="ad551-117">The managed application kind.</span></span>
<span data-ttu-id="ad551-118">Один из решений Marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="ad551-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad551-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ad551-119">-Location</span></span>
<span data-ttu-id="ad551-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ad551-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad551-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ad551-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="ad551-122">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad551-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="ad551-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad551-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="ad551-124">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad551-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad551-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad551-125">-Name</span></span>
<span data-ttu-id="ad551-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="ad551-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad551-127">-Параметр</span><span class="sxs-lookup"><span data-stu-id="ad551-127">-Parameter</span></span>
<span data-ttu-id="ad551-128">Форматированная строка JSON параметров управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="ad551-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="ad551-129">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему параметры, или параметрам в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ad551-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="ad551-130">-Планирование</span><span class="sxs-lookup"><span data-stu-id="ad551-130">-Plan</span></span>
<span data-ttu-id="ad551-131">Хэш-таблица, представляющая свойства плана управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="ad551-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="ad551-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="ad551-132">-Pre</span></span>
<span data-ttu-id="ad551-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="ad551-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ad551-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad551-134">-ResourceGroupName</span></span>
<span data-ttu-id="ad551-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad551-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad551-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="ad551-136">-Tag</span></span>
<span data-ttu-id="ad551-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad551-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ad551-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad551-138">-Confirm</span></span>
<span data-ttu-id="ad551-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad551-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad551-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad551-140">-WhatIf</span></span>
<span data-ttu-id="ad551-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad551-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad551-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad551-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad551-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad551-143">CommonParameters</span></span>
<span data-ttu-id="ad551-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad551-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad551-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad551-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad551-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad551-146">INPUTS</span></span>

### <span data-ttu-id="ad551-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ad551-147">System.String</span></span>

### <span data-ttu-id="ad551-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad551-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad551-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad551-149">OUTPUTS</span></span>

### <span data-ttu-id="ad551-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ad551-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ad551-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad551-151">NOTES</span></span>

## <span data-ttu-id="ad551-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad551-152">RELATED LINKS</span></span>