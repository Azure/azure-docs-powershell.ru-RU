---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911823"
---
# <span data-ttu-id="1e8ca-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="1e8ca-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="1e8ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8ca-103">Создание приложения, управляемого Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="1e8ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e8ca-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e8ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e8ca-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8ca-106">Командлет **New-AzManagedApplication** создает управляемое приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="1e8ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e8ca-107">EXAMPLES</span></span>

### <span data-ttu-id="1e8ca-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e8ca-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="1e8ca-109">Эта команда создает управляемое приложение</span><span class="sxs-lookup"><span data-stu-id="1e8ca-109">This command creates a managed application</span></span>

## <span data-ttu-id="1e8ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e8ca-110">PARAMETERS</span></span>

### <span data-ttu-id="1e8ca-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e8ca-111">-ApiVersion</span></span>
<span data-ttu-id="1e8ca-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1e8ca-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1e8ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8ca-114">-DefaultProfile</span></span>
<span data-ttu-id="1e8ca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e8ca-116">-Видах</span><span class="sxs-lookup"><span data-stu-id="1e8ca-116">-Kind</span></span>
<span data-ttu-id="1e8ca-117">Управляемое приложение.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-117">The managed application kind.</span></span>
<span data-ttu-id="1e8ca-118">Один из решений Marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="1e8ca-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="1e8ca-119">-Location</span><span class="sxs-lookup"><span data-stu-id="1e8ca-119">-Location</span></span>
<span data-ttu-id="1e8ca-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-120">The resource location.</span></span>

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

### <span data-ttu-id="1e8ca-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1e8ca-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="1e8ca-122">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="1e8ca-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8ca-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="1e8ca-124">Имя управляемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="1e8ca-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e8ca-125">-Name</span></span>
<span data-ttu-id="1e8ca-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-126">The managed application name.</span></span>

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

### <span data-ttu-id="1e8ca-127">-Параметр</span><span class="sxs-lookup"><span data-stu-id="1e8ca-127">-Parameter</span></span>
<span data-ttu-id="1e8ca-128">Форматированная строка JSON параметров управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="1e8ca-129">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему параметры, или параметрам в виде строки.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="1e8ca-130">-Планирование</span><span class="sxs-lookup"><span data-stu-id="1e8ca-130">-Plan</span></span>
<span data-ttu-id="1e8ca-131">Хэш-таблица, представляющая свойства плана управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="1e8ca-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e8ca-132">-Pre</span></span>
<span data-ttu-id="1e8ca-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1e8ca-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8ca-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e8ca-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-135">The resource group name.</span></span>

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

### <span data-ttu-id="1e8ca-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="1e8ca-136">-Tag</span></span>
<span data-ttu-id="1e8ca-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1e8ca-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e8ca-138">-Confirm</span></span>
<span data-ttu-id="1e8ca-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e8ca-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e8ca-140">-WhatIf</span></span>
<span data-ttu-id="1e8ca-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e8ca-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e8ca-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8ca-143">CommonParameters</span></span>
<span data-ttu-id="1e8ca-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e8ca-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8ca-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e8ca-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8ca-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e8ca-146">INPUTS</span></span>

### <span data-ttu-id="1e8ca-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1e8ca-147">System.String</span></span>

### <span data-ttu-id="1e8ca-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e8ca-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e8ca-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e8ca-149">OUTPUTS</span></span>

### <span data-ttu-id="1e8ca-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1e8ca-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1e8ca-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e8ca-151">NOTES</span></span>

## <span data-ttu-id="1e8ca-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e8ca-152">RELATED LINKS</span></span>
